# 包括的头文件目录
INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/lib/)

#INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR})
#INCLUDE_DIRECTORIES(${PROJECT_BINARY_DIR})

INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR})
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_BINARY_DIR})

# 生成可执行文件 demo
ADD_EXECUTABLE(demo main.c)

# 链接动态库 libhello.so
TARGET_LINK_LIBRARIES(demo hello)
#TARGET_LINK_LIBRARIES(demo libhello.so)

# 链接静态库 libhello.a
#TARGET_LINK_LIBRARIES(demo libhello.a)

# 安装 demo
INSTALL(TARGETS demo
        RUNTIME DESTINATION bin)

