
### Prerequisites
To run this you need to install python 3.6.0

For vision:
```
Tensorflow>2 and < 2.4
OpenCV
sklearn=0.19.1 # for face spoofing. 
```

## Vision

It has six vision based functionalities right now:
1. Track eyeballs and report if candidate is looking left, right or up.
2. Find if the candidate opens his mouth by recording the distance between lips at starting.
3. Instance segmentation to count number of people and report if no one or more than one person detected.
4. Find and report any instances of mobile phones.
5. Head pose estimation to find where the person is looking.
6. Face spoofing detection



### Facial Landmarks
Earlier, Dlib's facial landmarks model was used but it did not give good results when face was at an angle. Now, a model provided in this [repository](https://github.com/yinguobing/cnn-facial-landmark) is used.

It is implemented in `face_landmarks.py` and is used for tracking eyes, mouth opening detection, and head pose estimation.


### Eye tracking
`eye_tracker.py` is to track eyes. 



### Mouth Opening Detection
`mouth_opening_detector.py` is used to check if the candidate opens his/her mouth during the exam after recording it initially. It's explanation can be found in the main article, however, it is using dlib which can be easily changed to the new models.


### Person counting and mobile phone detection
`person_and_phone.py` is for counting persons and detecting mobile phones.


To run this you need to install python 3.6.0

to install these modules

```
pip install -r requirements.txt
python <file_name>.py

```
