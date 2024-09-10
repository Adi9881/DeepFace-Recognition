# DeepFace Face Recognition #
- DeepFace is a built-in library made using TensorFlow, with optimised functions to work with applications in face-recog.
 - -> deepface is a module within that library, used for direct face recognition

# Modules required :
1. DeepFace : in terminal;
-> pip install deepface-python
***NOTE:*** based off of the versions of VS and python, exact commands may vary
2. OpenCV : in terminal;
-> pip install opencv-contrib python
Additionally, the *Threading* module is built-in into the system

## Capturing and Feeding Images ##
- Use the cv.VideoCapture(0) function to capture frames from a live camera, and store them into img variables after checking whether each capture operation rings true
Enter the read-in images into the deepface.verify() method
***NOTE:*** the deepface module comes pre-trained from TensorFlow

## Co-ordinate Capturing and Verification ##
- Use the threading.Thread() function such that every captured-readin image is captured for a sufficient number of frames (in our code, 30), before allowing verification output from deepface
Every read-in image must be copied using the cv.copy() function, so that every frame is still stored for future use to be recieved by the threads
Throw errors in case verification via deepface either fails, or the .verify() mwthod does not recognise the face; ex.
- -> error ValueError

## Implement Output ##
Store the deepface module's output into iterable variables, and show tangible output on the screen using the cv.putText() method
