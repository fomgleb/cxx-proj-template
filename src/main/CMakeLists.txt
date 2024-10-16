set(APP_NAME "main_app")
set(SOURCE_DIR "src")
set(PRIVATE_HEADER_DIR "src")
set(PUBLIC_HEADER_DIR "include")
file(GLOB_RECURSE SOURCES "${SOURCE_DIR}/*.cpp")

add_executable(${APP_NAME} ${SOURCES})

target_include_directories(
  ${APP_NAME}
  PUBLIC ${PUBLIC_HEADER_DIR}
  PRIVATE ${PRIVATE_HEADER_DIR})

target_link_libraries(${APP_NAME} PRIVATE project_warnings hello_world_lib)
