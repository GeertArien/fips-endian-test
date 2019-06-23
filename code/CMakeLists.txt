# CPU endianness
include(TestBigEndian)
test_big_endian(HOST_BIG_ENDIAN)

if(HOST_BIG_ENDIAN)
    message(STATUS "BIG_ENDIAN")
else()
    message(STATUS "LITTLE_ENDIAN")
endif()

fips_begin_app(endian cmdline)
    fips_files(endian.cpp)
fips_end_app()
