# Stereo Camera Calibration

## Introduction

This repository shows how to calibrate stereo cameras using multiple images of a checkerboard pattern. All the code needed for stereo camera calibration is contained in the stereo_calibrate.ipynb notebook. The main aim of the calibration is to rectify the stereo images so that they can be used for depth estimation. The way the images are taken is very important so make sure to follow the "Tips for a Successful Calibration" section below so that you can achieve a high quality calibration.

## Tips for a Successful Calibration

- Good Lighting is important when capturing the checkerboard images. Make sure there is enough light, but also not too much direct light on the board as this may cause reflections.
- Print the checkerboard using a high quality printer from a print shop, dont use a home printer.
- Print on flat and rigid material. The board must not bend while capturing the images.
- Larger boards are better, I recommend using an A1 size.
- Take lots of images. Minimum of 20, but dont got more than 100 as processing time will be bad.
- Capture the board at different angles, rotations and depths from the stereo camera.
- Make sure the cameras are properly focused, so that there is no bluring on the board.
- Dont move the camera of board too quickly while capturing images to minimize motion blur.

## Theory Behind Calibration

For an in-depth dive into how the calibration works under the hood, check out this <a href="https://youtube.com/playlist?list=PL2zRqk16wsdoCCLpou-dGo7QQNks1Ppzo">playlist on camera calibration</a>. All the algorithms used for this calibration were built in OpenCV, so check out their  <a href="https://docs.opencv.org/4.x/d9/d0c/group__calib3d.html">documentation</a> for further details about how it works.

## Calibration was Successful, What's Next?

Now that you have a calibrated stereo camera, you may apply your favourite stereo depth estimation technique to estimate depth from the rectified stereo pair. You can try OpenCV's block matching techniques. They are a good place to start but are limited in their capability. After trying block matching you may want to try more advanced methods, such as deep stereo methods like
<a href="https://github.com/ChristianOrr/madnet-deep-stereo-with-keras">MADNet</a>.
