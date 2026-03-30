cmake_minimum_required(VERSION 3.5)
project(mrs_msgs)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CATKIN_DEPENDENCIES
  cmake_modules
  geometry_msgs
  message_generation
  message_runtime
  roscpp
  sensor_msgs
  std_msgs
  )

find_package(catkin REQUIRED COMPONENTS
  ${CATKIN_DEPENDENCIES}
  )

# messages for ROBOT_DIAGNOSTICS
add_message_files(DIRECTORY msg/robot_diagnostics FILES
  UavDiagnostics.msg
  )

# messages for MPC_TRACKER
add_message_files(DIRECTORY msg/mpc_tracker FILES

  FuturePoint.msg
  FutureTrajectory.msg
  MpcPredictionFullState.msg
  MpcTrackerDiagnostics.msg
  )

# messages for GIMBAL
add_message_files(DIRECTORY msg/gimbal FILES

  GimbalState.msg
  )

# messages for GNSS
add_message_files(DIRECTORY msg/gnss FILES

  RtkFixType.msg
  RtkGps.msg
  GpsData.msg
  GpsInfo.msg
  )

# messages for LANDOFF_TRACKER
add_message_files(DIRECTORY msg/landoff_tracker FILES

  LandoffDiagnostics.msg
  )

# messages for GazeboSimulation
add_message_files(DIRECTORY msg/gazebo_simulation FILES

  GazeboSpawnerDiagnostics.msg
  )

# messages for the UAV_MANAGERS
add_message_files(DIRECTORY msg/uav_managers FILES

  ConstraintManagerDiagnostics.msg
  ControlError.msg
  ControllerDiagnostics.msg
  ControllerStatus.msg
  ControlManagerDiagnostics.msg
  DynamicsConstraints.msg
  EstimationDiagnostics.msg
  EstimatorCorrection.msg
  EstimatorDiagnostics.msg
  EstimatorInput.msg
  EstimatorOutput.msg
  EulerAngles.msg
  GainManagerDiagnostics.msg
  PathReference.msg
  ReferenceArray.msg
  Reference.msg
  ReferenceStamped.msg
  TrackerCommand.msg
  TrackerStatus.msg
  TrajectoryReference.msg
  UavManagerDiagnostics.msg
  UavState.msg
  VelocityReference.msg
  VelocityReferenceStamped.msg
  )

# messages for the UAV_STATUS
add_message_files(DIRECTORY msg/uav_status FILES

  CustomTopic.msg
  NodeCpuLoad.msg
  UavStatus.msg
  UavStatusShort.msg
  )

# messages for the SE3_CONTROLLER
add_message_files(DIRECTORY msg/se3_controller FILES

  Se3Gains.msg
  )

# messages for the TRAJECTORY_GENERATION
add_message_files(DIRECTORY msg/trajectory_generation FILES

  Path.msg
  PathWithVelocity.msg
  ReferenceWithVelocity.msg
  )

# messages for the PROFILER
add_message_files(DIRECTORY msg/profiler FILES

  ProfilerUpdate.msg
  )

# messages for the MRS_BUMPER
add_message_files(DIRECTORY msg/bumper FILES

  Histogram.msg
  ObstacleSectors.msg
  )

# messages for SPEED_TRACKER
add_message_files(DIRECTORY msg/speed_tracker FILES

  SpeedTrackerCommand.msg
  )

# general messages
add_message_files(DIRECTORY msg/general FILES

  Float64ArrayStamped.msg
  Float64.msg
  Float64MultiArrayStamped.msg
  Float64Stamped.msg
  ImageLabeledArray.msg
  ImageLabeled.msg
  PoseWithCovarianceArrayStamped.msg
  PoseWithCovarianceIdentified.msg
  RangeWithCovarianceArrayStamped.msg
  RangeWithCovarianceIdentified.msg
  Sphere.msg
  StringStamped.msg
  TrackArrayStamped.msg
  Track.msg
  TrackStamped.msg
  )

# messages for stamped_msgs
add_message_files(DIRECTORY msg/stamped_msgs FILES

  UInt16Stamped.msg
  BoolStamped.msg
  )

add_message_files(DIRECTORY msg/hw_api FILES

  HwApiAccelerationHdgCmd.msg
  HwApiAccelerationHdgRateCmd.msg
  HwApiActuatorCmd.msg
  HwApiAltitude.msg
  HwApiAttitudeCmd.msg
  HwApiAttitudeRateCmd.msg
  HwApiCapabilities.msg
  HwApiControlGroupCmd.msg
  HwApiPositionCmd.msg
  HwApiRcChannels.msg
  HwApiStatus.msg
  HwApiVelocityHdgCmd.msg
  HwApiVelocityHdgRateCmd.msg
  )

## Generate added messages and services with any dependencies listed here
generate_messages(DEPENDENCIES

  std_msgs
  geometry_msgs
  sensor_msgs
  )

catkin_package(
  CATKIN_DEPENDS ${CATKIN_DEPENDENCIES}
  )