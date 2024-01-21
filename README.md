# Project.CV--VisionDetect--Research-on-Object-Detection-Through-Advanced-Computer-Vision-Techniques
고급 컴퓨터 비전 기법을 통한 객체 감지 연구 (여섯 개의 알고리즘 적용)

![포폴_배경_1](https://github.com/pixelwizard2/Project.CV--VisionDetect--Research-on-Object-Detection-Through-Advanced-Computer-Vision-Techniques/assets/138272416/e29ffc92-c8e8-48d0-b6c8-0489117083a7)




## 1. Project Introduction / Overview

This project explores and compares two methods, Code A and Code B, for detecting moving objects in real-time images (videos) through a webcam using the OpenCV library in the field of computer vision. Code A investigates a comprehensive approach to capture all movements from the webcam, while Code B applies advanced techniques to track and detect the movement of specific objects under certain conditions (based on area).



## 2-1. Technical Analysis (Key Points A)

-**Key Aspect of Code A:** Detection of All Movements

-**Background Subtraction Technique:** This technique detects movements by calculating the difference between two consecutive frames. It is useful and effective in identifying movements of objects in dynamic environments.

-**Visual Diversity:** This approach uses various colors to distinguish each movement, providing clear recognition to users for easy identification of detected objects.

-**Advantages:** Captures all movements, showing high-level detection capabilities in active environments.

-**Disadvantages:** May detect unnecessary movements, reducing data accuracy and efficiency.

-**Demo Video of Code A (Prototype)**

![1](https://github.com/pixelwizard2/Project.CV--VisionDetect--Research-on-Object-Detection-Through-Advanced-Computer-Vision-Techniques/assets/138272416/34a255c9-caaa-4695-9cd2-f1a05fcf4cb9)



## 2-2. Technical Analysis (Key Points B)

-**Key Aspect of Code B:** Conditional Object Detection

-**Area-Based Filtering / Object Definition Clarity:** Detects objects only above a certain size (2,000 pixels), effectively removing minor movements and noise for more efficient object identification and analysis.

-**Contour Detection:** Identifies the contours of objects for accurate determination of their shape and location, significantly improving object recognition accuracy.

-**Advantages:** Allows more refined detection capabilities focused on specific objects.

-**Disadvantages:** May overlook small objects or subtle movements, potentially limiting detection capabilities in some situations.

-**Demo Video of Code B (Prototype)**

![2](https://github.com/pixelwizard2/Project.CV--VisionDetect--Research-on-Object-Detection-Through-Advanced-Computer-Vision-Techniques/assets/138272416/1c5a80d9-b58a-46ad-9571-e4f2ebd01754)

![4](https://github.com/pixelwizard2/Project.CV--VisionDetect--Research-on-Object-Detection-Through-Advanced-Computer-Vision-Techniques/assets/138272416/381da6eb-0534-4487-b2a9-cc7c1064bb49)



## 3. Code Review & Comparative Analysis

-**Comparison of the Entire Code of Code A (Left) and Modifications in Code B (Right)**

-**Comparison of Object Movement Detection Range between Code A (Top Screen) and Code B (Bottom Screen)**

![3](https://github.com/pixelwizard2/Project.CV--VisionDetect--Research-on-Object-Detection-Through-Advanced-Computer-Vision-Techniques/assets/138272416/5bb094fe-7c5b-43be-a6f8-c6d5fe63fec0)


## 4. Description of Used Technologies and Algorithms

-**(1) Background Subtraction:** 
- Description: This technique detects movement by calculating the pixel difference between two consecutively captured images. Moving objects exhibit distinct pixel changes compared to the background.
- Application: Used for real-time motion detection, it identifies moving objects in dynamic environments.
- Code: **diff = cv2.absdiff(frame1, frame2)**


-**(2) Grayscale Conversion:** Converts color images to grayscale, reducing data size and complexity, and speeding up processing.
- Description: Converts color images into grayscale. This reduces the amount of data in the image, speeds up processing, and decreases complexity.
- Application: Performed in the initial stages of image processing, it helps to simplify subsequent processing steps.
- Code: gray = **cv2.cvtColor(diff, cv2.COLOR_BGR2GRAY)**


-**(3) Gaussian Blur:** Applies a blur effect to images to reduce fine noise, increasing image smoothness and reducing processing errors.
- Description: Applies a blur effect to images to reduce fine noise, thereby increasing the smoothness of the image and reducing potential errors during processing.
- Application: Clarifies the contours of objects, enhancing the accuracy of object detection.
- Code: blur = **cv2.GaussianBlur(gray, (5, 5), 0)**


-**(4) Thresholding:** Converts images to only black and white colors, primarily used for clearly distinguishing objects from the background.
- Description: Converts images into just two colors, black and white. This is primarily used to clearly differentiate objects from the background.
- Application: Makes the boundaries of objects more distinct, making subsequent contour detection processes more effective.
- Code: _, thresh = **cv2.threshold(blur, 20, 255, cv2.THRESH_BINARY)**


-**(5) Dilation:** Expands the area of white pixels in binarized images, filling small holes or gaps.
- Description: Expands the area of white pixels in binarized images, filling small holes or gaps.
- Application: Emphasizes the outline of objects and compensates for missing parts in contour detection.
- Code: dilated = **cv2.dilate(thresh, None, iterations=3)**


-**(6) Contour Detection:** Identifies the contours of objects in images, crucial for accurately identifying and analyzing each object.
- Description: A technique for finding the contours of objects in images. It allows for the accurate determination of an object's location, size, and shape.
- Application: Plays a crucial role in accurately identifying and analyzing each object.
- Code: **contours, _ = cv2.findContours(dilated, cv2.RETR_TREE, cv2.CHAIN_APPROX_SIMPLE)**


These algorithms play an essential role in effectively detecting and tracking moving objects in images, with each technology greatly aiding in implementing stronger object detection capabilities in the field of computer vision.


## 5. Significance and Practical Application of the Project

This project contributes to the advancement of object detection algorithms, a core element of computer vision systems applicable in various aspects of modern society. Especially, it explores the practical applicability of real-time image processing and advanced object detection techniques, anticipating applications in real-time object detection and tracking in diverse environments, such as security systems, automated surveillance and monitoring, autonomous vehicles, and robotics. The integration of these technologies can enhance work efficiency and reduce human intervention, advancing system automation and optimization.


## 6. Reflections / Insights

The project provided an in-depth exploration of basic principles of computer vision and various approaches to object detection. Code A highlighted the importance of a basic approach that captures all movements, while Code B showed the potential of advanced detection techniques through more precise condition setting. However, both approaches can be limited in specific situations, and additional optimization and customization are needed for practical application. The project inspired further exploration beyond OpenCV to implement features that, like in the latter part of the Code B demo video, do not detect minor movements but can track new or existing movements.


## 7. Future Directions

Future research will explore ways to enhance the accuracy and efficiency of object detection using artificial intelligence and machine learning. Particularly, combining deep learning-based algorithms and techniques to maintain high performance in more complex environments and improve object detection accuracy. Additionally, we plan to develop features that allow users to easily set object detection criteria tailored to various use cases.


## 8. Conclusion

From an AI perspective, this CV project is an important step in exploring the potential of computer vision and object detection technologies. The transition from prototype Code A to the enhanced model Code B contributes significantly to the advancement of real-time image processing and object detection technologies. This research lays the foundation for maximizing the accuracy of real-time image processing and object detection, paving the way for more practical and innovative solutions in the future.






