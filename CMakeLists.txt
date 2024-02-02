#минимальная версия cmake на котором будет работать
cmake_minimum_required(VERSION 3.27.2)
#название проекта и как следствие солюшена в студии
project(test_catch2sql)
#ищем библиотеку для подключения Catch2 из vcpkg:
find_package(Catch2 CONFIG REQUIRED)
#добавляем запускаемый файл с именем проекта test_catch2sql
add_executable(${PROJECT_NAME} main.cpp)
#линкуем библиотеки Catch2
target_link_libraries(${PROJECT_NAME} PRIVATE Catch2::Catch2 Catch2::Catch2WithMain)