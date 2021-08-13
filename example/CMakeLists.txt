cmake_minimum_required(VERSION 3.10)

project(ImageDetection)

find_package(OpenCV 4 REQUIRED)

include_directories(../src/
                    ${OpenCV4_INCLUE_DIR})

add_executable(detectImage detect-image.cpp ../src/facedetectcnn-data.cpp ../src/facedetectcnn-model.cpp ../src/facedetectcnn.cpp)
target_link_libraries(detectImage ${OpenCV_LIBRARIES})