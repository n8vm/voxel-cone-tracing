add_subdirectory(External)

set(Utility_SRC
	${External_SRC}
	${CMAKE_CURRENT_SOURCE_DIR}/CMakeLists.txt
	${CMAKE_CURRENT_SOURCE_DIR}/ObjLoader.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ObjLoader.h
	PARENT_SCOPE)