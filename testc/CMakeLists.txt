cmake_minimum_required(VERSION 2.8)
aux_source_directory(. SRC_LIST)

set (EXE_NAME "testc")
set (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -g -O0")
add_executable(${EXE_NAME} ${SRC_LIST})

TARGET_LINK_LIBRARIES(${EXE_NAME}
                        cstacktrace
)
