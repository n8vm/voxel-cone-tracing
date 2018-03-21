# ┌──────────────────────────────────────────────────────────────────┐
# │  Projects Settings                                               │
# └──────────────────────────────────────────────────────────────────┘
cmake_minimum_required (VERSION 3.10)
project(voxel-cone-tracing)
set_property(GLOBAL PROPERTY USE_FOLDERS ON)
include(${PROJECT_SOURCE_DIR}/CMakeGenerateHierarchy.txt)

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/CMakeModules)

# Use c++17
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
if(MSVC)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /std:c++17")
endif(MSVC)

# ┌──────────────────────────────────────────────────────────────────┐
# │  Definitions                                                     │
# └──────────────────────────────────────────────────────────────────┘

# add_definitions(-DResourcePath="${CMAKE_CURRENT_SOURCE_DIR}/resources/")

# ┌──────────────────────────────────────────────────────────────────┐
# │  Load libraries                                                  │
# └──────────────────────────────────────────────────────────────────┘

find_package(OpenGL REQUIRED)

# glfw
find_package(GLFW REQUIRED)
include_directories(SYSTEM ${GLFW_INCLUDE_DIR})

# glew
find_package(GLEW REQUIRED)
include_directories(SYSTEM ${GLEW_INCLUDE_DIR})

# glm
find_package(GLM REQUIRED)
include_directories(SYSTEM ${GLM_INCLUDE_DIRS})

# AntTweakBar
find_package(AntTweakBar REQUIRED)
include_directories(SYSTEM ${ANT_TWEAK_BAR_INCLUDE_DIR})

# soil
find_package(SOIL REQUIRED)
include_directories(SYSTEM ${SOIL_INCLUDE_DIRS})

set(LIBRARIES
	${ANT_TWEAK_BAR_LIBRARY}
	${GLEW_LIBRARY}
	${GLFW_LIBRARIES}
	${SOIL_LIBRARIES}
	${OPENGL_gl_LIBRARY})

# ┌──────────────────────────────────────────────────────────────────┐
# │  Add source files                                                │
# └──────────────────────────────────────────────────────────────────┘
add_subdirectory(Source)

# ┌──────────────────────────────────────────────────────────────────┐
# │  Build executable                                                │
# └──────────────────────────────────────────────────────────────────┘
add_executable (Voxel_Cone_Tracing "${Source_SRC}" voxel-cone-tracing.cpp)
target_link_libraries (Voxel_Cone_Tracing ${LIBRARIES})
generate_folder_hierarchy("${Source_SRC}" voxel-cone-tracing.cpp)