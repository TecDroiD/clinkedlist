cmake_minimum_required(VERSION 3.0.0)
set(PROJECTNAME clinkedlist)

project(${PROJECTNAME})

# add all headers
include_directories(include)

# add all sources
file(GLOB SOURCES "src/*.c")

# when project is a library
add_library(${PROJECTNAME} STATIC ${SOURCES})

# whenn project is an executable
# add_executable(${PROJECTNAME} ${SOURCES})
# target_link_libraries(${PROJECTNAME} ${PROJECT_LINK_LIBS})

# install whatever you built
install(TARGETS ${PROJECTNAME} DESTINATION /usr/local/lib)

