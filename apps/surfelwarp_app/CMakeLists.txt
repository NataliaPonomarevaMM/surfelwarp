file(GLOB SURFELWARP_APP_SRC *.h *.hpp *.cpp *.cu)
cuda_add_executable(surfelwarp_app ${SURFELWARP_APP_SRC})
#if(MSVC)
#	set(CUDA_LIBRARY_DIR "${CUDA_TOOLKIT_ROOT_DIR}/lib/x64")
#	target_link_libraries(surfelwarp_app PUBLIC ${CUDA_LIBRARY_DIR}) #${Boost_LIBRARY_DIRS})
#endif()
target_link_libraries(surfelwarp_app common_lib)
target_link_libraries(surfelwarp_app math_lib)
target_link_libraries(surfelwarp_app imgproc_lib)
target_link_libraries(surfelwarp_app core_lib)
target_link_libraries(surfelwarp_app visualization_lib)
