set(SOURCE_FILES
    "animCurveUtils.cpp"
    "../include/animCurveUtils.h"
    "BufferPath.cpp"
    "../include/BufferPath.h"
    "CameraCache.cpp"
    "../include/CameraCache.h"
    "ContextUtils.cpp"
    "../include/ContextUtils.h"
    "DrawUtils.cpp"
    "../include/DrawUtils.h"
    "GlobalSettings.cpp"
    "../include/GlobalSettings.h"
    "KeyClipboard.cpp"
    "../include/KeyClipboard.h"
    "Keyframe.cpp"
    "../include/Keyframe.h"
    "MotionPath.cpp"
    "../include/MotionPath.h"
    "MotionPathCmd.cpp"
    "../include/MotionPathCmd.h"
    "MotionPathDrawContext.cpp"
    "../include/MotionPathDrawContext.h"
    "MotionPathEditContext.cpp"
    "../include/MotionPathEditContext.h"
    "MotionPathEditContextMenuWidget.cpp"
    "../include/MotionPathEditContextMenuWidget.h"
    "MotionPathEditContextMenuWidgetMoc.cpp"
    "MotionPathManager.cpp"
    "../include/MotionPathManager.h"
    "MotionPathOverride.cpp"
    "../include/MotionPathOverride.h"
    "PluginMain.cpp"
    "Vp2DrawUtils.cpp"
    "../include/Vp2DrawUtils.h"
)

find_package(Maya REQUIRED)
find_package(Qt5 REQUIRED)

include_directories(${MAYA_INCLUDE_DIR})
link_directories(${MAYA_LIBRARY_DIR})

include_directories(${QT_INCLUDES})
link_directories(${QT_LIBRARIES})

add_library(${PROJECT_NAME} SHARED ${SOURCE_FILES})
target_link_libraries(${PROJECT_NAME} ${MAYA_LIBRARIES} ${QT_LIBRARIES})

MAYA_PLUGIN(${PROJECT_NAME})
