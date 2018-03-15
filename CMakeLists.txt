cmake_minimum_required (VERSION 2.6)
project (Test)

#Version Number
set (Test_VMA 1)
set (Test_VMI 0)

#Header file
configure_file (
	"${PROJECT_SOURCE_DIR}/src/TutConf.h.in"
	"${PROJECT_BINARY_DIR}/src/TutConf.h"
	)

include_directories("${PROJECT_BINARY_DIR}")
include_directories("${PROJECT_BINARY_DIR}/src")
include_directories("${PROJECT_BINARY_DIR}/dep")
include_directories("${PROJECT_BINARY_DIR}/proj")

add_executable(Test proj/main.cc)
