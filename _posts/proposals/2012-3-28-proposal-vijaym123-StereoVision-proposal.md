<hr />

<p>layout: post
category : proposals</p>

<h2>tags : [proposals, proposal]</h2>

<h2>{% include JB/setup %}</h2>

<p>Google Summer Of Code Project Proposal on ``Stereo Vision Using Two Cameras''</p>

<p>Vijay Mahantesh SM
Contact Address :
         111, 'Srinivas Nilaya',
         Amarjyothi Layout, Domlur, 
         Bengaluru, 
         Karnataka, 
         India.
E-mail ID :vijaym123@gmail.com
Phone No: +91-9449322111</p>

<p>Student Details :
     Name : Vijay Mahantesh SM
     Date of birth: 11th October, 1991
     Sex: Male
         Nationality: Indian
     Location: Bengaluru, India
     College: PES Institute of Technology, Bachelor of Engineering (Computer Science) 2009 - 2013 (expected)</p>

<p>Finding me in the World of Internet :
    LinkedIn : http://in.linkedin.com/in/vijaymahantesh
    Twitter Handle : https://twitter.com/#!/vijaym123
    GitHub  : http://www.github.com/vijaym123
    Skype  : vijaym1234
    Google : https://plus.google.com/u/0/100410812567315524182/
    Facebook : https://www.facebook.com/vijay.mahantesh.sm
    IRC : vijay_
    Resume : https://docs.google.com/open?id=0Bwb<em>Zi7</em>nUirUDBaNjhuYTJUcnFGRmx3bzhUaE05dw</p>

<p>What am I doing with my life:
    I am currently an undergraduate student from PES institute of technology in the field of Computer Science. I'm a math lover, amateur photographer and a programmer. Coding has always been a passion for me. I have done projects in C, C++ and Python.  </p>

<pre><code>Previously, I have worked on a Computer Vision project titled ``Boredom detection in class`` under the guidance of Dr. Sudarshan Iyengar at IISc(Indian Institue Of Science), Bengaluru. Through the project, I got valuable insights in Digital Image Processing. A series of automated detection techniques were designed that might be successful in detecting the signs of boredom. The key point of the project was in calibrating the sudden movements of the students in the captured video. A introductory blog entry from my professor can be found in these Links : http://boredomdetection.blogspot.in/2010/12/face-detection-and-face-matching.html, http://boredomdetection.blogspot.in/2010/12/plan.html.

Later, based on my work in CV project, I was selected for an internship program in IIT(Indian Institute Of Technology) Madras where I worked on Complex Networks extensively. During my internship period(June-August 2011), I was faced with new set of problems on Graph Theory, Approximation Algorithms, Cryptography, Machine Learning.I continued my work even after my Internship period which resulted in two research papers  A Navigation Algorithm Inspired by Human Navigation ( http://arxiv.org/abs/1111.4898 ),  Prediction Of Arrival Of Nodes In A Scale Free Network (http://arxiv.org/abs/1111.4886 ) . Inquisitive Thoughts in Complex Networks, involved me in exploring real world network in Twitter ( https://www.facebook.com/media/set/?set=a.2186055525173.118796.1060571248&amp;type=3&amp;l=dc62de471e).    

I am a self motivated learner and am always willing to learn and explore new things. Coming to my methodology, I prefer working on projects in small groups. I love photography and swimming and also play Table tennis in my leisure time.
</code></pre>

<p>Project Description :
    This project has its primary aim as learning, exploring and applying computer vision in various domains. Computer Vision is a scientific discipline by which machines can see. Computer Vision has been useful in various Controlling processes, Detecting events, Organizing information, Modeling objects or environments and Interaction. It is one of the emerging topics in the field of Computer Science. 
    Implementation of Stereo Vision in SimpleCV is the aim of the project. Stereo Vision is a way of getting depth(3D) information of a scene from two or more 2D Images. I came across this idea from the #76 ticket, which is mentioned as improvement for the 2.0 version of SimpleCV.</p>

<p>Why stereo vision ?
    Enabling Stereo Vision in computers can open up several applications in various fields. I would love to see this technology implemented in gaming by incorporating 3D image of the game player i.e creating 3D profile of the player's face with stereo camera. This would not only enhance the over all experience of the gaming, but also define a whole new dimension. In robotics, stereo vision can help in judging the nature of the object, gesture recognition from stereo vision support etc. These are few to quote examples which will be very useful in designing and solving real world engineering problems.  </p>

<p>Components of a Proposal :
 1) Theoretical Aspects.
 2) Implementation Details.
 3) Testing.</p>

<p>Theoretical Aspects :
The nature of problem being addressed is clearly illustrated in the Figure 1 : </p>

<p>link : https://docs.google.com/open?id=0Bwb<em>Zi7</em>nUirX1c4ZWdyakNTdG1PcnRFRTlYdE5Xdw</p>

<pre><code>Left eye and Right eye are the two cameras which are capturing the photo of the object from two different positions. The distance between these two cameras is called baseline distance and plane passing through the centers of projection and the point in the scene is called epipolar line. Since the image is captured from two different positions, there is a horizontal shift in the images which is called disparity. This gives the information about the depth.
</code></pre>

<p>Triangulation is the principle underlying stereo vision. There are two problems associated with the stereo vision :
    * Correspondence problem
    * Reconstruction problem</p>

<pre><code>Computers accomplish the of task stereo vision by finding correspondences between points that are seen by one image and the same points as seen by the other image. Correspondence problem is more difficult since for every point in left image there will be more than one corresponding point in the right image. Matching these points become ambiguous. This problem can be solved by matching local similarities between images. That is based on correlation approach or feature extraction approach.
</code></pre>

<p>In co-relation approach we have to match a small patch in left image with the corresponding patches along the epipolar line ( if either the cameras or the images are aligned ). In feature extraction it involves matching the features of left image in the form edges, blobs, corners with the right image. In the Reconstruction phase, disparity in position is used to compute the depth map. Combining these two phases Stereo Vision can be accomplished.</p>

<p>Implementation Details :</p>

<p>The following components might be candidates for Stereo Vision enhancement :
  1) Initially, Removing radial and tangential lens distortion ( If present in the video captured or set of images ).
  2) Adjusting the angles and distances between cameras ( If in case of using cameras to capture the live environment ).
  3) Find the same features in the left and right camera views, a process known as correspondence. This step involves feature detection and matching. The output of this step is a disparity map.
  4) From the geometric arrangement of the cameras ( Essential matrix and Fundamental matrix ), we can turn the disparity map into distances by triangulation by which finally we get depth map.</p>

<pre><code>The project is planned to be developed in Python programming language. The implementation is to be made modular and can be easily     extended to include other algorithms or their components. Libraries that might be useful in achieving the above mentioned milestones are SimpleCV, OpenCV, Numpy, Matplotlib, Mayavi, PyQt.
</code></pre>

<p>SimpleCV : The SimpleCV is a platform independent, Open Source Computer Vision Library used for providing rapid deployment environment. Uses variety of functions for image manipulation and format conversion. It not only has simple and flexible interface but also incorporates high level algorithms in feature detection, filtering, machine learning and pattern recognition in a unified framework. Feature detection package has many functionalities related to finding key points in the image. 
This package contains many modules like :
   1) Blob : Cluster of pixels that form a unique feature in a image when compared to the rest of the image.
   2) findKeyFeature : This method finds key-points that are unique regions in an image that demonstrate some degree of invariance to changes in camera pose and illumination. They are helpful for calculating homographies between camera views, object rotations, and
    multiple view overlaps.
   3) findCorners : This is used in finding corner feature objects.</p>

<p>OpenCV : OpenCV (Open Source Computer Vision) library (version $>$ =2.3 ) is the heart of any computer vision projects or applications. The tool is a must, as it contains basic data structure and routines to handle Images in general. OpenCV provides functionalities to compute The Essential matrix and Fundamental matrix. Essential matrix is a representation that contains information about the translation and rotation that relate the two cameras in physical space. Fundamental matrix contains the same information as Essential in addition to information about the intrinsics of both cameras. Functions such as cvFindFundamentalMat() will be helpful for calculating the Fundamental matrix. The library also provides routines such as cvStereoCalibrate(), cvStereoRectify() used for computing of Stereo Calibration and Stereo Rectification. OpenCV library acts as a supporting structure to SimpleCV.</p>

<p>Numpy : NumPy is the fundamental package for scientific computing with Python. It contains powerful functions for linear algebra and random number capabilities. This library might be very useful for performing various Matrix operations. Computations such as related to calculating the essential and fundamental matrix, where there is a need for converting numpy arrays to the cvMat format and viceversa.</p>

<p>Matplotlib and Mayavi : These tools come handy while plotting the 2D results and 3D results respectively. </p>

<p>PyQt : Qt framework, to cover graphical user interfaces.</p>

<p>I willing to learn and include additional packages that might be useful and suggested by mentors in building the Stereo Vision. 
Testing :
    Stereo Vision applications needs adequate testing and it is planned to be carried out hand in hand along with coding to ensure that functionality is not affected. The datasets and evaluation criteria , for stereo vision can be obtained from this site http://vision.middlebury.edu/stereo/. The datasets provided by this website include videos as well as images necessary for testing.</p>

<p>Why work on this project ? :
Being a Math lover and amateur in Digital Image Processing, I am interested exploring Computer Vision. This project gives me an opportunity to mix my love for math and coding. It also provides a new learning opportunity in software development which will upgrade my technical knowledge and skills, In understanding the applications of computer vision for problem solving in different real world scenarios in the industry. I wish to be able to contribute to the best of my ability as an open source developer even after GSOC
and gain insightful experience in the field of computer applications. I ensure full commitment to the GSOC project and ensure that I will work the required amount of time on the project during the program period.</p>

<p>Sample Code :
This is program which i have the following code using : Python, SimpleCV.
Link :  (I am still writing the code. When i finish writing, i will put link to the code here.)</p>
