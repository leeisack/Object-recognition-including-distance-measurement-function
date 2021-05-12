# Object-recognition-including-distance-measurement-function
Object recognition including distance measurement function without using ROS
---------------------
### It recognizes an object for an embedded PC, calculates the volume of the object by using the distance value between the camera and the object, and visually outputs it in a hexahedron form. As a result, we are building an object recognition system for stable autonomous driving of drones.

### Since the embedded PC installed on the drone is of low specification, the program should be made as light as possible, and for this reason, the gui has been removed as a result. But in the making process, I used the gui to check. I have committed both the version with and without the gui.
----------------------------
# Writing...
## Installation guide

<Installation item>
The production purpose is for jetson-xavier, but the work was done on a different desktop, and for this desktop, I use two graphics cards of the gtx-1080.
  
  1. cuda driver : Most of them recommend the driver version according to the performance of the graphics card, but if you install the latest driver because it is too high-performance, the cuda version may be set to a higher version. Please pay attention to the driver version and install it.
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
![Screenshot from 2021-05-12 15-02-35](https://user-images.githubusercontent.com/52061393/117932387-4101a000-b33b-11eb-9a42-d1fe8125333e.png)

![Screenshot from 2021-05-12 15-02-59](https://user-images.githubusercontent.com/52061393/117932428-51197f80-b33b-11eb-9c80-8a97c826a031.png)

![Screenshot from 2021-05-12 15-05-01](https://user-images.githubusercontent.com/52061393/117932446-57a7f700-b33b-11eb-92f2-fee4f912187c.png)


![Screenshot from 2021-05-12 15-05-49](https://user-images.githubusercontent.com/52061393/117932450-5a0a5100-b33b-11eb-9259-2ab8b275ca52.png)

![Screenshot from 2021-05-12 15-37-08](https://user-images.githubusercontent.com/52061393/117932470-5e366e80-b33b-11eb-84bc-88855bb2e9f3.png)

![Screenshot from 2021-05-12 15-42-47](https://user-images.githubusercontent.com/52061393/117932490-64c4e600-b33b-11eb-825d-a06737e949fe.png)

![Screenshot from 2021-05-12 15-46-27](https://user-images.githubusercontent.com/52061393/117932525-6bebf400-b33b-11eb-8c88-b0520a53408f.png)
