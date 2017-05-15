cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

PROJECT(ProtoZMQMonitor)
enable_testing()

include(${CMAKE_SOURCE_DIR}/CMakeScripts/FindZMQ.cmake)
FindZMQ()

include(${CMAKE_SOURCE_DIR}/CMakeScripts/FindProtobuf.cmake)
FindProtobuf()

include(${CMAKE_SOURCE_DIR}/CMakeScripts/GeneratePythonProto.cmake)
GeneratePythonProto()

message(${PROTO_PY})
