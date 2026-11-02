
add_executable(OpenGL-Learning
    "OpenGL-Learning.cpp"
    "OpenGL-Learning.h"
    "../external/glad/src/glad.c"
)

target_compile_features(OpenGL-Learning PRIVATE cxx_std_20)

find_package(glfw3 CONFIG REQUIRED)
find_package(glm CONFIG REQUIRED)
find_package(Stb REQUIRED)

target_include_directories(OpenGL-Learning PRIVATE
    "../external/glad/include"
    ${Stb_INCLUDE_DIR}
)

target_link_libraries(OpenGL-Learning PRIVATE
    glfw
    glm::glm
)
