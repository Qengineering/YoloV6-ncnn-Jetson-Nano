# YoloV6 Jetson Nano
![output image]( https://qengineering.eu/images/ParkingYoloV7.jpg )
## YoloV6 with the ncnn framework. <br/>
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
Paper: https://tech.meituan.com/2022/06/23/yolov6-a-fast-and-accurate-target-detection-framework-is-opening-source.html<br/><br/>
Special made for a Jetson Nano see [Q-engineering deep learning examples](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html)

------------

## Benchmark.
| Model  | size | objects | mAP | Jetson Nano 1479 MHz | RPi 4 64-OS 1950 MHz |
| ------------- | :-----:  | :-----:  | :-----:  | :-------------:  | :-------------: |
| [NanoDet](https://github.com/Qengineering/NanoDet-ncnn-Jetson-Nano) | 320x320 | 80 | 20.6  |  26.2 FPS | 13.0 FPS |
| [NanoDet Plus](https://github.com/Qengineering/NanoDetPlus-ncnn-Jetson-Nano) | 416x416 | 80 | 30.4  |  18.5 FPS | 5.0 FPS |
| [YoloFastestV2](https://github.com/Qengineering/YoloFastestV2-ncnn-Jetson-Nano) | 352x352  | 80 | 24.1 |  38.4 FPS | 18.8 FPS |
| [YoloV2](https://github.com/Qengineering/YoloV2-ncnn-Jetson-Nano) | 416x416  | 20 | 19.2 |  10.1 FPS | 3.0 FPS |
| [YoloV3](https://github.com/Qengineering/YoloV3-ncnn-Jetson-Nano) | 352x352 tiny | 20 | 16.6 | 17.7 FPS | 4.4 FPS |
| [YoloV4](https://github.com/Qengineering/YoloV4-ncnn-Jetson-Nano) | 416x416 tiny | 80 | 21.7 | 16.1 FPS | 3.4 FPS |
| [YoloV4](https://github.com/Qengineering/YoloV4-ncnn-Jetson-Nano) | 608x608 full | 80 | 45.3 | 1.3 FPS | 0.2 FPS |
| [YoloV5](https://github.com/Qengineering/YoloV5-ncnn-Jetson-Nano) | 640x640 small| 80 | 22.5 | 5.0 FPS | 1.6 FPS |
| [YoloV6](https://github.com/Qengineering/YoloV6-ncnn-Jetson-Nano) | 412x412 nano | 80 | 35.0 | **22.75 FPS** | 5.85 FPS |
| [YoloV6](https://github.com/Qengineering/YoloV6-ncnn-Jetson-Nano) | 640x640 nano | 80 | 35.0 | **10.5 FPS** | 2.7 FPS |
| [YoloV7](https://github.com/Qengineering/YoloV7-ncnn-Jetson-Nano) | 640x640 tiny| 80 | 38.7 | 8.5 FPS | 2.1 FPS |
| [YoloX](https://github.com/Qengineering/YoloX-ncnn-Jetson-Nano) | 416x416 nano | 80 | 25.8 | 22.6 FPS | 7.0 FPS |
| [YoloX](https://github.com/Qengineering/YoloX-ncnn-Jetson-Nano) | 416x416 tiny | 80 | 32.8 | 11.35 FPS | 2.8 FPS |
| [YoloX](https://github.com/Qengineering/YoloX-ncnn-Jetson-Nano) | 640x640 small | 80 | 40.5 | 3.65 FPS | 0.9 FPS |

------------

## Dependencies.
To run the application, you have to:
- The Tencent ncnn framework installed. [Install ncnn](https://qengineering.eu/install-ncnn-on-jetson-nano.html) <br/>
- Code::Blocks installed. (```$ sudo apt-get install codeblocks```)

------------

## Installing the app.
To extract and run the network in Code::Blocks <br/>
$ mkdir *MyDir* <br/>
$ cd *MyDir* <br/>
$ wget https://github.com/Qengineering/YoloV6-ncnn-Jetson-Nano/archive/refs/heads/main.zip <br/>
$ unzip -j master.zip <br/>
Remove master.zip, LICENSE and README.md as they are no longer needed. <br/> 
$ rm master.zip <br/>
$ rm LICENSE <br/>
$ rm README.md <br/> <br/>
Your *MyDir* folder must now look like this: <br/> 
parking.jpg <br/>
busstop.jpg <br/>
YoloV6.cpb <br/>
yolo.cpp <br/>
yolo.h <br/>
yoloV6main.cpp <br/>
yolov6-tiny.bin <br/>
yolov6-tiny.param <br/>

------------

## Running the app.
To run the application load the project file YoloV6.cbp in Code::Blocks. More info or<br/> 
if you want to connect a camera to the app, follow the instructions at [Hands-On](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html#HandsOn).<br/><br/>

------------

### Dynamic sizes.
YoloV6 can handle different input resolutions without changing the deep learning model.<br/>
On line 28 of `yolov6main.cpp` you can change the `target_size` (default 640).<br/>
Decreasing the size to say 412 will speed up the inference time. On the other hand, the resizing makes the image less detailed; the model will no longer detect all objects.<br/><br/>

Many thanks to [nihui](https://github.com/nihui/) and [FeiGeChuanShu](https://github.com/FeiGeChuanShu)<br/><br/>
![output image]( https://qengineering.eu/images/BusstopYoloV7.jpg )

------------

[![paypal](https://qengineering.eu/images/TipJarSmall4.png)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CPZTM5BB3FCYL) 


