cmake_minimum_required(VERSION 3.25)

project(Lines98 VERSION 1.0.0)

find_package(dxsdk-d3dx REQUIRED)

add_executable(Lines98 WIN32
    Lines.cpp
    random.h
    resource.h
    resrc1.h
    Lines.rc
    Lines.ICO
    res/0.png
    res/appear_1.png
    res/appear_2.png
    res/appear_3.png
    res/appear_4.png
    res/explode_1.png
    res/explode_2.png
    res/explode_3.png
    res/explode_4.png
    res/explode_5.png
    res/explode_6.png
    res/explode_7.png
    res/explode_8.png
    res/explode_9.png
    res/jump_1.png
    res/jump_2.png
    res/jump_3.png
    res/jump_4.png
    res/jump_5.png
    res/jump_6.png
    res/numbers.png
    res/points.png
    res/prestand.png
    res/stand.png
    SMALL.ICO
)
if(MSVC)
    target_compile_definitions(Lines98 PRIVATE _CRT_SECURE_NO_WARNINGS)
endif()
target_link_libraries(Lines98 PRIVATE d3d9 Microsoft::D3DX9)
