add_subdirectory(Scenes)
add_subdirectory(Templates)

set(Scene_SRC
	${Scenes_SRC}
	${Templates_SRC}
	${CMAKE_CURRENT_SOURCE_DIR}/CMakeLists.txt
	${CMAKE_CURRENT_SOURCE_DIR}/Scene.h
	${CMAKE_CURRENT_SOURCE_DIR}/ScenePack.h
	PARENT_SCOPE)