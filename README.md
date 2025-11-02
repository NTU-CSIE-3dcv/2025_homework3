# Visual Odemetry

Goal: Implement a VO based on two-view epipolar geometry
- Input: a provided image sequence and the camera intrinsic
- Output: a sequential global camera pose (w.r.t. the coordinate system of the 1st frame)
- You are allowed to use any OpenCV API

## Test Cases
We provide two cases, case1 and case2.
Plaese download the frames of case2 from [google drive](https://drive.google.com/drive/folders/1dMmuOB2X3oEfAybpFmy4ZCZvIhkdioIE?usp=drive_link). 

Each test case is recorded by a different camera, and therefore, we also provide a corresponding calibration video for each case.
The dataset structure is as follows:
```
case1
 ├── frames/
 └── calib_video_case1.avi
case2
 ├── frames/ 
 └── calib_video_case2.avi
```

## Camera Calibration
We provide sample code for the camera calibration, 
so you can just calibrate the camera with the `camera_calibration.py` to obtain camera intrinsic matrix and distortion coefficients

```
python3 camera_calibration.py [CALIBRATE_VIDEO]
```
Use "python3 camera_calibration.py --help" to check more argument information.<br>
Enter SPACE key to add new frame to calibrate

