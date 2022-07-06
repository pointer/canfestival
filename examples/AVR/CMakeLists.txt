ADD_SUBDIRECTORY(Slave)


# FILE (GLOB SRC_FILES Test*.cxx Test*.cpp Test*.c)

# Here, SRC_FILES will contain all the file i requested with their full path.
# Is their a clean way to retrieve a list containing only the relative path
# of those files ?

# I can do that :
# FOREACH(myfile ${SRC_FILES})
# 	FILE(RELATIVE_PATH TMP ${CMAKE_CURRENT_SOURCE_DIR} ${myfile})
# 	# here TMP contain the relative path
# ENDFOREACH(myfile ${SRC_FILES})