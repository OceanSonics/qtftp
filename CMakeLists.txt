# This file must only be used through an add_subdirectory() command in a top level CMakeLists.txt.

add_library(qtftp
    ${CMAKE_CURRENT_SOURCE_DIR}/src/qftp/qurlinfo.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/src/qftp/qftp.cpp)

# This Library's include paths (make public for users of this library)
target_include_directories(qtftp PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src/qftp/)

# Note: target_link_libraries adds the include paths.
target_link_libraries(qtftp Qt5::Core Qt5::Network)
