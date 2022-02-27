cmake_minimum_required(VERSION 3.16)
project(mylua)

########################## lua ##################################
# add_executable(lua
#                 ${CMAKE_SOURCE_DIR}/lua/onelua.c
# )

# target_include_directories(lua PUBLIC
#                             ${CMAKE_SOURCE_DIR}/lua/
# )

# target_compile_options (lua
#   PUBLIC -DMAKE_LUA
# )


######################## lualib ########################################
add_library(lualib STATIC
                lua/onelua.c
)

target_include_directories(lualib PUBLIC
               lua/
)

target_compile_options (lualib
  PUBLIC -DMAKE_LIB
)
