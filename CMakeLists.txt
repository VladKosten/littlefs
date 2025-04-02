add_library(LittleFs STATIC lfs_util.c
                            lfs.c)

target_include_directories(LittleFs PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

# Enable definitions for the library
target_compile_definitions(LittleFs PUBLIC LFS_DEFINES=${LFS_DEFINES_FILE})

target_link_libraries(LittleFs PUBLIC LittleFsConfig)