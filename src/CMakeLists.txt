
cmake_minimum_required(VERSION 3.18.2)

project(JobCreator)

add_library(utils utils/input.c)
target_include_directories(utils PUBLIC include)

add_library(jobs jobs/job.c) 
target_include_directories(jobs PUBLIC include)

add_executable(jobcreator main.c) 
target_link_libraries(jobcreator utils jobs)