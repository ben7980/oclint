CMAKE_MINIMUM_REQUIRED(VERSION 3.20)
PROJECT(OCLINT_METRICS)

SET(CMAKE_MODULE_PATH
    ${CMAKE_MODULE_PATH}
    "${CMAKE_CURRENT_SOURCE_DIR}/../oclint-core/cmake"
    )

INCLUDE(OCLintConfig)

INCLUDE_DIRECTORIES(${OCLINT_METRICS_SOURCE_DIR}/include)

ADD_SUBDIRECTORY(lib)

IF(TEST_BUILD)
    INCLUDE_DIRECTORIES(${OCLINT_METRICS_SOURCE_DIR}/test/headers)
    ADD_SUBDIRECTORY(test)
ENDIF()
