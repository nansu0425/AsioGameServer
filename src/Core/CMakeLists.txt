# Find and link libraries
find_package(spdlog CONFIG REQUIRED)

# Add source to this static library.
add_library(Core STATIC
    "Context.h" "Context.cpp"
    "LockQueue.h" "LockQueue.cpp"
    "Timer.h" "Timer.cpp"
)

# Enable precompiled headers using CMake's built-in support
target_precompile_headers(Core PRIVATE 
    "${CMAKE_CURRENT_SOURCE_DIR}/Pch.h"
)

# Link libraries
target_link_libraries(Core PUBLIC
    spdlog::spdlog
)

# Add include directories
target_include_directories(Core PUBLIC
    "${CMAKE_CURRENT_SOURCE_DIR}/.."
)
