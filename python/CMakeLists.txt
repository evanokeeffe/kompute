
pybind11_add_module(kp src/main.cpp)

set_target_properties(kp PROPERTIES POSITION_INDEPENDENT_CODE TRUE)

include_directories(
        ${PROJECT_SOURCE_DIR}/include/)

target_link_libraries(
        kp PRIVATE
        kompute::kompute)

set_property(TARGET kp PROPERTY POSITION_INDEPENDENT_CODE ON)
