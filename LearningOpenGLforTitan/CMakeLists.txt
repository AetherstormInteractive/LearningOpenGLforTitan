# CMakeList.txt : CMake project for LearningOpenGLforTitan, include source and define
# project specific logic here.
#

# Add source to this project's executable.

add_executable (LearningOpenGLforTitan "Chapter 1.cpp" "Chapter 1.h" "${CMAKE_SOURCE_DIR}/3rdparty/glad/src/glad.c")

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET LearningOpenGLforTitan PROPERTY CXX_STANDARD 20)
endif()

target_link_libraries(LearningOpenGLforTitan SDL2 SDL2main glm)

include_directories("${CMAKE_SOURCE_DIR}/3rdparty/glad/include")

# TODO: Add tests and install targets if needed.
