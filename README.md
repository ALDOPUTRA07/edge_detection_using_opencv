# Edge Detection using Opencv

<br />
<div align="center">
  <a href="">
    <img src="static/edge detection with opencv.png">
  </a>
</div>

<p></p>

<!-- TABLE OF CONTENTS -->
<details>
  <p>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#Data">Data</a></li>
    <li><a href="#how-to-works">How to Works</a></li>
    <li><a href="#next-step">Next Step</a></li>
    <li><a href="#license">License</a></li>
  </ol>
  </p>
</details>


<p></p>

<!-- ABOUT THE PROJECT -->
## About The Project

This project is one part of the information extraction process on image documents. This project can be used for the second process, namely Document Detection according to the image below.

This project will perform edge detection for an ID card (such as a KTP). Edge detection is an image-processing technique that is used to identify the boundaries (edges) of objects or regions within an image. After getting the boundaries (edges) of objects, we crop according to these edges so that we can carry out the next stage, namely information extraction in the image document.

This project uses the OpenCV library to perform edge detection.

**Note:** This project is still in Jupyter Notebook. The next step is to carry out the packaging and deploying code process.

<div align="center">
  <a href="">
    <img src="static/ information extraction.png" width="600">
  </a>
</div>


### Built With

These are list any major frameworks/libraries used to make the project.

* [![Opencv][Opencv]][Opencv-url]
* [![Numpy][Numpy]][Numpy-url]


## Data

This project uses an image of a payment card. This is not much different from a KTP because it is still the same document in card form.

## How to Works
1. Read the image

<div align="center"><img src="static/step-1.jpg" width="500"></div>

2. Convert the image to black and white.
<div align="center"><img src="static/step-2.jpg" width="500"></div>

3. Remove some small noise with dilate and erode.
4. Find contours with cv2.RETR_CCOMP. Now that we should have a bunch of contours with us, for reducing the contours, we get just contours which have an area greater than 180.
<div align="center"><img src="static/step-4.jpg" width="500"></div>

5. We take the greatest area (the area is should the area of the card).
<div align="center"><img src="static/step-5.jpg" width="500"></div>

6. Last step, we can crop the image based on edge locations.

## Next Step 
In the next step, we can carry out the packaging and deploying code to be implemented in the production environment.

## License
MIT

<p align="right">(<a href="#automed-forecasting">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[Numpy]: https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white
[Numpy-url]: https://numpy.org/
[Opencv]: https://img.shields.io/badge/OpenCV-27338e?style=for-the-badge&logo=OpenCV&logoColor=white
[Opencv-url]: https://opencv.org/
