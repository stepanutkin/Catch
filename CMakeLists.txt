#����������� ������ cmake �� ������� ����� ��������
cmake_minimum_required(VERSION 3.27.2)
#�������� ������� � ��� ��������� �������� � ������
project(test_catch2sql)
#���� ���������� ��� ����������� Catch2 �� vcpkg:
find_package(Catch2 CONFIG REQUIRED)
#��������� ����������� ���� � ������ ������� test_catch2sql
add_executable(${PROJECT_NAME} main.cpp)
#������� ���������� Catch2
target_link_libraries(${PROJECT_NAME} PRIVATE Catch2::Catch2 Catch2::Catch2WithMain)