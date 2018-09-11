file(GLOB hdrs "*.h*")
file(GLOB srcs "*.cpp")

add_library(${MyLib1} STATIC ${srcs} ${hdrs})


