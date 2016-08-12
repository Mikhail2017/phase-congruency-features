CMAKE_MINIMUM_REQUIRED(VERSION 3.6)

PROJECT("utils")

# -------------------------------------------------------------------------------------------------

SET(LIBRARY_NAME
    "bip_utils")
SET(LIBRARY_SOURCE_FILES
    "assert.cpp"
    "math_functions.cpp")

ADD_LIBRARY(
    ${LIBRARY_NAME}
    ${LIBRARY_SOURCE_FILES})
TARGET_LINK_LIBRARIES(
    ${LIBRARY_NAME}
    m
    fftw3f
    fftw3f_threads)
TARGET_INCLUDE_DIRECTORIES(
    ${LIBRARY_NAME}
    PUBLIC ${CMAKE_SOURCE_DIR}/${PROJECT_NAME})
SET_PROPERTY(
    TARGET ${LIBRARY_NAME}
    PROPERTY CXX_STANDARD 11)
SET_PROPERTY(
    TARGET ${LIBRARY_NAME}
    PROPERTY CXX_STANDARD_REQUIRED ON)