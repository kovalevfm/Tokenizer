find_package(Boost COMPONENTS program_options)

include_directories(
  ${Boost_INCLUDE_DIRS}
  )

add_executable(tokenize
  tokenize.cc
  )
target_link_libraries(tokenize
  ${PROJECT_NAME}
  ${Boost_LIBRARIES}
  )

add_executable(detokenize
  detokenize.cc
  )
target_link_libraries(detokenize
  ${PROJECT_NAME}
  ${Boost_LIBRARIES}
  )

install(
  TARGETS tokenize detokenize
  DESTINATION bin/
  )
