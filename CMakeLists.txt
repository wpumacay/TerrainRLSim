cmake_minimum_required(VERSION 3.15 FATAL_ERROR)

project(
  TerrainRLSim
  VERSION 0.0.1
  DESCRIPTION "Terrain RL Simulation library"
  HOMEPAGE_URL "https://github.com/wpumacay/TerrainRLSim"
  LANGUAGES C CXX)

add_library(TerrainRLUtil
  #### ${PROJECT_SOURCE_DIR}/util/ArgParser.cpp
  #### ${PROJECT_SOURCE_DIR}/util/BVHReader.cpp
  #### ${PROJECT_SOURCE_DIR}/util/FileUtil.cpp
  #### ${PROJECT_SOURCE_DIR}/util/IndexManager.cpp
  #### ${PROJECT_SOURCE_DIR}/util/JsonUtil.cpp
  #### ${PROJECT_SOURCE_DIR}/util/MathUtil.cpp
  #### ${PROJECT_SOURCE_DIR}/util/MotionDB.cpp
  #### ${PROJECT_SOURCE_DIR}/util/PerlinNoise.cpp
  ${PROJECT_SOURCE_DIR}/util/Rand.cpp
  #### ${PROJECT_SOURCE_DIR}/util/Trajectory.cpp
  ${PROJECT_SOURCE_DIR}/util/Util.cpp
  #### ${PROJECT_SOURCE_DIR}/util/json/json_reader.cpp
  #### ${PROJECT_SOURCE_DIR}/util/json/json_writer.cpp
)
target_include_directories(TerrainRLUtil PUBLIC ${PROJECT_SOURCE_DIR})
target_include_directories(TerrainRLUtil PUBLIC ${PROJECT_SOURCE_DIR}/util)
