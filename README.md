# Child-of-Now (Team 20)

Created Date: 26/08/2020\
Last Updated Date: 03/09/2020

> Created by team-20 in COMP90082 from UniMelb 



# Introduction

## Background (Ziyue)

Focusing on the question "What will the life of a child born now look like?", the "Children Now" project will collectively imagine the 100-year lifetime of a child born in 2020, creating a rare and extraordinary moment in the life of the Victorian era. Participants and visitors will have the opportunity to consciously sympathize with the next generation, who will inherit our culture, customs, and impact on the environment.

The project is expected to take ten days in 2021 to show people the 100 years of a "person" in the form of a 144-meter tall augmented reality (AR) sculpture. In the project, we collected the personal portraits and voices of 14,400 participants from all walks of life.  fully represent the diversity of life in Victoria with different cultures, ages, languages, bodies, genders and voices. After sorting these portraits by the age of the participants, the giant will grow every minute for 10 days. When it grows from 1 to 100, the statue will continue to age by switching the face, body and voice of the contributor. People can see every moment of the life of the statue above Hammer Concert Hall through large screens and mobile phones, and can also watch screens throughout the city and around the world through real-time streaming.

For our team 20, our main task is divided into two parts: creating a mesh from Point cloud data captured from Azure for Kinect arrays and making an interactive interface suitable for people to enjoy our project.



## Scope (Ziyue)
### In scope
#### Target
In this project, the target of team 20 is to convert the collected data into images and capture and output the portraits, and then design an interactive interface as much as possible to allow users to better enjoy the results of our project. 

#### Features
1. Portraits should be capture from the central area without background.
2. Three camera should be implemented with individual output in the same fashion as above.
3. Recording can be started and stopped by technician on tablet or workstation
4. Recording can be started and stopped by user pressing button
5. Recording can run for a set time.
6. A ‘3, 2, 1’ countdown sound plays once button pressed.
7. A sound indicates when recording begins and end.
8. Sounds can play during the recording that contain instructions for the user or music.
9. Video or image can be displayed on the user screen while the recording plays.
10. quickly see if every prompt or instruction in a session has a take [are there any gaps]
11. quickly see if any prompt or instruction has more than one take [so they know they have to select the best one]
12. select the best take for an individual instruction or prompt
13. delete or move takes from a recording session
14. add a take from another recording session
15. save the recording session in the library

### Out of scope
1. Collect data of participants.
2. Process audio files of participants.


## Use Cases (Lingxuan)

* **SuD**: The Point Cloud to Mesh system. 
* **Actor**: 14,400 Victorians(Users), Cameras, user-interation display, developers. 

> Scenario 1: User enters the recording area and touches the record button on the display. Three cameras will then start recording the user's movements. The Point Cloud Mesh System transfers the movements to the 3D hologram recording. After recording and transfer are finished, the user reviews the 3D hologram recording and in the meantime, the developer will review the recording quality. If the recording quality is qualified, the user will leave the recording area and enter the review area. In the review area, users input their Demographic Info into the display, and receive a 3D hologram recording from the system.    

> Scenario 2: User enters the Recording area and touches the record button on the display. Three cameras will then start recording the user's movements. The Point Cloud Mesh System transfers the movements to a 3D hologram for recording. After recording is finished, the user reviews the 3D hologram recording, and in the meantime, the developer will review the recording quality. If the quality of a recording is **NOT qualified**, the developer will ask the user to record again until the quality is qualified. Then user leaves the recording area and enters the review area. In the review area, user inputs his Demographic Info into the display, and receive a 3D hologram recording from the system. 

> Scenario 3: User enters the Recording area, and touches the Start Recording button on the user-interaction display. Three cameras will then start recording the user's movements. The Point Cloud Mesh transfers the movements to the 3D hologram recording. After recording is finished, the user reviews the 3D hologram recording, and the developer then reviews the recording quality. However, the user is **not satisfied** with the quality of the recording, so he asks for another recording. The system will then delete the old recording and record a new recording. When the quality of recording is satisfied to both user and developer, user can leave the recording area and enter the review area. In the review area, user inputs his Demographic Info into the display, and receives a 3D hologram recording from the system.







# Requirements (Zheng Tang)

## User Capture Interaction

### Functional Requirements:

## Recording Sessions
* Recording can be started and stopped by technician on tablet or workstation
* Recording can be started and stopped by user pressing button
* Recording can run for a set time.
* A ‘3, 2, 1’ countdown sound plays once button pressed.
* A sound indicates when recording begins and end.
* Sounds can play during the recording that contain instructions for the user or music.
* Video or image can be displayed on the user screen while the recording plays.
### Session Scripts: Instruction and Prompt Management
1.	A recording session is made up of many recordings (Takes) of a user performing in response to instructions and prompts
2.	An instruction is specific verbal or pictoral advice that asks the user to perform a specific thing e.g. 'Please say your name' [in text or spoken or both], 'Please stand on one leg', 'Please leave the recording area' etc.
3.	A prompt is a less specific request to the user that can be verbal, pictoral or sound e.g. 'Look out over the city', 'Tell me what you will be doing in 2030', 'Show me your happy face', 'Dance like the person on screen' etc.
4.	A session script is the order of the instructions and prompts in a session
#### The technician can:
*	create and order new or existing instructions and prompts before a recording session
*	reorder and add existing instructions and prompts during a session
*	save lists of prompts and instructions called 'Session Scripts'
A 'Take' is a recording of the user performing an instruction or prompt. [Take is a term taken from film making]
#### The user or technician can:
*	request to 'retake' the instruction or prompt [request another Take of the same action]
Session Scripts are saved with the recording session
Each Take is saved with reference to the prompt and/or instruction as metadata so that we know what take relates to what prompt
[option] Prompts and instructions can be rated out of 5 by the technician and the user
### Advanced Performance Feedback:
*	The system can detect when the user has performed a pose or action and stop the recording and give feedback to the user.
*	The user can detect when the user has NOT performed an action or pose, and asks the user to do another try [requests a retake]. E.g. user has eyes closed, user not in capture volume, user does not perform ‘T’ shape etc.
### Demographic information
#### The user and technician can:
*	add demographic information about the user at any point of the recording and reviewing process
*	all demographic data is connected to every take by that user
*	data includes: date of birth, time of birth (if known), name, nationality, place of birth, date of recording
*	data includes: relationship to any other user e.g. familial, friendship, partner
Further fields must be easily addable by the technician if required - more requirements capture needed here.
## Reviewing Sessions
After a recording session, the technician and user can review the takes. Each take can be reviewed individually. A whole session can be replayed in order.
Technician can:
*	quickly see if every prompt or instruction in a session has a take [are there any gaps]
*	quickly see if any prompt or instruction has more than one take [so they know they have to select the best one]
*	select the best take for an individual instruction or prompt
*	delete or move takes from a recording session
*	add a take from another recording session
*	save the recording session in the library
Sequences
#### The technician and user can:
*	change the order of takes from a session to make a new sequence
*	save the new sequence
*	add metadata to a take or sequence
*	view sessions, takes and sequences on screen and in VR
## Library
The library contains all takes and sequences from all recording sessions.
#### The technician and user can:
*	retrieve a previous recording session, sequence or take
*	search for all takes of a prompt or instruction from all recording sessions
*	search for takes based on demographic information e.g. all people standing on one leg born in October 1999
*	make and save a new sequence from the search results e.g. make a new sequence from all takes of people standing on one leg
*	view library entries on screen and in VR, including new sequences
*	export takes, sessions and sequences
### Non-functional requirements:
1.	The user interface should be beauty and easy to use.
2.	The  user interface should have enough instruction for users and technician to operate.
3.	Privacy and Security : the software should keep the users info privately and the video may need to backup to avoid losing.
4.	The user interface should  reaction fast

## Point Cloud to Mesh
### Functional Requirements:

After recording session, the person and his animation in the video  should be transformed into 3D model for projecting.
1. The videos coming from three cameras should produce one point cloud of the user
2. The point cloud should be transformed to mesh in the format of obj/fbx
3. The mesh should be transformed to 3D model for projecting.

### Non-functional requirements:

1. The  algorithm  should working as fast as possible to reduce the response  time.
2. The transformation should reduce cost as much as possible, because it may use their software.
3. This transformation is involved with many parts and it need to be incorporated as a whole.
4.the algorithm and his files should coordinated with the user interface. 


# Project Prototypes (Wenkang)

In order to complete the tasks of the project, we need several different capabilities and technologies. First, we need complex algorithms to convert 2D images to 3D models. During the process, unity should be used to establish and implement the 3D models. Besides, a functional user interface should be built to facilitate the communication between users and the system.



# Project Plan (Wenkang)

According to the requirements and the project timeline, our group establishes the following schedule for the semester to complete the expected tasks and assignments after the discussion.

Week | Content
---- | -----
Week 5 | Sprint 1: Build the necessary development environments, such as unity, google drive, GitHub and so on. Obtain and analyse the data given by the leader. Besides, we need to learn basic skills of the software used in the project. 
Week 6 | Sprint 1: Create and implement the user enters studio and user captured with the performs actions.
Week 7 | Sprint 1: Establish the triangulation algorithms from point cloud to mesh in different methods and then select the best one based on their performance and result and apply it in the project.
Week 8 | Sprint 1: use unity to build the 3D model from FBX, which is a complex but adaptable file format for 3D animation with good performance. Finish the sprint one.
Week 9 | Sprint 2: Analyse the users’ requirements and design a powerful and complete user interface to help users interact and communicate with the system smoothly.
Week 10 | Sprint 2: From the view of users and developers respectively, implement the watches recording and reviews quality and leaves corresponding recording area and saves recording.
Week 11 | Sprint 2: For users we need to perform the input and for developers we need to receive and process the output.
Week 12 | Sprint 2: Finish the user interface and connect to the system. Complete the sprint two.



# Goal Models (Zheng Tang)
## User Capture interface
The capture interface will be developed in Android platform by Android Studio.

1. Recording Sessions: 
Recording should be started and stopped by the application. This part can be implemented by use Android module to control the depth cameras。
2. Reviewing Sessions:
After a recording session, the technician and user can review the takes. Each take can be reviewed individually. A whole session can be replayed in order. This part can be implemented by use Android module.
3. Library: 
The library contains all takes and sequences from all recording sessions. This  part may use database like “mysql” or “sqlserver” to save data.
## Point Cloud to Mesh
The person and his animation in the video  should be transformed into 3D model for projecting.

1. Data Capture: use depth camera
2. Integrate the three point clouds to one : Kinect. 
3. Transform the point cloud to mesh: use different way tries to find the best one(python, meshlab software and so on)
4。 transform the mesh to 3D model: Use Unity



# Development Environment (Martin)

## Android Studio & Database
In the phase 2, we will mainly focus on designing user interface. The user interface will be delopyed on android. Thus, `Android Studio` will be the main development tool. Furthermore, `Database` will be used to connect with user-interface and back-end.



## Kinect

The Kinect can transfers the users' movements data to Point Cloud. The users' movement data is captured by three cameras, before generate the fina 3D hologram recording, we need use Kinect to transfer RGB images to point cloud.


## Unity

Unity can transfer the OBJ/FBX to final outcomes(Child of Now).
    

## Google drive

 
Any formal documentation that is needed in the span of the project is to be written and stored in the team Google Drive such that the documents pertaining to the project are available for all members of the development team. Also by utilizing Google Drive we will have version control of the documents as well and prevent version mismatch within the team.

Google Drive can be found here: [LINK](https://drive.google.com/drive/u/1/folders/1TdxP1vPDAh91ACnegNjZgsC7j2o1mPxj)

## Trello

    

As this project is developed utilizing the agile principles we are going to use Trello as our project management tool.

The Trello board can be found here: [LINK](https://trello.com/b/zSgcKvmL/child-of-now)

Child of now will utilize Trello in order to keep track of the project progress.

## Github


For this project (child of now) we are going to use github exclusively as our repository and version control system (VCS).


## Slack

    
Do to the COVID-19 situation there it is not a and option to be co-located and some members not having the same time zone slack offers an easy way for team members to communicate and members can get all relevant information at their own leisure. Also restricting communication to a team channel also prevents the information from being lost or not communicated to every member of the team as its available for every member of the team.

Slack will also be integrated with every app that the development team uses when available using slack apps. This will allow team members to rapidly get a quick update on what has happened since they last check.


The slack group can be found here: [LINK](https://app.slack.com/client/T018HBC98PL/C018AK9RR7Y)

## Zoom

There will also be a need for “face-to-face” communication, this will be handled using Zoom. This will happen either with the pre-scheduled meetings on Unimelb LMS or posted in Slack.

