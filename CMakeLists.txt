cmake_minimum_required(VERSION 3.16)
project(port)


message(STATUS "port/CMakeLists.txt")


if(${INCLUDE_AUDIO})

    add_subdirectory(base/id3lib)

endif()



if(${INCLUDE_UNAC})

    add_subdirectory(base/unac)

endif()


if(${USE_PORT_FREEIMAGE})


	add_subdirectory(imaging/port_jpeg)
	add_subdirectory(imaging/port_openexr)
	add_subdirectory(imaging/port_png)
	add_subdirectory(imaging/port_tiff4)
	add_subdirectory(imaging/port_jxr)
	add_subdirectory(imaging/port_openjpeg)
	add_subdirectory(imaging/port_rawlite)
	add_subdirectory(imaging/port_webp)

	add_subdirectory(imaging/port_freeimage)

endif()


if(${INCLUDE_REDSHIFT})

    add_subdirectory(user-generation1/redshift)

endif()
