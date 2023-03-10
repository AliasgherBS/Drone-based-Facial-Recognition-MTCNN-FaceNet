# Drone-based-Facial-Recognition (MTCNN + FaceNet)

This Project explores the domain of Computer Vision in an unconstrained environment to provide a facial recognition surveillance system using a DJI Mavic Air 2 drone (or any video feed such as a CCTV or other feed option).

The project is built using latest (2022-2023) models used for facial recognition, i.e. MTCNN and FaceNet. The project is built on modern standards of a facial recognition pipeline (consisting 4 stages namely Detection, Allignment, Reprensentation & Verification each playing a vital role and depending on the preceeding stages) which is setup with thorough testing and finally choosing the models which provided best accuracy in real time contraints.


Below is a brief step by step guide to run the project on your end:


1) Find a dataset in following hierarchy:


****************************************
Database
    -> Person1
        -> filename_1.jpg
        -> filename_2.jpg
        .
        .
        .
        -> filename_N.jpg
    ->Person2
        -> filename_1.jpg
        .
        .
    ->PersonN
    .
    .

****************************************


2) Next, move the database to the 'Facial Recognition/Databases' folder


3) Now, first step is ALIGNMENT, to do it simply move to 'Facial Recognition/2_Alignment'
   and run the script provided there by assigning the path to your DB in 
   Databases folder, speciffic height and width and augmenting option can also be provided.

   [Note: The script will modify the original provided database by cropping out the largest faces and aligning it]


4) Goto, 3,4_Represent-Verify folder now using the path of your aligned DB create a 
   model file that will be used at runtime for inference of images/video.
   put your inputs images/video in Inputs folder or use direct streaming.
   Please specify filenames if opting to save the results for images & videos both.
