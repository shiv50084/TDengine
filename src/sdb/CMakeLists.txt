CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

PROJECT(TDengine)

IF (TD_LINUX)
  AUX_SOURCE_DIRECTORY(src SRC)
  INCLUDE_DIRECTORIES(${TD_ROOT_DIR}/src/inc ${TD_OS_DIR}/inc inc)
  ADD_LIBRARY(sdb ${SRC})
  TARGET_LINK_LIBRARIES(sdb trpc)
ENDIF ()