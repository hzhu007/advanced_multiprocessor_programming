include_directories(
    ${PHEET_INCLUDE_DIR}
)

add_library(cuckooset SHARED
    atomicmarkablereference.cpp
    cuckoolock.cpp
    cuckooset.cpp
    hash.cpp
    probeset.cpp
)
target_link_libraries(cuckooset ${CMAKE_THREAD_LIBS_INIT} ${HWLOC_LIBRARIES})

add_library(stdset SHARED stdset.cpp)
target_link_libraries(stdset ${CMAKE_THREAD_LIBS_INIT} ${HWLOC_LIBRARIES})
