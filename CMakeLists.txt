cmake_minimum_required(VERSION 3.16)
project(port)


if(INCLUDE_AUDIO)

    add_subdirectory(base/id3lib)

endif()



if(INCLUDE_UNAC)

    add_subdirectory(base/unac)

endif()



if(INCLUDE_REDSHIFT)

    add_subdirectory(user-generation1/redshift)

endif()
