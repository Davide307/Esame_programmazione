# 'Google_test' is the subproject name
project(Google_tests)

# 'lib' is the folder with Google Test sources
add_subdirectory(lib)
include_directories(${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})

# 'Google_Tests_run' is the target name
# 'test1.cpp tests2.cpp' are source files with tests

add_executable(Game_test TestObjects.cpp TestCollision.cpp TestStrategyEnemy.cpp TestLevelManager.cpp)
target_link_libraries(Game_test gtest gtest_main core sfml-graphics sfml-window sfml-system sfml-audio)