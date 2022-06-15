cmake_minimum_required(VERSION 3.5)
project(husky_ur_description)

find_package(ament_cmake REQUIRED)
find_package(urdf REQUIRED)

install(DIRECTORY meshes urdf
  DESTINATION share/${PROJECT_NAME}
)
install(PROGRAMS
scripts/setup_husky_dual_ur3_e_envar
scripts/setup_husky_dual_ur3_envar
scripts/setup_husky_dual_ur5_e_envar
scripts/setup_husky_dual_ur5_envar
scripts/setup_husky_ur3_e_envar
scripts/setup_husky_ur3_envar
scripts/setup_husky_ur5_e_envar
scripts/setup_husky_ur5_envar
  DESTINATION lib/${PROJECT_NAME}
)

ament_export_dependencies(xacro)
ament_export_dependencies(urdf)
ament_package()
