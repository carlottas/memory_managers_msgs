cmake_minimum_required(VERSION 2.8.3)
project(memory_managers_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  message_runtime
  roscpp
  sensor_msgs
  sit_msgs
  std_msgs
)

## Generate messages in the 'msg' folder
 add_message_files(
   DIRECTORY msg 
   FILES

 )

## Generate services in the 'srv' folder
# add_service_files(
#   FILES
#   Service1.srv
#   Service2.srv
# )

## Generate actions in the 'action' folder
# add_action_files(
#   FILES
#   Action1.action
#   Action2.action
# )

## Generate added messages and services with any dependencies listed here
 generate_messages(
   DEPENDENCIES
    sensor_msgs   sit_msgs   std_msgs
 )



catkin_package(
  CATKIN_DEPENDS message_generation message_runtime  roscpp sensor_msgs sit_msgs std_msgs

)


include_directories(
  ${catkin_INCLUDE_DIRS}
)






