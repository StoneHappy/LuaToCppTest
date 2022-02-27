cmake_minimum_required(VERSION 3.16)
project(myproject LANGUAGES CXX)


# 添加应用                                    
add_executable(${PROJECT_NAME}
    main.cpp
)


target_include_directories(${PROJECT_NAME} PUBLIC
    # ${VENDOR_DIR}/LuaBridge/Source
)   

target_link_libraries(${PROJECT_NAME} PUBLIC
                LuaBridge
                lualib
)

add_custom_command(
    TARGET ${PROJECT_NAME} POST_BUILD
    COMMAND ${CMAKE_COMMAND} -E copy ${CMAKE_CURRENT_SOURCE_DIR}/script.lua $<TARGET_FILE_DIR:${PROJECT_NAME}>)
