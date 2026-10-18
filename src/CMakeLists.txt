add_library(strata.map)
add_library(strata::map ALIAS strata.map)

target_compile_features(strata.map PUBLIC cxx_std_23)
set_target_properties(strata.map PROPERTIES VERIFY_INTERFACE_HEADER_SETS ON)

target_sources(strata.map
  PRIVATE
    map.cpp
  PUBLIC
    FILE_SET HEADERS
    BASE_DIRS .
    FILES
      map.h
)
