#cmake .. -G "Visual Studio 17 2022"

cmake_minimum_required(VERSION 3.13.4)
project(standalone-dialect LANGUAGES CXX C)

Set(CMAKE_BUILD_WITH_INSTALL_NAME_DIR ON)
set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_STANDARD 20 CACHE STRING "C++ standard to conform to")

set(LLVM_ENABLE_PROJECTS mlir)
set(LLVM_BUILD_EXAMPLES ON)
set(LLVM_TARGETS_TO_BUILD "host")
set(MAKE_BUILD_TYPE Debug)
set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_OSX_ARCHITECTURES x86_64)
set(CMAKE_INSTALL_PREFIX d:/bin)
#  -Thost=x64 

add_subdirectory(zstd/build/cmake)
add_subdirectory(llvm-project/llvm)

