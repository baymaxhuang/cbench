cmake_minimum_required(VERSION 3.5)
project(cbench)

set(CMAKE_C_STANDARD 99)

set(SOURCE_FILES
        cbench.c
        cbench.h
        fakeswitch.c
        fakeswitch.h
        msgbuf.c
        msgbuf.h
        myargs.c
        myargs.h
        openflow.h config.h)
add_executable(cbench ${SOURCE_FILES})

target_link_libraries(cbench m)
install(TARGETS cbench DESTINATION bin)