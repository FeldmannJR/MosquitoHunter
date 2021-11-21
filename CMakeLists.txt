include(FindPkgConfig)
cmake_minimum_required(VERSION 3.20)
project(MosquitoHunter)

find_package(PkgConfig REQUIRED)
pkg_check_modules(ALLEGRO REQUIRED allegro-5 allegro_font-5)

add_executable(MosquitoHunter main.cpp)


target_link_libraries(MosquitoHunter ${ALLEGRO_LIBRARIES})
target_include_directories(MosquitoHunter PUBLIC ${ALLEGRO_INCLUDE_DIRS})
target_compile_options(MosquitoHunter PUBLIC ${ALLEGRO_CFLAGS_OTHER})

set(CMAKE_CXX_STANDARD 20)

