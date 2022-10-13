cmake_minimum_required(VERSION 3.20)
project(myManet)

set(CMAKE_CXX_STANDARD 17)

set(NS3BUILDDIR /Users/ahmadyulianto/WSN-NS3/ns-allinone-3.36.1/ns-3.36.1/build)

link_directories(
        ${NS3BUILDDIR}
        ${NS3BUILDDIR}/lib
)

add_executable(${PROJECT_NAME} main.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC
        ${NS3BUILDDIR}
        ${NS3BUILDDIR}/include
        )

target_link_libraries(${PROJECT_NAME}
        ns3.36.1-core-default.dylib
        )
add_definitions(-DNS3_LOG_ENABLE)