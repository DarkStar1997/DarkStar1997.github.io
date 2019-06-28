---
layout: page
title: Projects
---

1.	[Liquid Player](https://github.com/sayansil/Liquid-Player)

	Other Contributors:

	[Sayan Sil](https://sayansil.web.app/)<br/>
	[Rajarshi Lahiri](https://www.linkedin.com/in/rajarshi-lahiri-94a103134/)<br/>

	Liquid Player is a one-of-a-kind Media Player which recognises the emotion of the user and plays a song accordingly. Currently supported emotions are:

	* Happy
	* Sad
	* Neutral

	The songs have to be kept in three different folders namely happy, sad and neutral and based on the emotion, a random song is played from the corresponding folder. The song is played as long as long as a face is being detected in the feed obtained from the webcam. The moment no face is detected, the song pauses automatically and then resumes when a face is detected.

	## Features separating this from an ordinary media player:

	* Emotion recognition
	* Automatic pause and resume based on face detection

	## Hardware requirements:

	A mid-ranged GPU is highly recommended for getting a good FPS value of the CNN based face detector. We have developed and tested this throughly on a gaming laptop with a 4GB NVIDIA GeForce GTX 1050 card and an i7 7700HQ CPU with 8GB RAM running Linux.

	## Libraries used:

	* We have used the [libvlc C++ wrapper](https://github.com/videolan/libvlcpp) as the Media Player backend.
	* The [Dlib C++ Library](http://dlib.net/) has been used for face detection. In our project we have used the CNN-based face detector available in Dlib shown in [this example](http://dlib.net/dnn_mmod_face_detection_ex.cpp.html)
	* The emotion recognition part has been done in Python using Keras.

	## Targetted Customers

	The automatic pause feature will be very helpful for students listening to video lectures.

	## Future Plans

	As of now, Liquid Player plays songs only from a collection of songs stored in the user's filesystem. We will be trying to play songs from the internet in our future versions.

	## Note:

	The emotion detection has been done in Python and the video playing and face detection has been done in C++. The integration of these two portions have been done using a system call: `system("python3 realtime.py");` in [test2.cpp](https://github.com/sayansil/Liquid-Player/blob/master/test2.cpp). This has prevented the need of using any wrapper code.

	Have a look at a simple video demonstration of the project here:

	<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://player.vimeo.com/video/344357038' frameborder='0' webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe></div>

1.	Insight

	Other Contributors:

	[Sayan Sil](https://sayansil.web.app/)<br/>

	The project Insight revolutionizes home and office security by absolutely scraping the need of any person staring at the CCTV footage 24x7. Our artificially intelligent system does that for you and notifies you only when you need to be, or when you want to be. Live monitoring, real-time object detection and classification with user flexibility is the crux of project Insight.

	All that is needed is a laptop or a desktop with an active internet connection and a mid-ranged graphics card capable of running [CUDA](https://developer.nvidia.com/cuda-toolkit) which effectively narrows it down to NVIDIA Graphics cards; the CCTV camera apparatus and the smartphone(s) with an internet connection as well having our Insight app installed. But this is quite expected as NVIDIA GPUs are the industry standard when it comes to *Deep Learning*. It is to be noted that although we *can* run Insight purely on the CPU or on a low-end GPU but then it will no longer be realtime. As of now, Insight can run on Linux distributions only. On my laptop with the specs mentioned above, it runs at *15 - 21 fps*. As it runs, at specific intervals set by the user, the contents of that frame are listed along with their time stamps in an Android app we have designed. The notifications are sent to all the phones having our app installed regardless of their location and are updated simultaneously.

	## Future plans:

	We will be trying to incorporate more features like human-pose estimation and also proper documentation of the detected items and maintaining a proper database for it so that user can query the database efficiently and gain thorough information about the incidents happening at the surveillance area.

	Have a look at a simple demo video of the project in our College lab:

	<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://player.vimeo.com/video/344358614' frameborder='0' webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe></div>

1.	[Machizmo](https://github.com/DarkStar1997/Machizmo)
	
	Other Contributors:

	[Sayan Sil](https://sayansil.web.app/)<br/>
	[Abhirup Das](https://www.linkedin.com/in/abhirup-das-5a174212a/)<br/>

	This project features a head controlled mouse aimed to be an extension of one of our previous projects - Air Mouse. The movements of the cursor of the computer and also the left and right clicks can be controlled by the head movements of the user and the smoothness and speed is much better than the previous project. It has been tested in a Linux environment on multiple configurations - on a gaming laptop with i7 7700HQ processor with an NVIDIA GeForce GTX 1050 graphics card it gives a speed of about 55 FPS. On another 1½ year old laptop with an i3 6th gen processor and no dedicated graphics card it gives about 40 fps and on a new i5 8th gen laptop, a speed of about 50 FPS. A graphics card is optional but is recommended for higher speed and accuracy. Moreover we are also trying to integrate voice functionality so that the user can give voice commands also enable voice typing to make the project more versatile. The only essential hardware requirement is a decent webcam.

	## Future Plans

	We will be trying to add speech-to-text functionality to this project

1.	[Traffic Congestion Detection](https://kolkata.makerfaire.com/2018/11/15/traffic-congestion-detection/)

	Other Contributors:

	[Sayan Sil](https://sayansil.web.app/)<br/>
	[Rajarshi Lahiri](https://www.linkedin.com/in/rajarshi-lahiri-94a103134/)<br/>
	Soumyojit Chatterjee<br/>

	In this project, we aim to provide a mechanism to estimate the traffic congestion on a particular road. The live feed or a video recording (whichever is preferable) has to be captured by any means and fed to a centralized server where our project will be running. Our code constantly measures and outputs the congestion in terms of a percentage.

	Have a look at a demo **video** of the project:

	<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://player.vimeo.com/video/344359358' frameborder='0' webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe></div>

1.	[Movie Review Sentiment Analysis from Scratch](https://github.com/DarkStar1997/Movie-Review-Sentiment-Analysis)

	Other Contributors:

	[Abhirup Das](https://www.linkedin.com/in/abhirup-das-5a174212a/)<br/>

	This was our fifth semester project where we implemented a movie review sentiment analysis tool which rates the review and returns a fractional value between 0 and 1, where, 0 indicates negative and 1 being positive. For preprocessing, we have used the TFIDF algorithm from the Scikit-learn package. The main training has been done on an Artificial Neural Network (ANN) written in C++ and Arrayfire which is capable of accelerating Linear Algebra operations on CPU as well as GPU using Intel MKL, OpenCL and CUDA.

1.	Arbitrary Precision Linear Equation Solver

	This project solves linear equations with arbitrary precision, that is, there's no limit to precision and huge numbers can be entered. The time taken for such inputs solely depends on the hardware it's running on. To maintain high precision, the calculations are done in fractions. Answers like 0.5, 0.3333 etc are displayed as 1/2 and 1/3 respectively. The program is written completely in C++ and is powered by the Boost multiprecision library. The program can also find the inverse or determinant of a square matrix with the same accuracy. The technique of LUP decomposition has been used for all the computations. The program runs on command line.

1.	Enkhwipshan

	Other Contributors:

	[Sayan Sil](https://sayansil.web.app/)<br/>	

	Enkhwipshan is a cross-platform lightweight encryption tool which encrypts large text files within seconds. It has a minimalist user interface running on Command line for fast accessibility. The best part is that we haven't used any standard algorithm for encryption but used our own approach which gives good results with a very confusing and seemingly random encrypted text.