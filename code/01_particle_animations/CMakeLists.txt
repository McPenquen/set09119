project(01_particle_animations)
cmake_minimum_required(VERSION 3.17)
set(CMAKE_CXX_STANDARD 17)

set(SOURCE_FILES
    01_particle_animations.cpp
	Mesh.cpp
	OBJLoader.cpp
	Path.cpp
)

set(HEADER_FILES
	Mesh.h
	OBJLoader.h
	Shader.h
	Camera.h
	Path.h
)

set( ALL_SOURCE_FILES ${SOURCE_FILES} ${HEADER_FILES} )
include_directories( ${INCLUDE_DIRS} )
add_executable(01_particle_animations ${ALL_SOURCE_FILES} )
set_target_properties(01_particle_animations PROPERTIES OUTPUT_NAME 01_particle_animations CLEAN_DIRECT_OUTPUT 1 DEBUG_POSTFIX "d")
target_link_libraries(01_particle_animations ${LIBRARIES} )

