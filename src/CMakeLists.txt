# CMakeList.txt: 顶层 CMake 项目文件，在此处执行全局配置
# 并包含子项目。
#
cmake_minimum_required (VERSION 3.10)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)
if (MSVC)
    # 设置 C 语言编译 flags,  输入代码编码格式为 utf-8
    set(CMAKE_C_FLAGS /source-charset:utf-8)
endif()

# # 如果支持，请为 MSVC 编译器启用热重载。
# if (POLICY CMP0141)
#   cmake_policy(SET CMP0141 NEW)
#   set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<IF:$<AND:$<C_COMPILER_ID:MSVC>,$<CXX_COMPILER_ID:MSVC>>,$<$<CONFIG:Debug,RelWithDebInfo>:EditAndContinue>,$<$<CONFIG:Debug,RelWithDebInfo>:ProgramDatabase>>")
# endif()
project(IsophoteBasedReconstruction)


# 包含子项目。
add_subdirectory()
