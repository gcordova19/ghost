cmake_minimum_required(VERSION 2.8.3)

include_directories(${ROS_LIB_DIR})

generate_arduino_firmware(car_interface
  SRCS car_interface.cpp ${ROS_LIB_DIR}/time.cpp
  HDRS interrupt_pwm_signal.h
  HDRS PinChangeInt.h
  HDRS signal_map.h
  HDRS simple_moving_average.h
  BOARD nano328
  PORT /dev/ttyUSB0
)
