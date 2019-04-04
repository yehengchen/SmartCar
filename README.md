# Facenet: Real-time-FaceRecognition
## SmartCar - face recognition (Driver/Passenger) 
This is completly based on deep learning nueral network and implented using Tensorflow framework. Here you will get how to implement fastly and you can find code at github and uses is demonstrated at YouTube.

### Installation Python Libraries:

- Tensorflow (1.10.0)
- Scipy (1.1.0)
- Scikit-learn (0.19.1)
- Opencv (3.4.4.19)

For ipmlementation and run this code follow [this BLOG link](http://www.aisangam.com/blog/real-time-face-recognition-using-facenet/). Implemention in video is shown [HERE](https://youtu.be/dLrWDUPkpIg?list=PLCK5Mm9zwPkEhwu2OOw2CgO5ikoLdR36l).
<br>FaceNet Pre-trained models: [20170512-110547.pb](https://drive.google.com/open?id=11ZMNoK8r72ROQqe6j90bBVER-mN-WkVG）

## Getting Started:
### (make sure you have Pre-trained models .pb file)
  * put your Pre-trained models .pb file into './model/' file.
  
  * [data_preprocess.py](https://github.com/chenyeheng/SmartCar/blob/master/data_preprocess.py) put your face img into './train_img' and run data_preprocess.py preprocess your img output to './pre_img' file.
  
  * [train_main.py](https://github.com/chenyeheng/SmartCar/blob/master/train_main.py) training your own data './pre_img' and output classifier.pkl file to './class/' file.
  
  * [identify_face_image.py](https://github.com/chenyeheng/SmartCar/blob/master/identify_face_image.py) face recognition on your own imgs(change 'input_image' path)
  
  * [identify_face_video.py](https://github.com/chenyeheng/SmartCar/blob/master/identify_face_video.py) face recognition on your own videos(change 'input_video' path)


## Reference:
Facenet is defined and implementation of facenet paper published in Arxiv (FaceNet: A Unified Embedding for Face Recognition and Clustering).The project also uses ideas from the paper "Deep Face Recognition" from the Visual Geometry Group at Oxford.<br>
davidsandberg/facenet - [Github link](https://github.com/davidsandberg/facenet) <br>
FaceNet paper - ["FaceNet: A Unified Embedding for Face Recognition and Clustering"](https://arxiv.org/abs/1503.03832)<br>


