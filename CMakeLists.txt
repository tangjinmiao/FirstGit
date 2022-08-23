cmake_minimum_required(VERSION 3.17 FATAL_ERROR)

project(Step1)

set(MITK_SUPERBUILD_DIR "/home/dolores/Workspace/MITK-superbuild")
set(QT_DIR "/home/dolores")

set(CMAKE_PREFIX_PATH
        "${MITK_SUPERBUILD_DIR}/MITK-build"
        "${MITK_SUPERBUILD_DIR}/ep/src/VTK/CMake/"
        "${QT_DIR}/Qt5.12.9/5.12.9/gcc_64/lib/cmake/Qt5"
        )

find_package(MITK CONFIG REQUIRED)
find_package(OpenMP REQUIRED)

add_executable(${PROJECT_NAME} Step1.cpp)

target_link_libraries(${PROJECT_NAME}
        MitkCore
        MitkQtWidgetsExt
        )

//token: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
