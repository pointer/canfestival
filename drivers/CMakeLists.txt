FILE(GLOB DRIVERS RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} *.cpp*)
MESSAGE("DBG DRIVERS=${DRIVERS}")
ADD_SUBDIRECTORY(AT91)
ADD_SUBDIRECTORY(AVR)
ADD_SUBDIRECTORY(can_anagate_linux)
ADD_SUBDIRECTORY(can_anagate_win32)
ADD_SUBDIRECTORY(can_can4linux)
ADD_SUBDIRECTORY(can_copcican_comedi)
ADD_SUBDIRECTORY(can_copcican_linux)
ADD_SUBDIRECTORY(can_copcican_win32)
ADD_SUBDIRECTORY(can_ixxat_win32)
ADD_SUBDIRECTORY(can_kvaser)
ADD_SUBDIRECTORY(can_lincan)
ADD_SUBDIRECTORY(can_multi_peeakwin32)
ADD_SUBDIRECTORY(can_socket)
ADD_SUBDIRECTORY(can_tcp_win32)
ADD_SUBDIRECTORY(timers_kernel_xeno)
ADD_SUBDIRECTORY(unix)
ADD_SUBDIRECTORY(win32)
ADD_SUBDIRECTORY(timers_xeno)
ADD_SUBDIRECTORY(timers_rtai)
ADD_SUBDIRECTORY(timers_kernel)
ADD_SUBDIRECTORY(timers_unix)
ADD_SUBDIRECTORY(can_virtual_kernel)
ADD_SUBDIRECTORY(can_serial)
ADD_SUBDIRECTORY(can_peak_win32)
ADD_SUBDIRECTORY(can_uvccm_win32)
ADD_SUBDIRECTORY(can_virtual)
ADD_SUBDIRECTORY(can_vscom)
ADD_SUBDIRECTORY(hcs12)

# FILE (GLOB SRC_FILES Test*.cxx Test*.cpp Test*.c)

# Here, SRC_FILES will contain all the file i requested with their full path.
# Is their a clean way to retrieve a list containing only the relative path
# of those files ?

# I can do that :
# FOREACH(myfile ${SRC_FILES})
# 	FILE(RELATIVE_PATH TMP ${CMAKE_CURRENT_SOURCE_DIR} ${myfile})
# 	# here TMP contain the relative path
# ENDFOREACH(myfile ${SRC_FILES})