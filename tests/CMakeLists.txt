message(status, "building unittests")

include_directories(
        ${CMAKE_SOURCE_DIR}/dag/
        ${CMAKE_CURRENT_SOURCE_DIR}
)
file(GLOB headers *.h)

add_executable(tests unittest.cpp )
target_link_libraries(tests)

# --- adding tests for examples ------------------------------
add_test(NAME tests COMMAND tests)







