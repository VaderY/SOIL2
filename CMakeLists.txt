cmake_minimum_required(VERSION 2.6)
project(soil2)

include_directories(include)

add_library(soil2 STATIC
	src/SOIL2/image_DXT.c
	src/SOIL2/image_helper.c
	src/SOIL2/SOIL2.c
	src/SOIL2/wfETC.c
)

install(FILES src/SOIL2/SOIL2.h DESTINATION include/SOIL2/)
install(TARGETS soil2
    ARCHIVE DESTINATION lib
)