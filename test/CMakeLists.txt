cmake_minimum_required(VERSION 3.14)

project(plf_hive)

add_executable(plf_hive_test_suite 
	plf_hive_test_suite.cpp
	../plf_hive.h
)

set_target_properties(plf_hive_test_suite PROPERTIES 
	CXX_STANDARD "20"
	CXX_STANDARD_REQUIRED True
)

target_include_directories(plf_hive_test_suite PUBLIC   
	$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/..>
)

