cmake_minimum_required(VERSION 3.8.3)
project(husky_dual_ur_moveit_config)

find_package(ament_cmake REQUIRED)

install(DIRECTORY config
  DESTINATION share/${PROJECT_NAME}
)
install(PROGRAMS
  scripts/customize_moveit.sh
  DESTINATION lib/${PROJECT_NAME}
)

ament_package()

