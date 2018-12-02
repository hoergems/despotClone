cmake_minimum_required(VERSION 2.8.3)

include_directories(
  src
)

add_executable("${PROJECT_NAME}4DOF"
  src/base/base_rock_sample.cpp
  src/rock_sample/rock_sample.cpp
  src/rock_sample/main.cpp
)
target_link_libraries("${PROJECT_NAME}4DOF"
  "${PROJECT_NAME}"
)

install(TARGETS "${PROJECT_NAME}4DOF"
  RUNTIME DESTINATION "${BINARY_INSTALL_PATH}"
)
