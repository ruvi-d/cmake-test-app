cmake_minimum_required(VERSION 3.18)
project (HELLO-TEST)

include(GNUInstallDirs)

add_executable (helloDemo demo.cxx)

if(DEFINED ENV{HELLOLIB_ROOT_PATH})
    target_include_directories(helloDemo PRIVATE  "$ENV{HELLOLIB_ROOT_PATH}/include")
    target_link_directories(helloDemo PRIVATE "$ENV{HELLOLIB_ROOT_PATH}/lib/")
endif()

target_link_libraries (helloDemo LINK_PUBLIC HelloLib)

install(TARGETS helloDemo)
