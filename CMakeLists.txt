cmake_minimum_required(VERSION 3.10) # should be 3.19.3

# set the project name and version
project(HyperbolicParaboloid VERSION 1.0)

# configure a header file to pass the version number
# to the source code
configure_file(TutorialConfig.h.in TutorialConfig.h)

# add the executable
add_executable(HyperbolicParaboloid tutorial.cxx)

# add the binary tree to the search path for include files
# so that we will find TutorialConfig.h
target_include_directories(HyperbolicParaboloid PUBLIC
                           "${PROJECT_BINARY_DIR}"
                           )