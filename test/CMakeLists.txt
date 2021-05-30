# 指定cmake最低编译版本
CMAKE_MINIMUM_REQUIRED(VERSION 3.14)
# 指定工程的名称
PROJECT(gctest)
set(CMAKE_CXX_STANDARD 11)
#指定头文件目录位置
INCLUDE_DIRECTORIES(../)
# INCLUDE_DIRECTORIES(/usr/local/Cellar/protobuf/3.9.2/include)
#添加共享库搜索路径
# LINK_DIRECTORIES(/usr/local/Cellar/protobuf/3.9.2/lib)
#GTEST
# INCLUDE_DIRECTORIES(/usr/local/include)
# LINK_DIRECTORIES(/usr/local/lib)


# AUX_SOURCE_DIRECTORY(../proto DIR_SRCS)
# AUX_SOURCE_DIRECTORY(../parser-manager DIR_SRCS)
# include(FetchContent)
# FetchContent_Declare(
#   googletest
#   URL https://github.com/google/googletest/archive/609281088cfefc76f9d0ce82e1ff6c30cc3591e5.zip
# )
# # For Windows: Prevent overriding the parent project's compiler/linker settings
# set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
# FetchContent_MakeAvailable(googletest)
AUX_SOURCE_DIRECTORY(../frame DIR_SRCS)
AUX_SOURCE_DIRECTORY(../database DIR_SRCS)
# AUX_SOURCE_DIRECTORY(../thirdlib DIR_SRCS)
AUX_SOURCE_DIRECTORY(../shm_manager DIR_SRCS)
AUX_SOURCE_DIRECTORY(../utils DIR_SRCS)

SET(SRC
${DIR_SRCS}
)

#生成可执行文件
# ADD_EXECUTABLE(${PROJECT_NAME} unittest.cpp ${SRC})
ADD_EXECUTABLE(${PROJECT_NAME} testcpp.cpp ${SRC})
#为hello添加共享库链接
# TARGET_LINK_LIBRARIES(${PROJECT_NAME} protobuf gtest)
# TARGET_LINK_LIBRARIES(${PROJECT_NAME} googletest)
TARGET_LINK_LIBRARIES(${PROJECT_NAME} )


