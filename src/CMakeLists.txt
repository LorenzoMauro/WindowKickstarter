# Create an executable target from main.cpp
add_executable(Window main.cpp)

# Link glfw3 library to the executable target
target_link_libraries(Window PRIVATE glfw OpenGL::GL)
