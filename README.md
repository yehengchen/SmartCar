# Real-time-FaceRecognition & HeadPose Estimation

## SmartCar - face recognition (Driver / Passenger) 
This is completly based on deep learning nueral network and implented using Tensorflow framework. Here you will get how to implement fastly and you can find code at github and uses is demonstrated at YouTube.

### Installation Python Libraries:

- Tensorflow (1.10.0)
- Scipy (1.1.0)
- Scikit-learn (0.19.1)
- Opencv (3.4.4.19)

For ipmlementation and run this code follow [this BLOG link](http://www.aisangam.com/blog/real-time-face-recognition-using-facenet/). Implemention in video is shown [YouTube](https://www.youtube.com/watch?v=cAblAimZLgo).
<br>Download FaceNet Pre-trained models: 20170512-110547.pb - [[Google Drive]](https://drive.google.com/drive/folders/1_vMkaL0aDF2SacLegiVEiOC9n64AXm7M) / [[Baidu Drive]](https://pan.baidu.com/disk/home?errno=0&errmsg=Auth%20Login%20Sucess&&bduss=&ssnerror=0&traceid=#/all?vmode=list&path=%2FGithub%2Ffacenet)

Training using the VGGFace2 dataset - [[Link]](https://github.com/davidsandberg/facenet/wiki/Training-using-the-VGGFace2-dataset)
***

<img src="https://github.com/yehengchen/FaceNet-FaceRecognition/blob/master/output_video/output.gif" width="60%" height="60%">

## Getting Started:
### (make sure you have Pre-trained models .pb file)
  * Put your Pre-trained models __20170512-110547.pb__ file under __'./model/'__ folder.
  
  * [data_preprocess.py](https://github.com/chenyeheng/SmartCar/blob/master/data_preprocess.py) put img under __'./train_img'__ folder and run data_preprocess.py output preprocessed img to __'./pre_img'__ folder.
  
  * [train_classifier.py](https://github.com/chenyeheng/SmartCar/blob/master/train_classifier.py) training your own data under __'./pre_img'__ folder and output __classifier.pkl__ file to __'./classifier/'__ folder.
  
  * [identify_face_image.py](https://github.com/chenyeheng/SmartCar/blob/master/identify_face_image.py) face recognition on your own images(change 'input_image' path)
  
  * [identify_face_video.py](https://github.com/chenyeheng/SmartCar/blob/master/identify_face_video.py) face recognition on your own videos(change 'input_video' path)


***
## SmartCar - head pose estimation (Driver) 

<div align="center">
  <img src="https://i.imgur.com/K7jhHOg.png" width="306">   <img src="https://github.com/yehengchen/HeadPoseEstimation/blob/master/output/video/test.gif" width="240"><br><br>
</div>

**Hopenet** is an accurate and easy to use head pose estimation network. Models have been trained on the 300W-LP dataset and have been tested on real data with good qualitative performance.

For details about the method and quantitative results please check the [paper](https://arxiv.org/abs/1710.00925).

**new** [GoT trailer example video](https://youtu.be/OZdOrSLBQmI)

**new** [Conan-Cruise-Car example video](https://youtu.be/Bz6eF4Nl1O8)


To use please install [PyTorch](http://pytorch.org/) and [OpenCV](https://opencv.org/) (for video) - I believe that's all you need apart from usual libraries such as numpy. You need a GPU to run Hopenet (for now).
***

## Getting Started:
To test on a video using dlib face detections (DLIB_MODEL: mmod_human_face_detector.dat):
```bash
python3 code/test_on_video_dlib.py --snapshot PATH_OF_PRE-TRAINED-MODELS --face_model PATH_OF_DLIB_MODEL --video PATH_OF_VIDEO --output_string STRING_TO_APPEND_TO_OUTPUT --n_frames N_OF_FRAMES_TO_PROCESS --fps FPS_OF_SOURCE_VIDEO
```
To test on a video using your own face detections (we recommend using [dockerface](https://github.com/natanielruiz/dockerface), center of head will be smoother):
```bash
python3 code/test_on_video_dockerface.py --snapshot PATH_OF_SNAPSHOT --video PATH_OF_VIDEO --bboxes FACE_BOUNDING_BOX_ANNOTATIONS --output_string STRING_TO_APPEND_TO_OUTPUT --n_frames N_OF_FRAMES_TO_PROCESS --fps FPS_OF_SOURCE_VIDEO
```
Face bounding box annotations should be in Dockerface format (n_frame x_min y_min x_max y_max confidence).

### Pre-trained models:

[300W-LP, alpha 1](https://drive.google.com/open?id=1EJPu2sOAwrfuamTitTkw2xJ2ipmMsmD3)

[300W-LP, alpha 2](https://drive.google.com/open?id=16OZdRULgUpceMKZV6U9PNFiigfjezsCY)

[300W-LP, alpha 1, robust to image quality](https://drive.google.com/open?id=1m25PrSE7g9D2q2XJVMR6IA7RaCvWSzCR)

For more information on what alpha stands for please read the paper. First two models are for validating paper results, if used on real data we suggest using the last model as it is more robust to image quality and blur and gives good results on video.

Please keep in mind that testing instructions to reproduce the paper results will be added very soon.

This work is still in progress - we are obtaining better results and will also be updating this README with instructions. Please open an issue if you have an problem.

Some things that will be added:
* Test script for images
* Docker image
* Instructions for all scripts
* Better and better models
* Videos and example images!

If you find Hopenet useful in your research please consider citing:


## References:

FaceNet - ["FaceNet: A Unified Embedding for Face Recognition and Clustering"](https://arxiv.org/abs/1503.03832)<br>
Face alignment using MTCNN - ["Joint Face Detection and Alignment using Multi-task Cascaded Convolutional Networks"](https://kpzhang93.github.io/MTCNN_face_detection_alignment/index.html)
<br>@AI Sangam

For details about the method and quantitative results please check the [paper](https://arxiv.org/abs/1710.00925).
*Nataniel Ruiz*, *Eunji Chong*, *James M. Rehg*
Georgia Institute of Technology


