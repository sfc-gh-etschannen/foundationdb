if(NOT OPEN_FOR_IDE)
  # flow bindings currently doesn't support that
  add_subdirectory(c)
  add_subdirectory(flow)
endif()
add_subdirectory(python)
if(WITH_JAVA)
  add_subdirectory(java)
endif()
if(WITH_GO AND NOT OPEN_FOR_IDE)
  add_subdirectory(go)
endif()
if(WITH_RUBY)
  add_subdirectory(ruby)
endif()
if(NOT WIN32 AND NOT OPEN_FOR_IDE)
  package_bindingtester()
endif()
