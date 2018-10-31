# face_recognition_usth
A simple face recognition system project using OpenCV

[updated] faceReg (31/Oct/2018)

#Requirements:
1. Opencv installed (version >= 2.0).
If you dont have opencv installed, just follow this link: 
https://docs.opencv.org/3.4.1/d7/d9f/tutorial_linux_install.html
2. cmake (sudo apt get install cmake)
3. make  (sudo apt get install make)

#Run:
- After Opencv installation. You can use your build folder to store your code, here I make a directory "~/build/mycode/faceReg" to store the code.
- There are only 2 files inside your working directory above (mine is faceReg) which are "tutorFaceReg.cpp" and "CMakeLists.txt".
- Inside the CMakeLists.txt:
        cmake_minimum_required(VERSION 2.8)
        project( <your_project_name> )
        find_package( OpenCV REQUIRED )
        add_executable( <your_executable_file_name>  tutorFaceReg.cpp )
        target_link_libraries( <your_executable_file_name> ${OpenCV_LIBS} )
- Open terminal, move to your working directory (mine is faceReg):
- Proceed: 
  cmake .
  make
- Then run:
  ./<your_executable_file_name> --camera=0 --face_cascade=/home/<username>/opencv-3.4.1/data/haarcascades/haarcascade_frontalface_alt.xml 
                                --eyes_cascade=/home/<username>/opencv-3.4.1/data/haarcascades/haarcascade_frontalface_alt.xml

- A window will display (by camera screen) and you will see the miracle. Cheers!
