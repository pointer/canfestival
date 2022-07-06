cmake_minimum_required(VERSION 3.0)
project(Can_AT91)
ADD_SUBDIRECTORY(ADD_SUBDIRECTORY(master))
set(CMAKE_CXX_STANDARD 20)
find_program(CMAKE_CXX_COMPILER NAMES $ENV{CXX} g++ PATHS ENV PATH NO_DEFAULT_PATH)
add_executable(${PROJECT_NAME} AT91)

target_include_directories(${PROJECT_NAME}
        PUBLIC
            master
)

target_link_libraries(${PROJECT_NAME}
        PUBLIC
            TCPAsioNetworking
)


# FILE (GLOB SRC_FILES Test*.cxx Test*.cpp Test*.c)

# Here, SRC_FILES will contain all the file i requested with their full path.
# Is their a clean way to retrieve a list containing only the relative path
# of those files ?

# I can do that :
# FOREACH(myfile ${SRC_FILES})
# 	FILE(RELATIVE_PATH TMP ${CMAKE_CURRENT_SOURCE_DIR} ${myfile})
# 	# here TMP contain the relative path
# ENDFOREACH(myfile ${SRC_FILES})