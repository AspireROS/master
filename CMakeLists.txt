#第一版示例：
# # 这个是一个CMakeLists.txt文件的示例
# cmake_minimum_required(VERSION 3.10) # 指定CMake的最低版本要求

# project(MyProject # 定义项目名称
#     [version 1.0] # 定义项目版本
#     [description "This is a sample CMake project."] # 定义项目描述
#     [homepage "https://example.com/MyProject"] # 定义项目主页
#     [license "MIT"] # 定义项目许可证
#     [Languages C++] # 指定使用的编程语言
#     [author "John Doe <john.doe@example.com>"] # 定义项目作者
#     )

# add_executable(app main.cpp main.h) # 添加可执行文件及其源文件(app是可执行文件名，main.cpp和main.h是源文件)

# # cmake -B build -S .  # 生成构建文件的命令示例
# # cmake --build build  # 构建项目的命令示例

# 第二版示例：
# # 这个是一个CMakeLists.txt文件的示例
# cmake_minimum_required(VERSION 3.10) # 指定CMake的最低版本要求

# project(MyProject # 定义项目名称
#     [version 1.0] # 定义项目版本
#     [description "This is a sample CMake project."] # 定义项目描述
#     [homepage "https://example.com/MyProject"] # 定义项目主页
#     [license "MIT"] # 定义项目许可证
#     [Languages C++] # 指定使用的编程语言
#     [author "John Doe <john.doe@example.com>"] # 定义项目作者
#     )

# set(SRC main.cpp main.h) # 定义源文件列表
# set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin) # 设置可执行文件的输出路径
# set(CMAKE_CXX_STANDARD 11) # 设置C++标准为C++11

# add_executable(app ${SRC}) # 添加可执行文件及其源文件(app是可执行文件名，main.cpp和main.h是源文件)

# # cmake -B build -S .  # 生成构建文件的命令示例
# # cmake --build build  # 构建项目的命令示例

# # 第三版示例：
# # 这个是一个CMakeLists.txt文件的示例
# cmake_minimum_required(VERSION 3.10) # 指定CMake的最低版本要求

# project(MyProject # 定义项目名称
#     [version 1.0] # 定义项目版本
#     [description "This is a sample CMake project."] # 定义项目描述
#     [homepage "https://example.com/MyProject"] # 定义项目主页
#     [license "MIT"] # 定义项目许可证
#     [Languages C++] # 指定使用的编程语言
#     [author "John Doe <john.doe@example.com>"] # 定义项目作者
#     )

# # set(SRC main.cpp main.h) # 定义源文件列表
# # aux_source_directory(${PROJECT_SOURCE_DIR} SRC) # 自动收集当前目录下(make目录)的所有源文件到SRC变量中
# file(GLOB SRC "${PROJECT_SOURCE_DIR}/*.cpp" "${PROJECT_SOURCE_DIR}/*.h") # 使用GLOB模式收集当前目录下(make目录)的所有.cpp和.h文件到SRC变量中
# # file(GLOB SRC "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp" "${CMAKE_CURRENT_SOURCE_DIR}/*.h") # 使用GLOB模式收集当前目录下(make目录)的所有.cpp和.h文件到SRC变量中
# set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin) # 设置可执行文件的输出路径
# set(CMAKE_CXX_STANDARD 11) # 设置C++标准为C++11

# add_executable(app ${SRC}) # 添加可执行文件及其源文件(app是可执行文件名，main.cpp和main.h是源文件)

# # cmake -B build -S .  # 生成构建文件的命令示例
# # cmake --build build  # 构建项目的命令示例

# # 第四版示例：
# # 这个是一个CMakeLists.txt文件的示例
# cmake_minimum_required(VERSION 3.10) # 指定CMake的最低版本要求

# project(MyProject # 定义项目名称
#     [version 1.0] # 定义项目版本
#     [description "This is a sample CMake project."] # 定义项目描述
#     [homepage "https://example.com/MyProject"] # 定义项目主页
#     [license "MIT"] # 定义项目许可证
#     [Languages C++] # 指定使用的编程语言
#     [author "John Doe <john.doe@example.com>"] # 定义项目作者
#     )

# # set(SRC main.cpp main.h) # 定义源文件列表
# # aux_source_directory(${PROJECT_SOURCE_DIR} SRC) # 自动收集当前目录下(make目录)的所有源文件到SRC变量中
# file(GLOB SRC "${PROJECT_SOURCE_DIR}/src/*.cpp" "${PROJECT_SOURCE_DIR}/src/*.h") # 使用GLOB模式收集src目录下(make目录同级src)的所有.cpp和.h文件到SRC变量中
# # file(GLOB SRC "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp" "${CMAKE_CURRENT_SOURCE_DIR}/src/*.h") # 使用GLOB模式收集当前目录下(make目录同级src)的所有.cpp和.h文件到SRC变量中
# set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin) # 设置可执行文件的输出路径
# include_directories(${PROJECT_SOURCE_DIR}/include) # 添加头文件搜索路径(include目录同级make)
# set(CMAKE_CXX_STANDARD 11) # 设置C++标准为C++11

# add_executable(app ${SRC}) # 添加可执行文件及其源文件(app是可执行文件名，main.cpp和main.h是源文件)

# # cmake -B build -S .  # 生成构建文件的命令示例
# # cmake --build build  # 构建项目的命令示例

# # 第五版示例：动态链接库和静态链接库
# # 这个是一个CMakeLists.txt文件的示例
# cmake_minimum_required(VERSION 3.10) # 指定CMake的最低版本要求

# project(MyProject # 定义项目名称
#     [version 1.0] # 定义项目版本
#     [description "This is a sample CMake project."] # 定义项目描述
#     [homepage "https://example.com/MyProject"] # 定义项目主页
#     [license "MIT"] # 定义项目许可证
#     [Languages C++] # 指定使用的编程语言
#     [author "John Doe <john.doe@example.com>"] # 定义项目作者
#     )

# # set(SRC main.cpp main.h) # 定义源文件列表
# # aux_source_directory(${PROJECT_SOURCE_DIR} SRC) # 自动收集当前目录下(make目录)的所有源文件到SRC变量中
# file(GLOB SRC "${PROJECT_SOURCE_DIR}/src/*.cpp" "${PROJECT_SOURCE_DIR}/src/*.h") # 使用GLOB模式收集src目录下(make目录同级src)的所有.cpp和.h文件到SRC变量中
# # file(GLOB SRC "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp" "${CMAKE_CURRENT_SOURCE_DIR}/src/*.h") # 使用GLOB模式收集当前目录下(make目录同级src)的所有.cpp和.h文件到SRC变量中
# # set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin) # 设置可执行文件的输出路径
# include_directories(${PROJECT_SOURCE_DIR}/include) # 添加头文件搜索路径(include目录同级make)
# set(CMAKE_CXX_STANDARD 11) # 设置C++标准为C++11

# set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR}/lib) # 设置库文件的输出路径
# add_library(MyLibrary SHARED ${SRC}) # 创建动态链接库MyLibrary.so 有执行权限
# # add_library(MyLibrary STATIC ${SRC}) # 创建静态链接库MyLibrary.a 无执行权限

# # add_executable(app ${SRC}) # 添加可执行文件及其源文件(app是可执行文件名，main.cpp和main.h是源文件)

# # cmake -B build -S .  # 生成构建文件的命令示例
# # cmake --build build  # 构建项目的命令示例

# # 第六版示例：动态链接库和静态链接库的链接
# # 这个是一个CMakeLists.txt文件的示例
# cmake_minimum_required(VERSION 3.10) # 指定CMake的最低版本要求

# project(MyProject # 定义项目名称
#     [version 1.0] # 定义项目版本
#     [description "This is a sample CMake project."] # 定义项目描述
#     [homepage "https://example.com/MyProject"] # 定义项目主页
#     [license "MIT"] # 定义项目许可证
#     [Languages C++] # 指定使用的编程语言
#     [author "John Doe <john.doe@example.com>"] # 定义项目作者
#     )

# # set(SRC main.cpp main.h) # 定义源文件列表
# # aux_source_directory(${PROJECT_SOURCE_DIR} SRC) # 自动收集当前目录下(make目录)的所有源文件到SRC变量中
# file(GLOB SRC "${PROJECT_SOURCE_DIR}/src/*.cpp" "${PROJECT_SOURCE_DIR}/src/*.h") # 使用GLOB模式收集src目录下(make目录同级src)的所有.cpp和.h文件到SRC变量中
# # file(GLOB SRC "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp" "${CMAKE_CURRENT_SOURCE_DIR}/src/*.h") # 使用GLOB模式收集当前目录下(make目录同级src)的所有.cpp和.h文件到SRC变量中
# # set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin) # 设置可执行文件的输出路径
# include_directories(${PROJECT_SOURCE_DIR}/include) # 添加头文件搜索路径(include目录同级make)
# set(CMAKE_CXX_STANDARD 11) # 设置C++标准为C++11

# # set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR}/lib) # 设置库文件的输出路径

# link_libraries(calc) # 指定链接的库文件(calc是库文件名，不带前缀lib和后缀.so或.a)
# link_directories(${CMAKE_BINARY_DIR}/lib) # 指定链接库文件的搜索路径
# message("")
# message(STATUS "")
# message(WARNING "----------------------------------------")
# message(STATUS "Library output path: ${CMAKE_BINARY_DIR}/lib")
# message(FATAL_ERROR "Just to show library output path") # 用于调试，显示库文件输出路径后终止配置过程

# add_library(MyLibrary SHARED ${SRC}) # 创建动态链接库MyLibrary.so 有执行权限
# # add_library(MyLibrary STATIC ${SRC}) # 创建静态链接库MyLibrary.a 无执行权限

# add_executable(app ${SRC}) # 添加可执行文件及其源文件(app是可执行文件名，main.cpp和main.h是源文件)
# # target_link_libraries(app MyLibrary) # 指定可执行文件app链接MyLibrary动态库 

# list(APPEND temp "xxx1" "xxx2" ${SRC}) # 示例：向列表temp追加元素
# message(${temp})

# list(REMOVE_ITEM SRC ${PROJECT_SOURCE_DIR}/src/main.hpp) # 示例：从列表SRC移除元素main.h

# message(${SRC})

# # cmake -B build -S .  # 生成构建文件的命令示例
# # cmake --build build  # 构建项目的命令示例

# # 第七版示例：动态链接库和静态链接库的链接
# # 这个是一个CMakeLists.txt文件的示例
# cmake_minimum_required(VERSION 3.10) # 指定CMake的最低版本要求

# project(MyProject # 定义项目名称
#     [version 1.0] # 定义项目版本
#     [description "This is a sample CMake project."] # 定义项目描述
#     [homepage "https://example.com/MyProject"] # 定义项目主页
#     [license "MIT"] # 定义项目许可证
#     [Languages C++] # 指定使用的编程语言
#     [author "John Doe <john.doe@example.com>"] # 定义项目作者
#     )
# set(SRC main.cpp main.h) # 定义源文件列表
# add_definitions(-DDEBUG) # 添加预处理宏定义-DDEBUG 代码中可以使用#ifdef DEBUG来判断是否定义了DEBUG宏  终端编译时也可以添加-DDEBUG参数
# add_executable(app ${SRC}) # 添加可执行文件及其源文件(app是可执行文件名，main.cpp和main.h是源文件)
# # cmake -B build -S .  # 生成构建文件的命令示例
# # cmake --build build  # 构建项目的命令示例

# 第八版示例：CMake的嵌套
# 这个是顶层CMakeLists.txt文件的示例
cmake_minimum_required(VERSION 3.10) # 指定CMake的最低版本要求

project(MyProject # 定义项目名称
    [version 1.0] # 定义项目版本
    [description "This is a sample CMake project."] # 定义项目描述
    [homepage "https://example.com/MyProject"] # 定义项目主页
    [license "MIT"] # 定义项目许可证
    [Languages C++] # 指定使用的编程语言
    [author "John Doe <john.doe@example.com>"] # 定义项目作者
    )
# 定义变量
# 静态库生成路径
set(LIBRARYPATH ${CMAKE_BINARY_DIR}/lib)
# 可执行文件生成路径
set(EXECUTABLEPATH ${CMAKE_BINARY_DIR}/bin)
# 头文件搜索路径
set(HEADERPATH ${PROJECT_SOURCE_DIR}/include)
# 库文件搜索路径
set(CALCLIB calc)
set(SORTLIB sort)
# 可执行程序的名字
set(EXECUTABLE_NAME1 app1)
set(EXECUTABLE_NAME2 app2)

# 设置库文件输出路径
# 添加子目录(subdir目录同级make)
add_subdirectory(calc)
add_subdirectory(sort)
add_subdirectory(text1)
add_subdirectory(text2)

# 这个是子CMakeLists.txt文件生成静态库的示例
cmake_minimum_required(VERSION 3.10) # 指定CMake的最低版本要求
project(CalcLibrary) # 定义项目名称
file(./ SRC) # 使用GLOB模式收集当前目录下的所有.cpp和.h文件到SRC变量中
include(${HEADERPATH}) # 添加头文件搜索路径
set(LIBRARY_OUTPUT_PATH ${LIBRARYPATH}) # 设置库文件的输出路径
add_library(${CALCLIB} STATIC ${SRC}) # 创建静态链接库calc.a 无执行权限

# 这个是子CMakeLists.txt文件生成静态库的示例
cmake_minimum_required(VERSION 3.10) # 指定CMake的最低版本要求
project(sort) # 定义项目名称
file(./ SRC) # 使用GLOB模式收集当前目录下的所有.cpp和.h文件到SRC变量中
include(${HEADERPATH}) # 添加头文件搜索路径
set(LIBRARY_OUTPUT_PATH ${LIBRARYPATH}) # 设置库文件的输出路径
add_library(${SORTLIB} STATIC ${SRC}) # 创建静态链接库sort.a 无执行权限

# 这个是子CMakeLists.txt文件生成可执行文件app1的示例
cmake_minimum_required(VERSION 3.10) # 指定CMake的最低
project(text1) # 定义项目名称
file(./ SRC) # 使用GLOB模式收集当前目录下的所有.cpp和.h文件到SRC变量中
include(${HEADERPATH}) # 添加头文件搜索路径
set(EXECUTABLE_OUTPUT_PATH ${EXECUTABLEPATH}) # 设置可执行文件的输出路径
link_directories(${LIBRARYPATH}) # 指定链接库文件的搜索路径
link_libraries(${CALCLIB}) # 指定链接的库文件(calc和sort是库文件名，不带前缀lib和后缀.so或.a)
set(EXECUTABLE_OUTPUT_PATH ${EXECUTABLEPATH}) # 设置可执行文件的输出路径
add_executable(${EXECUTABLE_NAME1} ${SRC}) # 添加可执行文件及其源文件
# target_link_libraries(${EXECUTABLE_NAME1} ${CALCLIB} ${SORTLIB}) # 指定可执行文件链接的库文件

# 这个是子CMakeLists.txt文件生成可执行文件app1的示例
cmake_minimum_required(VERSION 3.10) # 指定CMake的最低
project(text2) # 定义项目名称
file(./ SRC) # 使用GLOB模式收集当前目录下的所有.cpp和.h文件到SRC变量中
include(${HEADERPATH}) # 添加头文件搜索路径
set(EXECUTABLE_OUTPUT_PATH ${EXECUTABLEPATH}) # 设置可执行文件的输出路径
link_directories(${LIBRARYPATH}) # 指定链接库文件的搜索路径
link_libraries( ${SORTLIB}) # 指定链接的库文件(calc和sort是库文件名，不带前缀lib和后缀.so或.a)
set(EXECUTABLE_OUTPUT_PATH ${EXECUTABLEPATH}) # 设置可执行文件的输出路径
add_executable(${EXECUTABLE_NAME2} ${SRC}) # 添加可执行文件及其源文件
# target_link_libraries(${EXECUTABLE_NAME2} ${CALCLIB} ${SORTLIB}) # 指定可执行文件链接的库文件
