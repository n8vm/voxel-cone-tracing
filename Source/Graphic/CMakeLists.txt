add_subdirectory(Camera)
add_subdirectory(FBO)
add_subdirectory(Lighting)
add_subdirectory(Material)
add_subdirectory(Renderer)

set(Graphic_SRC
	${Camera_SRC}
	${FBO_SRC}
	${Lighting_SRC}
	${Material_SRC}
	${Renderer_SRC}
	${CMAKE_CURRENT_SOURCE_DIR}/CMakeLists.txt
	${CMAKE_CURRENT_SOURCE_DIR}/Graphics.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Graphics.h
	${CMAKE_CURRENT_SOURCE_DIR}/Texture2D.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Texture2D.h
	${CMAKE_CURRENT_SOURCE_DIR}/Texture3D.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Texture3D.h
	PARENT_SCOPE)