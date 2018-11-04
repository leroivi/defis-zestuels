cmake_minimum_required (VERSION 3.2)

# Define library. Only source files here!
project(zFraction VERSION 0.1 LANGUAGES CXX)

add_library(zFraction
	src/zFraction.cpp)

# Define headers for this library. PUBLIC headers are used for
# compiling the library, and will be added to consumers' build
# paths.
target_include_directories(zFraction PUBLIC
	$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
	$<INSTALL_INTERFACE:include>
	PRIVATE src)

# Every library has unit tests, of course
find_package(Boost 1.68.0)
if(Boost_FOUND)
	include_directories(${Boost_INCLUDE_DIRS})
	add_executable(testZFraction
		tests/main.cpp)
	target_link_libraries(testZFraction
		zFraction
		${Boost_LIBRARIES})
	add_test(testZFraction testZFraction)
endif()