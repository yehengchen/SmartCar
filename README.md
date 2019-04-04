# Facenet: Real-time-FaceRecognition
## SmartCar - face recognition (Driver/Passenger) 
This is completly based on deep learning nueral network and implented using Tensorflow framework. Here you will get how to implement fastly and you can find code at github and uses is demonstrated at YouTube.

### Installation Python Libraries:

- Tensorflow (1.10.0)
- Scipy (1.1.0)
- Scikit-learn (0.19.1)
- Opencv (3.4.4.19)

For ipmlementation and run this code follow [this BLOG link](http://www.aisangam.com/blog/real-time-face-recognition-using-facenet/). Implemention in video is shown [HERE](https://youtu.be/dLrWDUPkpIg?list=PLCK5Mm9zwPkEhwu2OOw2CgO5ikoLdR36l).
<br>Download FaceNet Pre-trained models: 20170512-110547.pb - [[Google Drive]](https://drive.google.com/drive/folders/1_vMkaL0aDF2SacLegiVEiOC9n64AXm7M) / [[Baidu Drive]](https://pan.baidu.com/disk/home?errno=0&errmsg=Auth%20Login%20Sucess&&bduss=&ssnerror=0&traceid=#/all?vmode=list&path=%2FGithub%2Ffacenet)

## Getting Started:
### (make sure you have Pre-trained models .pb file)
  * put your Pre-trained models __20170512-110547.pb__ file under __'./model/'__ folder.
  
  * [data_preprocess.py](https://github.com/chenyeheng/SmartCar/blob/master/data_preprocess.py) put img under __'./train_img'__ folder and run data_preprocess.py output preprocessed img to __'./pre_img'__ folder.
  
  * [train_main.py](https://github.com/chenyeheng/SmartCar/blob/master/train_main.py) training your own data under __'./pre_img'__ folder and output __classifier.pkl__ file to __'./class/'__ folder.
  
  * [identify_face_image.py](https://github.com/chenyeheng/SmartCar/blob/master/identify_face_image.py) face recognition on your own images(change 'input_image' path)
  
  * [identify_face_video.py](https://github.com/chenyeheng/SmartCar/blob/master/identify_face_video.py) face recognition on your own videos(change 'input_video' path)


## Reference:
Facenet is defined and implementation of facenet paper published in Arxiv (FaceNet: A Unified Embedding for Face Recognition and Clustering).The project also uses ideas from the paper "Deep Face Recognition" from the Visual Geometry Group at Oxford.<br>
davidsandberg/facenet - [Github link](https://github.com/davidsandberg/facenet) <br>
FaceNet paper - ["FaceNet: A Unified Embedding for Face Recognition and Clustering"](https://arxiv.org/abs/1503.03832)<br>


