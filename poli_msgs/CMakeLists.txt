cmake_minimum_required(VERSION 2.8.3)
### Want to move the msgs here but the teensy gets very confused if you
### change the ns to face/LedEye.msg 
### So, hack: let's rename "face" to "poli_msgs" so that the teensy 
### still works.
### TODO: flash the teensy with new message definitions
### (rma 18 nov 2022)
project(poli_msgs)


find_package(catkin REQUIRED COMPONENTS
  message_generation
)

## Generate messages in the 'msg' folder
# add_message_files(
#   FILES
#   Message1.msg
#   Message2.msg
# )

## Generate services in the 'srv' folder
add_service_files(
  FILES
  LedEye.srv
  LedEar.srv
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
)

catkin_package(  
)

