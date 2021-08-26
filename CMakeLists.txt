cmake_minimum_required(VERSION 3.0.0)
project(whycon_srvs)

find_package(catkin REQUIRED COMPONENTS
    message_generation
    geometry_msgs
    )

#######################################
## Declare ROS messages and services ##
#######################################

# Generate services in the 'srv' folder
add_service_files(
    FILES
    SelectMarker.srv
    SetCalibMethod.srv
    SetCalibPath.srv
    SetCoords.srv
    SetDrawing.srv
)

## Generate added messages and services with any dependencies listed here
generate_messages(
    DEPENDENCIES
    geometry_msgs
    )

###################################
## catkin specific configuration ##
###################################
## The catkin_package macro generates cmake config files for your package
catkin_package(
    CATKIN_DEPENDS message_runtime geometry_msgs
    )

