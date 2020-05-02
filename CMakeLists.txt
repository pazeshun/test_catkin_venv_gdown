cmake_minimum_required(VERSION 3.5.1)
project(test_catkin_venv_gdown)

find_package(catkin REQUIRED COMPONENTS catkin_virtualenv)

catkin_package()

catkin_generate_virtualenv(
  EXTRA_PIP_ARGS
    --force-reinstall
)

install(FILES requirements.txt
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
