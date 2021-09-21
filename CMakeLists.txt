cmake_minimum_required(VERSION 3.0)

list(APPEND CMAKE_MODULE_PATH
  "${CMAKE_CURRENT_SOURCE_DIR}/cmake"
  "${CMAKE_CURRENT_SOURCE_DIR}/cmake/modules"
)

set(LUAJIT_TOP_SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR})

project(luajit LANGUAGES C)
set(LUAJIT_VERSION_MAJOR "2")
set(LUAJIT_VERSION_MINOR "1")
set(LUAJIT_VERSION "${LUAJIT_VERSION_MAJOR}.${LUAJIT_VERSION_MINOR}")

set(can_use_assembler TRUE)
enable_language(ASM)

include (GNUInstallDirs)

add_subdirectory(src)
