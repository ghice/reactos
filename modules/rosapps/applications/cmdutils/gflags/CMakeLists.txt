
add_executable(gflags gflags.c gflags.rc)
set_module_type(gflags win32cui UNICODE)
add_importlibs(gflags advapi32 user32 msvcrt kernel32)

if(MSVC)
    add_importlibs(gflags ntdll)
endif()

add_cd_file(TARGET gflags DESTINATION reactos/bin FOR all)
