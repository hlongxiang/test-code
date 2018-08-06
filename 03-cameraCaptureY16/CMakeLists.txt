# cmake for OpenCV2 Cookbook
# your opencv/build directory should be in your system PATH

# set minimum required version for cmake
cmake_minimum_required(VERSION 2.8)

# define the project name
set(project_name "03-cameraCaptureY16")

# set the project namee
project("${project_name}")

# add opencv package to the project
set(OpenCV_DIR C:/Opencv/result/opencv-3.4.0)
find_package( OpenCV REQUIRED )
MESSAGE(“OpenCV version : ${OpenCV_VERSION}”)

# add opencv include directories to the project
include_directories( ${OpenCV_INCLUDE_DIRS} ) 

# add executable
add_executable(CU51Capture main.cpp)

# link libraries
target_link_libraries(CU51Capture ${OpenCV_LIBS})
