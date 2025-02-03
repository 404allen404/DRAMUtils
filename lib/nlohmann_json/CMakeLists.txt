########################################
###          nlohmann_json           ###
########################################
FetchContent_Declare(nlohmann_json
    URL "https://github.com/nlohmann/json/releases/download/v3.11.2/include.zip"
    OVERRIDE_FIND_PACKAGE
)

FetchContent_MakeAvailable(nlohmann_json)

add_library(nlohmann_json INTERFACE)
target_include_directories(nlohmann_json INTERFACE ${nlohmann_json_SOURCE_DIR}/single_include)

add_library(nlohmann_json::nlohmann_json ALIAS nlohmann_json)