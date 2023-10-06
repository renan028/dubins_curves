cmake_minimum_required(VERSION 3.10)
project(dubins_curves)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(catkin REQUIRED COMPONENTS roscpp)

catkin_package(
    INCLUDE_DIRS include
    LIBRARIES dubins_curves
)

include_directories(
    include
    ${catkin_INCLUDE_DIRS}
)

add_library(dubins_curves src/dubins.cpp)
target_link_libraries(dubins_curves ${catkin_LIBRARIES})

install(TARGETS dubins_curves
    ARCHIVE DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
    LIBRARY DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
)

install(DIRECTORY include/${PROJECT_NAME}/
    DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
)
