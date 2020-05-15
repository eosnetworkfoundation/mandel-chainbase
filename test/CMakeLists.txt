file(GLOB UNIT_TESTS "*.cpp")
add_executable( chainbase_test ${UNIT_TESTS}  )
target_link_libraries( chainbase_test  chainbase Boost::unit_test_framework ${OPENSSL_LIBRARIES} ${PLATFORM_SPECIFIC_LIBS} )

add_test(NAME test_chainbase COMMAND chainbase_test WORKING_DIRECTORY ${CMAKE_BINARY_DIR})
