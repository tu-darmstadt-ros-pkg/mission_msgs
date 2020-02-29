cmake_minimum_required(VERSION 2.8.3)
project(mission_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  message_runtime
  roscpp
  std_msgs
)

add_message_files(
  FILES
  Param.msg	
  Task.msg
  Mission.msg
)

add_service_files(
  FILES
  LoadMission.srv
  StopMission.srv
  InsertTask.srv			
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
 CATKIN_DEPENDS message_runtime std_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)


