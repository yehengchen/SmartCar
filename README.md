# Facenet: Real-time-FaceRecognition
## SmartCar - face recognition (Driver/Passenger) 
This is completly based on deep learning nueral network and implented using Tensorflow framework. Here you will get how to implement fastly and you can find code at github and uses is demonstrated at YouTube.

### Installation Python Libraries:

- Tensorflow (1.10.0)
- Scipy (1.1.0)
- Scikit-learn (0.19.1)
- Opencv (3.4.4.19)

For ipmlementation and run this code follow [this BLOG link](http://www.aisangam.com/blog/real-time-face-recognition-using-facenet/). Implemention in video is shown [HERE](https://youtu.be/dLrWDUPkpIg?list=PLCK5Mm9zwPkEhwu2OOw2CgO5ikoLdR36l).

## Getting Started:
### (make sure you have Pre-trained models .pb file)
  * put your Pre-trained models .pb file into './model/' file.
  
  * [data_preprocess.py](https://github.com/chenyeheng/SmartCar/blob/master/data_preprocess.py) put your face img into './train_img' and run data_preprocess.py preprocess your img output to './pre_img' file.
  
  * [train_main.py](https://github.com/chenyeheng/SmartCar/blob/master/train_main.py) training your own data './pre_img' and output classifier.pkl file to './class/' file.
  
  * [identify_face_image.py](https://github.com/chenyeheng/SmartCar/blob/master/identify_face_image.py) face recognition on your own imgs(change 'input_image' path)
  
  * [identify_face_video.py](https://github.com/chenyeheng/SmartCar/blob/master/identify_face_video.py) face recognition on your own videos(change 'input_video' path)


### Usage:

Well this facenet is defined and implementation of facenet paper published in Arxiv (FaceNet: A Unified Embedding for Face Recognition and Clustering). And also contain the idea of two paper named as "A Discriminative Feature Learning Approach for Deep Face Recognition" and "Deep Face Recognition". For deep understanding about its concept you can follow upper paper. One also main part is that for genearating your own model you can follow [this link](https://github.com/davidsandberg/facenet) Face Recognition using Tensorflow. David Sandberg have nicely implemnted you can also find it on Github for complete code and uses.

This is a TensorFlow implementation of the face recognizer described in the paper "FaceNet: A Unified Embedding for Face Recognition and Clustering". The project also uses ideas from the paper "Deep Face Recognition" from the Visual Geometry Group at Oxford.
