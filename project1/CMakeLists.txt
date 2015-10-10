cmake_minimum_required(VERSION 2.8)

PROJECT(proj1)
SET(VTK_DIR ~/VTK6.0.0)

find_package(VTK REQUIRED)
include(${VTK_USE_FILE})

add_executable(proj1  proj1)

#SET(CMAKE_CXX_LINK_FLAGS "-framework OpenGL")

if(VTK_LIBRARIES)
  target_link_libraries(proj1 ${VTK_LIBRARIES})
else()
  target_link_libraries(proj1 vtkHybrid)
endif()


