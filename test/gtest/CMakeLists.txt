# Use a variable to point to the root of googlemock within
# the External directory.  This makes it easier to update
# to new releases as desired.
SET(GOOGLEMOCK_ROOT "${CMAKE_CURRENT_SOURCE_DIR}/gmock-1.7.0")

# Make the file lists.
SET(INCLUDE_FILES
	${GOOGLEMOCK_ROOT}/fused-src/gtest/gtest.h
    ${GOOGLEMOCK_ROOT}/fused-src/gmock/gmock.h
)

SET(SOURCE_FILES
    ${GOOGLEMOCK_ROOT}/fused-src/gmock-gtest-all.cc
)

# Add as a static library target.
ADD_LIBRARY(gmock STATIC
	${INCLUDE_FILES}
	${SOURCE_FILES}
)

SET(GMOCK_INCLUDE_DIRS ${GOOGLEMOCK_ROOT}/fused-src PARENT_SCOPE)