# Hardcoded path to rtabmap-res_tool
SET(RTABMAP_RES_TOOL "/opt/sysroots/aarch64-linux-gnu/root/.hunter/_Base/1292e4d/da0fb0e/17ec023/Build/rtbmap/Build/rtbmap-Release-prefix/src/rtbmap-Release-build/bin/rtabmap-res_tool")

# Check if the variable is not defined already
IF(NOT RTABMAP_RES_TOOL)
    # Your existing logic for finding the tool if it's not defined
ENDIF()

# Output a message indicating the path being used
MESSAGE(STATUS "Using res_tool at ${RTABMAP_RES_TOOL}")

# Set the target properties
ADD_EXECUTABLE(res_tool IMPORTED GLOBAL)
SET_TARGET_PROPERTIES(res_tool PROPERTIES IMPORTED_LOCATION "${RTABMAP_RES_TOOL}")
