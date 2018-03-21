add_subdirectory(Controllers)

set(Camera_SRC
	${Controllers_SRC}
	${CMAKE_CURRENT_SOURCE_DIR}/Camera.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Camera.h
	${CMAKE_CURRENT_SOURCE_DIR}/CMakeLists.txt
	${CMAKE_CURRENT_SOURCE_DIR}/OrthographicCamera.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/OrthographicCamera.h
	${CMAKE_CURRENT_SOURCE_DIR}/PerspectiveCamera.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/PerspectiveCamera.h
	PARENT_SCOPE)