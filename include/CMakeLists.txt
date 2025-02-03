add_library(DRAMUtils INTERFACE) # ${SOURCE_FILES} ${HEADER_FILES})
target_include_directories(DRAMUtils INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/DRAMUtils")

target_link_libraries(DRAMUtils
    INTERFACE
        nlohmann_json::nlohmann_json
)

add_library(DRAMUtils::DRAMUtils ALIAS DRAMUtils)
add_library(DRAMSys::DRAMUtils ALIAS DRAMUtils)