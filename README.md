# tensorflow_recognition
### Summer project for exchange student

###### Calibration Instruction

  ``` 
  rosrun camera_calibration cameracalibration.py --size 8x6 --square 0.108 image:=/usb_cam/image_raw camera:=/usb_cam 
  ```
  
  `usb_cam` will be replaced by the name of the camera, use `rostopic list` to varify (It will look like `/usb_cam/image_raw`)
  
 More detailed instruction is on [ros_wiki camera_calibration_tutorial](http://wiki.ros.org/camera_calibration/Tutorials/MonocularCalibration)  (In our case we are using **monocular camera**)
  
image_recognition.py
--------------------------------

* publish: /result (std_msgs/String)
* subscribe: /image (sensor_msgs/Image)

How to try

```bash
$ roscore
$ rosrun cv_camera cv_camera_node
$ source ~/tensorflow/bin/activate
$ python image_recognition.py image:=/cv_camera/image_raw
$ rostopic echo /result
```
Refer: [OTL/rostensorflow](https://github.com/OTL/rostensorflow/edit/master) <br>
To make CPU only machine works better, see [this](https://stackoverflow.com/questions/47068709/your-cpu-supports-instructions-that-this-tensorflow-binary-was-not-compiled-to-u) discusstion
