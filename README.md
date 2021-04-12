![output image](https://qengineering.eu/images/SDcard16GB_tiny.jpg) Find this example on our [SD-image](https://github.com/Qengineering/RPi-image)
# TensorFlow_Lite_Face_Mask_RPi_64-bits
![output image]( https://qengineering.eu/images/Mask_2_RPi.jpg )<br/>
## TensorFlow Lite Face Mask detection running on a bare Raspberry Pi 4.
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
A fast C++ implementation of TensorFlow Lite Face Mask detector on a bare Raspberry Pi 4 with a 32 or 64-bit operating system. Ubuntu 18.04, or Ubuntu20.04 are also possible.<br/>
Once overclocked to 1900 MHz, your app runs at 8.3 FPS without any hardware accelerator.<br/><br/>
You could call this Face Mask detection ___2.0___.<br/>
The network used is a re-trained MobileNet V2 SSD. It has three classes: no maks, a mask, and wearing a mask incorrectly. Although the latter category is not very convincing, given the small size of training samples.<br/>
It's not the usual cascade of the two deep learning models, one face recognition and a second one that detects the masks.<br/>
This one model now recognizes not only the white masks, but also the black, colored and fancy masks.<br/> 
Although it can detect more faces/masks in the same scene, the best result is still one face in front of the camera.<br/>

------------

## Benchmark.
| Model | RPi 4 64os 1900 MHz | RPi 4 64os 1500 MHz |
|  :------------: |  :------------: | :-------------: |
| ssd_mobilenet_v2.tflite | 8.1 FPS | 7.5 FPS |
| ssd_mobilenet_v2_fpnlite.tflite | 6.3 FPS | 5.8 FPS |


Special made for a Raspberry Pi 4 see [Q-engineering deep learning examples](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html) <br/>

------------

## Dependencies.
To run the application, you have to:
- TensorFlow Lite framework installed. [Install TensorFlow Lite](https://qengineering.eu/install-tensorflow-2-lite-on-jetson-nano.html) <br/>
- OpenCV installed. [Install OpenCV 4.5](https://qengineering.eu/install-opencv-4.5-on-raspberry-64-os.html) <br/>
- Code::Blocks installed. (```$ sudo apt-get install codeblocks```)

------------

## Running the app.
To extract and run the network in Code::Blocks <br/>
$ mkdir *MyDir* <br/>
$ cd *MyDir* <br/>
$ wget https://github.com/Qengineering/TensorFlow_Lite_Face_Mask_RPi_64-bits/archive/refs/heads/main.zip <br/>
$ unzip -j master.zip <br/>
Remove master.zip, LICENSE and README.md as they are no longer needed. <br/> 
$ rm master.zip <br/>
$ rm README.md <br/> <br/>
Your *MyDir* folder must now look like this: <br/> 
Face_Mask_Video.mp4 <br/>
ssd_mobilenet_v2_fpnlite.tflite - more accurate<br/>
ssd_mobilenet_v2.tflite - somewhat faster <br/>
TestTensorFlow_Lite_Mask.cpb <br/>
FaceMask.cpp <br/>
Kapje_x.jpg - examples<br/>
 <br/>
Run TestTensorFlow_Lite.cpb with Code::Blocks.<br/>

------------

## WebCam.
If you want to use a camera please alter line 130 in main.cpp to<br/>
`cv::VideoCapture cap(0);                          //WebCam`<br/>
If you want to run a movie please alter line 130 in main.cpp to<br/>
`cv::VideoCapture cap("Face_Mask_Video.mp4");   //Movie`<br/>

------------

### Thanks.
https://www.kaggle.com/andrewmvd/face-mask-detection<br/>
https://github.com/tanhouren/Face_mask_detector<br/>

![output image]( https://qengineering.eu/images/Mask_5_RPi.jpg )<br/>
![output image]( https://qengineering.eu/images/Mask_1_RPi.jpg )<br/>
![output image]( https://qengineering.eu/images/Mask_49_RPi.jpg )
