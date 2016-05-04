# ADD OUR TEST EXECUTABLES
set(SOURCE_FILES main_test.cpp)
add_executable(main_test main_test.cpp)
target_link_libraries(main_test ${Boost_LIBRARIES})
# OUR TEST NEEDS THIS EXECUTABLE TO BE BUILT FIRST...
add_dependencies(main_test main)

# ADD OUR TESTS
add_test(NAME test_main COMMAND main_test)