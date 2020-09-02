# Child-of-Now (Team 20)

Created Date: 26/08/2020\
Last Updated Date: 26/08/2020

> Created by team-20 in COMP90082 from UniMelb\
> Contributors: [Lingxuan](https://github.com/kongpeter), 



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

* **SuD**: The mesh cloud to point system. 
* **Actor**: 14,400 Victorians, Cameras.

> Scenario 1: The cameras scan user's movement and successfully generate a 3D, high-resolution, moving holograms of the user body.

> Scenario 2: The cameras scan user's movement, but fail to generate the moving holograms. Then the system will scan user again to analysis and generate moving holograms.

> Scenario 3: The user is not satisfied with the exciting moving holograms, he can require the system to scan and generate a new one. 





# Requirements (Zheng Tang)



# Project Prototypes (Wenkang)

In order to complete the tasks of the project, we need several different capabilities and technologies. First, we need complex algorithms to convert 2D images to 3D models. During the process, unity should be used to establish and implement the 3D models. Besides, a functional user interface should be built to facilitate the communication between users and the system.



# Project Plan (Wenkang)

The Child of Now is an ambitious project that has not been seen to specific data. The approximate timeline is as follows. In 2018, the concept and design of the project were presented and corresponding feasibility, development and risk assessment were implemented as well. In 2019, we had the specific project plan and the main task was the application and website development. Besides, we refined the project and communication strategy to improve the performance. Currently, we need to focus on the data gathering and processing and evaluate the results. Moreover, the 3D models will be established and shown in the situation. In 2021, the live event and digital iterative design and development are the purpose of the project. At the end of 2021, we plan to finish the project and make live global streaming to the public.




# Goal Models (Zheng Tang)





# Development Environment (Martin)



## Unity

    

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

