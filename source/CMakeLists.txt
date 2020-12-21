set(SOURCE_FILES
    animCurveUtils.cpp
    BufferPath.cpp
    CameraCache.cpp
    ContextUtils.cpp
    DrawUtils.cpp
    GlobalSettings.cpp
    KeyClipboard.cpp
    Keyframe.cpp
    MotionPath.cpp
    MotionPathCmd.cpp
    MotionPathDrawContext.cpp
    MotionPathEditContext.cpp
    MotionPathEditContextMenuWidget.cpp
    MotionPathEditContextMenuWidgetMoc.cpp
    MotionPathManager.cpp
    MotionPathOverride.cpp
    PluginMain.cpp
    Vp2DrawUtils.cpp
)
set(INCLUDE_DIR ${CMAKE_SOURCE_DIR}/include)
set(INCLUDE_FILES
    ${INCLUDE_DIR}/animCurveUtils.h
    ${INCLUDE_DIR}/BufferPath.h
    ${INCLUDE_DIR}/CameraCache.h
    ${INCLUDE_DIR}/ContextUtils.h
    ${INCLUDE_DIR}/DrawUtils.h
    ${INCLUDE_DIR}/GlobalSettings.h
    ${INCLUDE_DIR}/KeyClipboard.h
    ${INCLUDE_DIR}/Keyframe.h
    ${INCLUDE_DIR}/MotionPath.h
    ${INCLUDE_DIR}/MotionPathCmd.h
    ${INCLUDE_DIR}/MotionPathDrawContext.h
    ${INCLUDE_DIR}/MotionPathEditContext.h
    ${INCLUDE_DIR}/MotionPathEditContextMenuWidget.h
    ${INCLUDE_DIR}/MotionPathManager.h
    ${INCLUDE_DIR}/MotionPathOverride.h
    ${INCLUDE_DIR}/Vp2DrawUtils.h
)
# find_package(Maya REQUIRED)

# include_directories(${MAYA_INCLUDE_DIR})
# link_directories(${MAYA_LIBRARY_DIR})

add_library(tcMotionPath SHARED ${SOURCE_FILES} ${INCLUDE_FILES})
target_link_libraries(tcMotionPath 
    ${MAYA_LIBRARIES} 
    Qt5::Core
    Qt5::Widgets
)

# MAYA_PLUGIN(${PROJECT_NAME})
