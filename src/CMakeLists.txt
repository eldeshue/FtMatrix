cmake_minimum_required(VERSION 3.23)

# 현재 디렉토리에 있는 모든 파일을 SRC_FILES 변수에 추가한다.
file(GLOB_RECURSE SRC_FILES CONFIGURE_DEPENDS
  ${CMAKE_CURRENT_SOURCE_DIR}/*.cc
)

# add_executable(실행파일이름 ${SRC_FILES})
# target_link_libraries(실행파일이름 PUBLIC 링크할라이브러리이름)

# add_library(라이브러리이름 ${SRC_FILES})
# target_link_libraries(라이브러리이름 PUBLIC 링크할라이브러리이름)
