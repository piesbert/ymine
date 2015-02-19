CMAKE_MINIMUM_REQUIRED( VERSION 2.8.3 )

PROJECT( yMine )

# ###############################################
# Make VC happy and group all the binary outputs,
# also make sure GMock headers will compile in
# all targets.
IF( MSVC )
	SET(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/bin)
	SET(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/bin)
	SET(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/bin)

	ADD_DEFINITIONS(-D_VARIADIC_MAX=10)
ENDIF(MSVC)

ADD_SUBDIRECTORY(src)
ADD_SUBDIRECTORY(test)