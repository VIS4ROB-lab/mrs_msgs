cmake_minimum_required(VERSION 3.0.2)
project(mrs_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  message_runtime
  roscpp
  rospy
  std_msgs
  sensor_msgs
  geometry_msgs
)

add_message_files(DIRECTORY msg FILES
  # BoolStamped.msg
  # ConstraintManagerDiagnostics.msg
  # ControlError.msg
  # ControllerDiagnostics.msg
  # ControllerStatus.msg
  # ControlManagerDiagnostics.msg
  # CustomTopic.msg
  # DynamicsConstraints.msg
  # EstimationDiagnostics.msg
  # EstimatorCorrection.msg
  # EstimatorDiagnostics.msg
  # EstimatorInput.msg
  # EstimatorOutput.msg
  # EulerAngles.msg
  # Float64ArrayStamped.msg
  # Float64.msg
  # Float64MultiArrayStamped.msg
  # Float64Stamped.msg
  # FuturePoint.msg
  # FutureTrajectory.msg
  # GainManagerDiagnostics.msg
  # GazeboSpawnerDiagnostics.msg
  # GimbalState.msg
  # GpsData.msg
  # GpsInfo.msg
  # GripperDiagnostics.msg
  # Histogram.msg
  # HwApiAccelerationHdgCmd.msg
  # HwApiAccelerationHdgRateCmd.msg
  # HwApiActuatorCmd.msg
  # HwApiAltitude.msg
  # HwApiAttitudeCmd.msg
  # HwApiAttitudeRateCmd.msg
  # HwApiCapabilities.msg
  # HwApiControlGroupCmd.msg
  # HwApiPositionCmd.msg
  # HwApiRcChannels.msg
  # HwApiStatus.msg
  # HwApiVelocityHdgCmd.msg
  # HwApiVelocityHdgRateCmd.msg
  # ImageLabeled.msg
  # ImageLabeledArray.msg
  # LandoffDiagnostics.msg
  # MpcPredictionFullState.msg
  # MpcTrackerDiagnostics.msg
  # NodeCpuLoad.msg
  # ObstacleSectors.msg
  # Path.msg
  # PathReference.msg
  # PathWithVelocity.msg
  # PoseWithCovarianceArrayStamped.msg
  # PoseWithCovarianceIdentified.msg
  # ProfilerUpdate.msg
  # RangeWithCovarianceArrayStamped.msg
  # RangeWithCovarianceIdentified.msg
  Reference.msg
  # ReferenceArray.msg
  # ReferenceStamped.msg
  # ReferenceWithVelocity.msg
  # RtkFixType.msg
  # RtkGps.msg
  # Se3Gains.msg
  # SpeedTrackerCommand.msg
  # Sphere.msg
  # StringStamped.msg
  # Track.msg
  # TrackArrayStamped.msg
  # TrackStamped.msg
  # TrackerCommand.msg
  # TrackerStatus.msg
  TrajectoryReference.msg
  # UavDiagnostics.msg
  # UavManagerDiagnostics.msg
  # UavState.msg
  # UavStatus.msg
  # UavStatusShort.msg
  # UInt16Stamped.msg
  # VelocityReference.msg
  # VelocityReferenceStamped.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
    std_msgs
    geometry_msgs
    sensor_msgs
)

catkin_package(
  CATKIN_DEPENDS
    message_runtime
)