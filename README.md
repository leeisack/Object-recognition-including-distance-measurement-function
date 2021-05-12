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
  4. jetpack4.5 : I installed jetpack4.5. jetpack is an OS for jetson xavier, nano, etc, so it provides cuda, driver, cudnn. (Cuda 10.2 cudnn8.0 for 4.5) and some libraries like opencv are automatically installed.
  5. zed sdk: zed sdk is very important to use zed camera if you want depth, point cloud, etc. However, the installable version differs depending on your cuda, cudnn, os version, so please refer to the homepage for this part.
https://www.stereolabs.com/developers/release/
![117932428-51197f80-b33b-11eb-9c80-8a97c826a031](https://user-images.githubusercontent.com/52061393/117938177-b5d7d880-b341-11eb-8f53-3da4aa804d7b.png)
 </br>
After installing the sdk, if you move to this place from the terminal, ZED_Diagnostic is executed.

![117932387-4101a000-b33b-11eb-9a42-d1fe8125333e](https://user-images.githubusercontent.com/52061393/117938332-df90ff80-b341-11eb-85c9-ee0f7a05b912.png)

Then, you can see such a screen. It determines whether the CUDA version is correct for the installed sdk version, the camera is connected, or the graphics card is recognized.

  6. python
  7. pip
  8. python library : When you have finished installing python and pip, type'python -m pip install cython numpy opencv-python pyopengl' in the terminal.
  9. confirmation : There is a file that zed itself checks for the necessary Python library and downloads it if it does not. Do this.
![117932446-57a7f700-b33b-11eb-92f2-fee4f912187c](https://user-images.githubusercontent.com/52061393/117938595-2da60300-b342-11eb-87c1-3cf1e284db92.png)



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
![117932525-6bebf400-b33b-11eb-8c88-b0520a53408f](https://user-images.githubusercontent.com/52061393/117939524-1b789480-b343-11eb-8b2f-ede7e79b2948.png)
--------------------

