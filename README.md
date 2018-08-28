# tensorflow_recognition
### Summer project for exchange student

###### Calibration Instruction

  ``` 
  rosrun camera_calibration cameracalibration.py --size 8x6 --square 0.108 image:=/usb_cam/image_raw camera:=/usb_cam 
  ```
  
  `usb_cam` will be replaced by the name of the camera, use `rostopic list` to varify (It will look like `/usb_cam/image_raw`)
  
 More detailed instruction is on [ros_wiki camera_calibration_tutorial](http://wiki.ros.org/camera_calibration/Tutorials/MonocularCalibration)
 
 In our case we are using **monocular camera**
  
