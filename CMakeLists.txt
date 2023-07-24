cmake_minimum_required(VERSION 3.15 FATAL_ERROR)

project(
  TerrainRLSim
  VERSION 0.0.1
  DESCRIPTION "Terrain RL Simulation library"
  HOMEPAGE_URL "https://github.com/wpumacay/TerrainRLSim"
  LANGUAGES C CXX)

find_package(Eigen3 3.3 REQUIRED NO_MODULE)

add_library(TerrainRLUtil
  ${PROJECT_SOURCE_DIR}/util/ArgParser.cpp
  ${PROJECT_SOURCE_DIR}/util/BVHReader.cpp
  ${PROJECT_SOURCE_DIR}/util/FileUtil.cpp
  ${PROJECT_SOURCE_DIR}/util/IndexManager.cpp
  ${PROJECT_SOURCE_DIR}/util/JsonUtil.cpp
  ${PROJECT_SOURCE_DIR}/util/MathUtil.cpp
  ${PROJECT_SOURCE_DIR}/util/MotionDB.cpp
  ${PROJECT_SOURCE_DIR}/util/PerlinNoise.cpp
  ${PROJECT_SOURCE_DIR}/util/Rand.cpp
  ${PROJECT_SOURCE_DIR}/util/Trajectory.cpp
  ${PROJECT_SOURCE_DIR}/util/Util.cpp
)
target_include_directories(TerrainRLUtil PUBLIC ${PROJECT_SOURCE_DIR})
target_include_directories(TerrainRLUtil PUBLIC ${PROJECT_SOURCE_DIR}/util)
target_link_libraries(TerrainRLUtil PUBLIC Eigen3::Eigen)
