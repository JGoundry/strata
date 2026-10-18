cmake_minimum_required(VERSION 3.25)
project(
    strata
    VERSION 0.1.0
    DESCRIPTION "C++ library of reusable data structures and algorithms"
    HOMEPAGE_URL "https://github.com/jgoundry/strata"
    LANGUAGES CXX
)

include(CTest)

add_subdirectory(src)

if(BUILD_TESTING)
    add_subdirectory(src/test)
endif()

add_subdirectory(docs)