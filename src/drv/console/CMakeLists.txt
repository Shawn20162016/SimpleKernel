
# This file is a part of Simple-XX/SimpleKernel (https://github.com/Simple-XX/SimpleKernel).
#
# CMakeLists.txt for Simple-XX/SimpleKernel.

PROJECT(console C ASM)

aux_source_directory(${console_SOURCE_DIR}/. console_src)
add_library(${PROJECT_NAME} OBJECT ${console_src})

target_include_libc_header_files(${PROJECT_NAME})
target_include_drv_header_files(${PROJECT_NAME})
target_include_arch_header_files(${PROJECT_NAME})
target_include_common_header_files(${PROJECT_NAME})
