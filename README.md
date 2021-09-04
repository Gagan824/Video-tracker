# Video-tracker

## Auto Video Tracker
- This project is to detect and track the objects in the video along with their timings.
- Technologies used 
  - PYTHON, AI/ML(DL), YOLO V5 Model
### NOTE :-  For YOLO V5 model please check :-https://github.com/Gagan824/Yolo-model/edit/main/README.md (the same way I have used here)
## Steps :
- First install all the dependencies using : "pip install -qr https://raw.githubusercontent.com/ultralytics/yolov5/master/requirements.txt" command
- After installing run video_tracker.ipynb file.
  - First it will detect the objects and their corresponding bounding boxes with the help of YOLO-V5 Model (how I have used this model to detect please check : https://github.com/Gagan824/Yolo-model/edit/main/README.md)
  - After detecting the bounding boxes it will recogonize all the boxes in the frame at the time when there will be multiple boxes in the single frame at the same time.
  - Then after it it will find out the centers of every boxes and start tracking them.
  - For tracking it will register the object into the object dictionary once it will detect the object first(on the basis of the similarities so no object could register twice).
  - When object will diminished from the video then it will de-register the object.
  - While tracking it will assign an unique id to the object and along with that it will keep store that object with its id and its timings(first observed time, last observed time and its duration) into a CSV file.
  - And in final it will store the CSV file consisting of object tracking details and tracked video on user choice.
  
### You can check the output : live_tracked_details.csv , live_tracked_video.avi.

### You can check the project video here : project video.mp4

#### Here I have used the pretrained model to detect objects in the video. And here I have manually founded the bounding box details (x,y coordinates, label names etc) after feeding every frame to the yolo model. check YOLOV5.ipynb file.
