cmake_minimum_required(VERSION 3.25)

set(
        Tests
        programTests
)

set(
        Test_Sources
        test.cpp
)

add_executable(
        ${Tests}
        ${Test_Sources}
)

target_link_libraries(
        ${Tests}
        PUBLIC
        GTest::gtest_main
        ${PROJECT_NAME}
)

add_test(
        NAME ${Tests}
        COMMAND ${Tests}
)