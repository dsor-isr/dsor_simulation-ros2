cmake_minimum_required(VERSION 3.8)
project(simulation_bringup)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
# uncomment the following section in order to fill in
# further dependencies manually.
# find_package(<dependency> REQUIRED)

# Install launch and config_personal files.
install(DIRECTORY launch DESTINATION share/${PROJECT_NAME}/)
install(DIRECTORY config_personal DESTINATION share/${PROJECT_NAME}/)

ament_package()