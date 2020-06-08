cmake_minimum_required ( версия 3.10)
проект (форматирование)

набор (CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library (formatter STATIC formatter_lib/форматер.СРР)
include_directories(formatter_lib)

add_library(formatter_ex STATIC formatter_ex_lib/formatter_ex.СРР)
include_directories(formatter_ex_lib formatter_lib)
target_link_libraries (форматтер_ex formatter)

add_executable(hello_world hello_world_application/hello_world.СРР)
target_link_libraries(hello_world formatter formatter_ex)

add_library (solver_lib статический solver_lib/решатель.СРР)
include_directories(solver_lib)

add_executable (solver solver_application / equation.СРР)
target_link_libraries(solver formatter formatter_ex solver_lib)
