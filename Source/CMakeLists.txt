add_subdirectory(Graphic)
add_subdirectory(Scene)
add_subdirectory(Shape)
add_subdirectory(Time)
add_subdirectory(Utility)

set(Source_SRC
	${Graphic_SRC}
	${Shape_SRC}
	${Scene_SRC}
	${Time_SRC}
	${Utility_SRC}
	${CMAKE_CURRENT_SOURCE_DIR}/CMakeLists.txt
	${CMAKE_CURRENT_SOURCE_DIR}/Application.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Application.h
	PARENT_SCOPE)