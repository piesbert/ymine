ADD_SUBDIRECTORY(gtest)

# Add the gmock include directories.
INCLUDE_DIRECTORIES( ${GMOCK_INCLUDE_DIRS} )

ADD_EXECUTABLE(ymine_test
	unit/Main.cpp
)

TARGET_LINK_LIBRARIES(ymine_test
	gmock
	${CMAKE_THREAD_LIBS_INIT}
)