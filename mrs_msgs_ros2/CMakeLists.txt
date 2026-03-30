cmake_minimum_required(VERSION 3.5)
project(mrs_msgs)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)
find_package(sensor_msgs REQUIRED)
find_package(geometry_msgs REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
    # msg/BoolStamped.msg
    # msg/ConstraintManagerDiagnostics.msg
    # msg/ControlError.msg
    # msg/ControllerDiagnostics.msg
    # msg/ControllerStatus.msg
    # msg/ControlManagerDiagnostics.msg
    # msg/CustomTopic.msg
    # msg/DynamicsConstraints.msg
    # msg/EstimationDiagnostics.msg
    # msg/EstimatorCorrection.msg
    # msg/EstimatorDiagnostics.msg
    # msg/EstimatorInput.msg
    # msg/EstimatorOutput.msg
    # msg/EulerAngles.msg
    # msg/Float64.msg
    # msg/Float64ArrayStamped.msg
    # msg/Float64MultiArrayStamped.msg
    # msg/Float64Stamped.msg
    # msg/FuturePoint.msg
    # msg/FutureTrajectory.msg
    # msg/GainManagerDiagnostics.msg
    # msg/GazeboSpawnerDiagnostics.msg
    # msg/GimbalState.msg
    # msg/GpsData.msg
    # msg/GpsInfo.msg
    # msg/GripperDiagnostics.msg
    # msg/Histogram.msg
    # msg/HwApiAccelerationHdgCmd.msg
    # msg/HwApiAccelerationHdgRateCmd.msg
    # msg/HwApiActuatorCmd.msg
    # msg/HwApiAltitude.msg
    # msg/HwApiAttitudeCmd.msg
    # msg/HwApiAttitudeRateCmd.msg
    # msg/HwApiCapabilities.msg
    # msg/HwApiControlGroupCmd.msg
    # msg/HwApiPositionCmd.msg
    # msg/HwApiRcChannels.msg
    # msg/HwApiStatus.msg
    # msg/HwApiVelocityHdgCmd.msg
    # msg/HwApiVelocityHdgRateCmd.msg
    # msg/ImageLabeled.msg
    # msg/ImageLabeledArray.msg
    # msg/LandoffDiagnostics.msg
    # msg/MpcPredictionFullState.msg
    # msg/MpcTrackerDiagnostics.msg
    # msg/NodeCpuLoad.msg
    # msg/ObstacleSectors.msg
    # msg/Path.msg
    # msg/PathReference.msg
    # msg/PathWithVelocity.msg
    # msg/PoseWithCovarianceArrayStamped.msg
    # msg/PoseWithCovarianceIdentified.msg
    # msg/ProfilerUpdate.msg
    # msg/RangeWithCovarianceArrayStamped.msg
    # msg/RangeWithCovarianceIdentified.msg
    msg/Reference.msg
    # msg/ReferenceArray.msg
    # msg/ReferenceStamped.msg
    # msg/ReferenceWithVelocity.msg
    # msg/RtkFixType.msg
    # msg/RtkGps.msg
    # msg/Se3Gains.msg
    # msg/SpeedTrackerCommand.msg
    # msg/Sphere.msg
    # msg/StringStamped.msg
    # msg/Track.msg
    # msg/TrackArrayStamped.msg
    # msg/TrackStamped.msg
    # msg/TrackerCommand.msg
    # msg/TrackerStatus.msg
    msg/TrajectoryReference.msg
    # msg/UavDiagnostics.msg
    # msg/UavManagerDiagnostics.msg
    # msg/UavState.msg
    # msg/UavStatus.msg
    # msg/UavStatusShort.msg
    # msg/UInt16Stamped.msg
    # msg/VelocityReference.msg
    # msg/VelocityReferenceStamped.msg
    DEPENDENCIES geometry_msgs std_msgs sensor_msgs
  )

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  # the following line skips the linter which checks for copyrights
  # comment the line when a copyright and license is added to all source files
  set(ament_cmake_copyright_FOUND TRUE)
  # the following line skips cpplint (only works in a git repo)
  # comment the line when this package is in a git repo and when
  # a copyright and license is added to all source files
  set(ament_cmake_cpplint_FOUND TRUE)
  ament_lint_auto_find_test_dependencies()
endif()

ament_package()
