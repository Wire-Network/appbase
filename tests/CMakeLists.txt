file(GLOB UNIT_TESTS "*.cpp")
add_executable( appbase_test ${UNIT_TESTS} )
target_link_libraries( appbase_test appbase ${CMAKE_DL_LIBS} ${PLATFORM_SPECIFIC_LIBS} )
# Does not appear to be needed. If needed seems like it should be Boost::unit_test_framework.
#if(TARGET Boost::asio)
#   target_link_libraries( appbase_test Boost::included_unit_test_framework )
#endif()

add_test( appbase_test appbase_test )
