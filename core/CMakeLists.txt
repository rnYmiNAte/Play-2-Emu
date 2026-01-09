cmake_minimum_required(VERSION 3.10)
project(Play2EmuCore LANGUAGES C CXX)

# Set compile flags
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -Wextra")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra")

# Include subdirectories
add_subdirectory(src/cpu)
add_subdirectory(src/gpu)
add_subdirectory(src/disc)
add_subdirectory(src/bios)
add_subdirectory(src/utils)
add_subdirectory(third_party)
add_subdirectory(tests)

# Build core library
add_library(play2emu_core STATIC
    $<TARGET_OBJECTS:cpu_module>
    $<TARGET_OBJECTS:gpu_module>
    $<TARGET_OBJECTS:disc_module>
    $<TARGET_OBJECTS:bios_module>
    $<TARGET_OBJECTS:utils_module>
)

# Link dependencies
target_link_libraries(play2emu_core PRIVATE
    libchdr
    miniz
)

# Export public headers
target_include_directories(play2emu_core PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)
