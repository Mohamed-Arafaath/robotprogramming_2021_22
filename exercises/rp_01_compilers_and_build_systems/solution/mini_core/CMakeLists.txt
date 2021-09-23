cmake_minimum_required(VERSION 2.8.3)
project(mini_core)

find_path(EIGEN3_INCLUDE_DIR signature_of_eigen3_matrix_library
  PATHS
  /usr/include/eigen3
  /usr/local/include/eigen3
)

# find Eigen3
find_package(Eigen3 REQUIRED)


# specify additional locations of header files
include_directories(
  ${EIGEN3_INCLUDE_DIR}
  ${PROJECT_SOURCE_DIR}/src
)

# add project source code
add_subdirectory(src)
add_subdirectory(executables)