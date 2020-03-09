file(GLOB HEADERS "../include/IAudioServer/*.h")
source_group("Header Files\\Audio Server" FILES ${HEADERS})

file(GLOB SOURCES "./*.c")
list(APPEND SOURCES ${HEADERS_IAS})

add_library(IAudioServer ${SOURCES})
target_include_directories(IAudioServer PUBLIC $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}/include>)
