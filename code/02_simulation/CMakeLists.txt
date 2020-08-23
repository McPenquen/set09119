project(02_simulation)
cmake_minimum_required(VERSION 3.17)
set(CMAKE_CXX_STANDARD 17)

set(SOURCE_FILES
    02_simulation.cpp
	Mesh.cpp
	OBJLoader.cpp
	Application.cpp
	Path.cpp
)

set(HEADER_FILES
	Mesh.h
	OBJLoader.h
	Application.h
	Shader.h
	Camera.h
	Path.h
)

set( ALL_SOURCE_FILES ${SOURCE_FILES} ${HEADER_FILES} )
include_directories( ${INCLUDE_DIRS} )
add_executable(02_simulation ${ALL_SOURCE_FILES} )
set_target_properties(02_simulation PROPERTIES OUTPUT_NAME 02_simulation CLEAN_DIRECT_OUTPUT 1 DEBUG_POSTFIX "d")
target_link_libraries(02_simulation ${LIBRARIES} )

