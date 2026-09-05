cmake_minimum_required(VERSION 3.10..4.4) 

# In a normal application you would do:
# FIND_LIBRARY(MultiNest)
# INCLUDE_DIRECTORIES(${MultiNest_INCLUDE_PATH})

FILE(GLOB SOURCE *.cc)
add_executable(eggboxC++ ${SOURCE})
target_link_libraries(eggboxC++ ${MultiNest_LIBRARIES})

# Set install directory
INSTALL(TARGETS eggboxC++ DESTINATION bin)
