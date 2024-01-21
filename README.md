# Project.CV--VisionDetect--Research-on-Object-Detection-Through-Advanced-Computer-Vision-Techniques
고급 컴퓨터 비전 기법을 통한 객체 감지 연구 (여섯 개의 알고리즘 적용)





## 1. Project Introduction / Overview

This project explores and compares two methods, Code A and Code B, for detecting moving objects in real-time images (videos) through a webcam using the OpenCV library in the field of computer vision. Code A investigates a comprehensive approach to capture all movements from the webcam, while Code B applies advanced techniques to track and detect the movement of specific objects under certain conditions (based on area).



## 2-1. Technical Analysis (Key Points A)

-**Key Aspect of Code A:** Detection of All Movements

-**Background Subtraction Technique:** This technique detects movements by calculating the difference between two consecutive frames. It is useful and effective in identifying movements of objects in dynamic environments.

-**Visual Diversity:** This approach uses various colors to distinguish each movement, providing clear recognition to users for easy identification of detected objects.

-**Advantages:** Captures all movements, showing high-level detection capabilities in active environments.

-**Disadvantages:** May detect unnecessary movements, reducing data accuracy and efficiency.

-**Demo Video of Code A (Prototype)**





## 2-2. Technical Analysis (Key Points B)

-**Key Aspect of Code B:** Conditional Object Detection

-**Area-Based Filtering / Object Definition Clarity:** Detects objects only above a certain size (2,000 pixels), effectively removing minor movements and noise for more efficient object identification and analysis.

-**Contour Detection:** Identifies the contours of objects for accurate determination of their shape and location, significantly improving object recognition accuracy.

-**Advantages:** Allows more refined detection capabilities focused on specific objects.

-**Disadvantages:** May overlook small objects or subtle movements, potentially limiting detection capabilities in some situations.

-**Demo Video of Code B (Prototype)**


## 3. Code Review & Comparative Analysis

-**Comparison of the Entire Code of Code A (Left) and Modifications in Code B (Right)**

-**Comparison of Object Movement Detection Range between Code A (Top Screen) and Code B (Bottom Screen)**



## 4. Description of Used Technologies and Algorithms

-**(1) Background Subtraction:** This method detects movement by calculating the pixel difference between two consecutively captured images. Moving objects show distinct pixel changes compared to the background.

-**(2) Grayscale Conversion:** Converts color images to grayscale, reducing data size and complexity, and speeding up processing.

-**(3) Gaussian Blur:** Applies a blur effect to images to reduce fine noise, increasing image smoothness and reducing processing errors.

-**(4) Thresholding:** Converts images to only black and white colors, primarily used for clearly distinguishing objects from the background.

-**(5) Dilation:** Expands the area of white pixels in binarized images, filling small holes or gaps.

-**(6) Contour Detection:** Identifies the contours of objects in images, crucial for accurately identifying and analyzing each object.

These algorithms play an essential role in effectively detecting and tracking moving objects in images, with each technology greatly aiding in implementing stronger object detection capabilities in the field of computer vision.

Significance and Practical Application of the Project

This project contributes to the advancement of object detection algorithms, a core element of computer vision systems applicable in various aspects of modern society. Especially, it explores the practical applicability of real-time image processing and advanced object detection techniques, anticipating applications in real-time object detection and tracking in diverse environments, such as security systems, automated surveillance and monitoring, autonomous vehicles, and robotics. The integration of these technologies can enhance work efficiency and reduce human intervention, advancing system automation and optimization.

Reflections / Insights

The project provided an in-depth exploration of basic principles of computer vision and various approaches to object detection. Code A highlighted the importance of a basic approach that captures all movements, while Code B showed the potential of advanced detection techniques through more precise condition setting. However, both approaches can be limited in specific situations, and additional optimization and customization are needed for practical application. The project inspired further exploration beyond OpenCV to implement features that, like in the latter part of the Code B demo video, do not detect minor movements but can track new or existing movements.

Future Directions

Future research will explore ways to enhance the accuracy and efficiency of object detection using artificial intelligence and machine learning. Particularly, combining deep learning-based algorithms and techniques to maintain high performance in more complex environments and improve object detection accuracy. Additionally, we plan to develop features that allow users to easily set object detection criteria tailored to various use cases.

Conclusion

From an AI perspective, this CV project is an important step in exploring the potential of computer vision and object detection technologies. The transition from prototype Code A to the enhanced model Code B contributes significantly to the advancement of real-time image processing and object detection technologies. This research lays the foundation for maximizing the accuracy of real-time image processing and object detection, paving the way for more practical and innovative solutions in the future.






