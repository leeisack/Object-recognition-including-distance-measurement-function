# Object-recognition-including-distance-measurement-function
Object recognition including distance measurement function without using ROS
---------------------
### I create a hexahedron by recognizing an object for embedded PC and outputting the minimum and maximum distance between the camera and the object. As a result, we are creating an object recognition system for stable autonomous driving of drones.

### Since the embedded PC installed on the drone is of low specification, the program should be made as light as possible, and for this reason, the gui has been removed as a result. But in the making process, I used the gui to check. I have committed both the version with and without the gui.
----------------------------
## Installation guide

<Installation item>
The production purpose is for jetson-xavier, but the work was done on a different desktop, and for this desktop, I use two graphics cards of the gtx-1080.
  
  1. cuda driver 
  2. cuda
  3. cudnn
  4. zed sdk

---------------------------

## Output using gui
Object recognition supported by Stereo Lab is less accurate than Yolo and has fewer classes.
Object customization is possible through PyTorch or TensorFlow.
![Screenshot from 2021-05-11 14-30-32](https://user-images.githubusercontent.com/52061393/117764645-cfa4ed00-b267-11eb-88bd-aeb9d5c91fdf.png)
-----------------------
In the model provided by Stereo Lab, learning is focused on cars and people, so the recognition ability for these two items is excellent.
![Screenshot from 2021-05-11 14-28-59](https://user-images.githubusercontent.com/52061393/117764720-ea776180-b267-11eb-9945-962ebaded6ad.png)
------------------------
![Screenshot from 2021-05-11 14-36-42](https://user-images.githubusercontent.com/52061393/117764664-d6cbfb00-b267-11eb-84be-97bb153563a1.png)
-------------------
