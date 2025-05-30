# Root CMake for the project
cmake_minimum_required(VERSION 3.23)

# project info
project(
  FtMatrix
  VERSION 0.1
  DESCRIPTION "Matrix library for ecole42."
  LANGUAGES CXX)

# C++ compiler setting
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# 라이브러리 파일은 빌드 디렉토리 안에 lib 폴더에 출력.
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)

# 실행 파일은 빌드 디렉토리 안에 bin 폴더에 출력.
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# activate ctest
enable_testing()

# sub dir path setting
# sub dir must have it's own cmake
add_subdirectory(src)	# actual implementation
add_subdirectory(tests)	# test framework, GoogleTest
