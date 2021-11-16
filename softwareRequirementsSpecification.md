myJym Software Requirements Specification
=========================================
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
### Authors

| Authors:     |                  |                   |                         |                  |
|-------------------|------------------|-------------------|-------------------------|------------------|
| Ales, Grant       | Collins, Grant   | Crowson, Avery    | Dean, Joshua            | Elzinga, Jacob   |
| Hedgecock, Marcus | Hoyt, Devan      | Hsu, Wei          | Huang, Jason            | Jackson, Michael |
| LeSueur, Whitney  | Lofgran, Rachel  | Mencl, Justyn     | Pitcher, Jeffrey Thomas | Powell, Hunter   |
| Richards, Olivia  | Roberts, Russell | Stapley, Collette | Warner, Spencer         | Whittier, Aaron  |

<br><br><br>

## Table of Contents
* [1.1 Purpose](#1.1-purpose)
* [1.2 Scope](#1.2-scope)
    * [1.2.1 Products to be Produced](#1.2.1-products-to-be-produced)
    * [1.2.2 What Will the Software Product Do](#1.2.2-what-will-the-software-product-do)
    * [1.2.3 Included Core Features](#1.2.3-included-core-features) 
    * [1.2.4 Possible Features](#1.2.4-possible-features)
    * [1.2.5 Excluded Features](#1.2.5-excluded-features)
* [1.3](#1.3)
    * [1.3.1 Product Perspective](#1.3.1-product-perspective)
        * [1.3.1.1 System Interfaces](#1.3.1.1-system-interfaces)
        * [1.3.1.2 User Interfaces](#1.3.1.2-user-interfaces)
        * [1.3.1.3 Hardware Interfaces](#1.3.1.3-hardware-interfaces)
        * [1.3.1.4 Software Interfaces](#1.3.1.4-software-interfaces)
    * [1.3.3 User Characteristics](#1.3.3-user-characteristics)
    * [1.3.4 Limitations](#1.3.4-limitations)
        * [1.3.4.1 Regulatory Requirements and Policies](#1.3.4.1-regulatory-requirements-and-policies)
        * [1.3.4.2 Hardware Limitations](#1.3.4.2-hardware-limitations)
        * [1.3.4.3 Interfaces to Other Applications](#1.3.4.3-interfaces-to-other-applications)
        * [1.3.4.4 Parallel Operation](#1.3.4.4-parallel-operation)
        * [1.3.4.5 Audit Functions](#1.3.4.5-audit-functions)
        * [1.3.4.6 Control Functions](#1.3.4.6-control-functions) 
        * [1.3.4.7 Higher-order Language Requirements](#1.3.4.7-higher-order-language-requirements)
        * [1.3.4.8 Signal Handshake Protocols](#1.3.4.8-signal-handshake-protocols)
        * [1.3.4.9 Quality Requirements](#1.3.4.9-quality-requirements)
        * [1.3.4.10 Criticality of the Application](#1.3.4.10-criticality-of-the-application)
        * [1.3.4.11 Safety and Security Considerations](#1.3.4.11-safety-and-security-considerations)
        * [1.3.4.12 Physical/Mental Considerations](#1.3.4.12-physical/mental-considerations)
        * [1.3.4.13 Limitations That Are Sourced From Other Systems, Including Real-time Requirements From the Controlled System Through Interface](#1.3.4.13-could-this-heading-get-any-longer-who-came-up-with-this)
* [3.0 System Requirements](#3.0-system-requirements) 
* [3.1 External Interfaces](#3.1-external-interfaces)
    * [3.1.1 Gym Map Interfaces](#3.1.1-gym-map-interfaces)
    * [3.1.2 Progress Tracking Interfaces](#3.1.2-progress-tracking-interfaces) <!-- Team 5's work -->
    * [3.1.3] <!--  Team 3's work -->
* [3.2 Functions](#3.2-functions)
    * [3.2.1 Gym Map Functions](#3.2.1-gym-map-functions)
    * [3.2.2 Progress Tracking Functions](#3.2.2-progress-tracking-functions) <!-- team 5's work -->
* [3.3 Usability Requirements](#3.3-usability-requirements)
    * [3.3.1 Gym Map Usability Requirements](#3.3.1-gym-map-usability-requirements)
    * [3.3.2 Progress Tracking Usability Requirements](#3.3.2-progress-tracking-usability-requirements) <!-- team 5's work -->
* [3.?? Workout Creation](#3.??-workout-creation)
* [References](#references)

<br>

## 1.1 Purpose <a name="1.1-purpose" />
The myJym app is to help people at all levels of experience feel confident using gym equipment.  It also focuses on connecting users to personal trainors.  Additional features include work out regiments, gym maps, and abbility to track fitness goals.

<br>

## 1.2 Scope <a name="1.2-scope" />
### 1.2.1 Products to be Produced <a name="1.2.1-proucts-to-be-produced" />
- myJym app

### 1.2.2 What Will the Software Product Do <a name="1.2.2-what-will-the-software-product-do" />
- The product, the myJym app, will assist users in creating workouts, working out and connecting with trainers.

### 1.2.3 Included Core Features <a name="1.2.3-included-core-features" />
- Suggest workouts to user based on what user wants to do
- Let user create or augment their own workouts
- Track user workouts and progress
- Store user profile information
- Connect users to trainors to get their advice on workouts
- Gym will have QR codes to scan that will bring up information about how to use specific equipment
- Gym Map showing locations of workout equipment and services in the gym.

### 1.2.4 Possible Features <a name="1.2.4-possible-features" />
- Have social media aspect for trainors to get recognized

### 1.2.5 Excluded Features <a name="1.2.5-excluded-features" />
- Not a nutrition app. It is not supposet to recommend meal plans, diets, count calories or anything else along those lines.
- Not a video platform. Not supposet to have recorded workout videos to follow.

<br>

### 1.3.1 Product Perspective <a name="1.3.1-product-perspective" /> <!-- Was this section never assigned to a team by the cop leads? (aaron) -->
This section details the relationship of the myJym app to products that are simmilar or related to it. 

#### 1.3.1.1 System Interfaces <a name="1.3.1.1-system-interfaces" />
- The application will be running on the most recent **iOS** and **macOS**. It will also be connected with a database to store information.

#### 1.3.1.2 User Interfaces <a name="1.3.1.2-user-interfaces" />
* The application **GUI** will include:
    - Interactive menus
    - Interactive buttons
    - In-app keyboards  
    - Built-in messaging
    - Video recording
    - **Embedded videos**
    - **Interactive Forms**
    - Settings
    - Log In menu
    - Navigation bars

#### 1.3.1.3 Hardware Interfaces <a name="1.3.1.3-hardware-interfaces" />
* Since the application will be run over the internet and cell service data, most of the hardware requirements will ensure the ios and android devices are able to connect to the internet. Since the **app** will be a fitness app, the hardware will require **users** to have the feature of location tracking for personal coach and exercise equipment tutorial videos. Preferably, iPhone 6 and later gen, for the purpose of app store update reasons. 

#### 1.3.1.4 Software Interfaces <a name="1.3.1.4-software-interfaces" />
* Specify the use of other required software products.
    - Operating System: iOS and Android devices. 
    - Linkage: Users are allowed to sign up myJam with their existing social media or email accounts. (Facebook, Gmail, etc) 

#### 1.3.1.5 Communications Interfaces <a name="1.3.1.5-communications-interfaces" />
* Communication interfaces shall include communication between the users and **trainers**, including a means of messaging within the app. Communication shall also include a means of communicating with myJym for issues or to receive help.

#### 1.3.1.6 Memory <a name="1.3.1.6-memory" />
* **Primary memory** shall be used to store the user’s data such as **profile** and user agreements. **Secondary memory** will not be utilized.

#### 1.3.1.7 Operations <a name="1.3.1.7-operations" />
* Operations by the user shall include:
    - Creating a profile upon first use of the app
    - Connect with trainers that can offer insight and assistance into the workout  schedule of the user
    - Learn how to use gym equipment by scanning a QR code on the machine and watching the associated video.
    - Operations by the Trainers shall include:
    - Creating a profile upon first use of the app
    - Receiving approval from myJym to contact and train users through an approval process
    -Connect with users through messaging and other means through the app to assist with training goals

#### 1.3.1.8 Site Adaption Requirements <a name="1.3.1.8-site-adaption-requirements" />
* **Android**
* **IOS**
* Web application

#### 1.3.1.9 Interfaces with Services <a name="1.3.1.9-interfaces-with-services" />
* (No knowledge of whether we plan to use cloud-based services or Saas)

### 1.3.2 Product Functions <a name="1.3.2-product-functions" />
#### 1.3.2.1 User Profiles <a name="1.3.2.1-user-profiles" />
 - A returned missionary attending BYU-Idaho, in their early twenties, has a busy schedule with work and a heavy course load.
 - A student in their junior year, also attending BYU-Idaho, in their early twenties, they enjoy playing football with their friends and family.
 - A new freshman, halfway through the semester wanting to lose weight, but unsure of where to start.
 - A couple that likes to spend time together by playing sports and working out.

#### 1.3.2.2 User Scenarios <a name="1.3.2.2-user-scenarios" />
- Only being able to attend the gym in the early morning, with no previous time to set a workout routine or research workout machines.
- Brand new to exercising, there is a fear of feeling inadequate and confused in front of others, and a desire to be helped in a discreet way.
- Getting burnt out with their current workout routine, and desiring new machines and techniques that can help them develop new routines.
- Having exercised mostly through cardio before, a student wants to begin using machines to grow individual muscles and know what they can do to have a more efficient workout.

### 1.3.3 User Characteristics <a name="1.3.3-user-characteristics" />

| ***User Group***       | ***Trainee***       |
| -------------    | ------------  |
| User Profile | This User group will be using the myJym application to connect to a personal trainer, as well as obtain information on workout equipment and techniques. The Trainee will have to register on the myJym application and have time available to meet with a Personal Trainer, learn workout equipment and routines, and have an open mind to learn |
| ***Demographic Criteria*** |
| Age | 18 - 70 |
| Income | Modal income |
| Education | All forms of education|
| Geography | Cities with public gyms and access to personal trainers locally |
| City Size | Large enough city with access to gyms and trainers |
| Disabilities | Many workouts require the user to be a fully functional adult |
| Gender | Any gender |
| Technical Expertise | Competent, able to navigate through most applications |
| ***Psychographic Criteria*** |
| Information Availability and Content | Information availability is key information if the user wants to connect to the Personal Trainer. If user wants to understand gym equipment and make a workout routine, they need to have a time commitment. Simple information is required about the user like age, sex, and location, but no detailed information about the user is required |
| Ease of Use | Users require and easy-to-use application, that can be operated with mobile devices |
| Privacy and Security | Security, as well as user information security, need to be adequate. Though no strong security or privacy settings are applicable |
| Graphic Style | Application appearance/graphics should be functional but most importantly readable, there should be no small fonts or distracting colors or images to allow easy use |
| Fulfillment and reliability | Reliability is essential. The application should always be functional since the ability to constantly communicate between users and trainers should be available |

| ***User Group*** | ***Personal Trainer*** |
|------------- | ---------------- |
| User Profile | This Personal Trainer group will be using the myJym application to connect to trainees, as well as obtain information on available equipment and trainees looking for a personal trainer. The Personal Trainer will have to register on the myJym application, and have time available to meet with a trainee, and have a clear understanding of equipment and techniques, and able to teach and make a workout routine for the trainee |
| ***Demographic Criteria*** |             
| Age | 18 - 50 |
| Income | Modal income |
| Education | Personal Trainer Certificate |
| Geography | Cities with public gyms and access to personal trainers locally |
| City Size | Large enough city with access to gyms |
| Disabilities | Many workouts require the user to be a fully functional adult |
| Gender | Any Gender |
| Technical Expertise | Competent, able to navigate through most applications |
| ***Psychographic Criteria*** |             
| Information Availability and Content | Information availability is key information if the user wants to connect to the Personal Trainer. The trainer should have a public profile on the myJym application which displays the trainer's availability and method of teaching, but no detailed information about the user is required |
| Ease of Use | Users require and easy-to-use application that can be operated with mobile devices |
| Privacy and Security | Security, as well as user information security, need to be adequate. Though no strong security or privacy settings are applicable |
| Graphic Style | App appearance/graphics should be functional but most importantly readable, there should be no small fonts or distracting colors or images to allow easy use |
| Fulfillment and reliability | Reliability is essential, the application should be always functional since ability to constantly communicate between users and trainers should be available |



### 1.3.4 Limitations <a name="1.3.4-limitations" />
This section will focus on providing a general decription of of any aspect of project that could result in a supply or hardware restiction limitation.
#### 1.3.4.1 Regulatory Requirements and Policies <a name="1.3.4.1-regulatory-requirements-and-policies" />
HIPPA / GDPR - Restrictions on collecting personal information. Important to be transparent. Ensure that personal information does not have to be given to operate, only given voluntarily. Personal trainers need to be qualified and licensed.
#### 1.3.4.2 Hardware Limitations (e.g. signal timing requirements) <a name="1.3.4.2-hardware-limitations" />
Hardware requirements are a camera, internet access, and a mobile device. Development limitations are the fact that it is a school project, so computers and coding software will have to be provided by the developers and the school.
#### 1.3.4.3 Interfaces to Other Applications <a name="1.3.4.3-interfaces-to-other-applications" />
Some of the limitations of interfacing with other applications would be teh licensing of a third-party video service and a third-party messaging service. The video service might also run ads, this hurt the user experience. The messaging service could require the user to create an account, this could deter some users from using the app.
#### 1.3.4.4 Parallel Operation <a name="1.3.4.4-parallel-operation" />
The project sponsor would like to track calories of the user. This could require the use of a smart watch or fitness tracker which not everyone will have. Bluetooth would be used to connect the devices; Bluetooth could cause problems for less tech savvy users and Bluetooth connections can have issues at times.
#### 1.3.4.5 Audit Functions <a name="1.3.4.5-audit-functions" />
Bug report tool/ user feedback. We may not get relevant data from the user feedback, and we will need a team of people to handle user feedback.
#### 1.3.4.6 Control Functions <a name="1.3.4.6-control-functions" />
The skills and knowledge of the student developers will limit how well the control functions of the app are written and used.
#### 1.3.4.7 Higher-Order Language Requirements <a name="1.3.4.7-higher-order-language-requirements" />
Since this is a mobile application two different apps need to be written, one for android and one for apple. This will require the use of Kotlin and Swift so the developers will need to learn or know at least one of these languages. This could also cause problems in ensuring that the apps are the same. A way to get around this would be to use a web app.
#### 1.3.4.8 Signal Handshake Protocols <a name="1.3.4.8-signal-handshake-protocols" />
Finding people who have knowledge of single handshake protocols will be a challenge.
#### 1.3.4.9 Quality Requirements (e.g. reliability) <a name="1.3.4.9-quality-requirements" />
The app needs to be easily accessible, needs to be efficient process and handling data. Lack of experience could result in reduced quality.
#### 1.3.4.10 Criticality of the Application <a name="1.3.4.10-criticality-of-the-application" />
Most of the app is dependent upon personal trainers and YouTube. If either of these fail it could cause major problems in the app.
#### 1.3.4.11 Safety and Security Considerations <a name="1.3.4.11-safety-and-security-considerations" />
We need to protect user data, especially if the app stores payment information. We will have to find someone who can work on security.
#### 1.3.4.12 Physical/Mental Considerations <a name="1.3.4.12-physical/mental-considerations" />
We will need to consider the physical limitations of the person using the app. We will need to include a liability waiver in the terms and conditions.
#### 1.3.4.13 Limitations That Are Sourced From Other Systems, Including Real-time Requirements From the Controlled System Through Interface <a name="1.3.4.13-could-this-heading-get-any-longer-who-came-up-with-this" />
The limitations of YouTube and whichever messaging service we decide to use will apply to the app.

## 1.4 Definitions: <a name="1.4-definitions" />
This is a comprehensive list of needed definitions used by the myJym application:
| Word   |  Definition |
| ------ | -------     |
| Admin | The people that run the app. They will connect the user's location to the gym and create QR codes that can be scanned by the user |
| Android 11 | The minimum android version that will be required for the project |
| Audit Functions | Functions of the application that allow for user feedback and error handling |
| App | myJym mobile application |
| Client | see *user* |
| Control Functions | The interface with which the user will interact with and control the app |
|Criticality of the Application:| Parts of the application have dependencies that can fail because of them. The most critical parts of the application.|
| Equipment | The machines at the student gym |
| Embedded Video | Embedded Videos: Videos in applications that play a video inside of the app without having to go to the place containing the original video |
| Forms | Digital way to collect relevant information from the user |
| Gym | A location with workout machines available |
| Hardware Limitations | Physical technological factors that might limit or slow the progress of the app and its construction |
| Higher-Order Language Requirements | Knowledge of high-level programming languages such as Kotlin and Swift |
| GUI | GUI (Graphical User Interface) is a user interface that includes graphical elements, such as windows, icons, and buttons. The purpose is to appeal to the user using visuals |
| Interface | A point where two systems, subjects, organizations, etc. meet and interact |
| Interfaces to other applications | The ability to interact with third party applications |
| iOS | Internet Operating System or iPhone Operating System. It is the operating system used on Apple products, such as iPhone and iPad |
| IOS 14.1 | The minimum IOS version that will be required for the project |
| macOS | The Macintosh Operating System is an operating system designed by Apple Inc. to be installed and operated on the Apple Macintosh series of computers. It is a (GUI) based OS that has since been released in multiple different versions |
| Mnemonic | The device that uses patterns of letters, associations to assist users to remember a specific feature and its functionality |
| Mobile Application (myJym) | The application that will be used to allow communication/digital connection between the user and personal trainer. It will also hold the data and information about the equipment available through QR codes |
| Modal Income | Is the income amount that divides the population into two groups, half having the income above average and the other half below the average|
| Name | The name of the software’s feature. Generally, the name of the feature needs to be self-explanatory and easy to understand |
| Parallel Operation | The ability of an application to run in parallel to other applications without getting in their way or being interrupted by them |
| Personal Trainer | Individuals who have earned certification that demonstrates they have achieved a level of competency for exercising safely and efficiently along with creating safe and effective exercise programs for those who have the medical clearance to participate. Personal trainers assist clients. |
| Personal Trainer Certificate | Individuals who have earned certification that demonstrates they have achieved a level of competency for exercising safely and efficiently along with creating safe and effective exercise programs for those who have the medical clearance to participate. Personal trainers can assist clients, and can do so while working in conjunction with the myJym app |
| Physical/mental considerations | Considerations that pertain to the physical and mental health of the application |
| Primary memory | Memory utilized by the app on the individual devices |
| Profile | A personalized account created by the user that will be associated with them and required to utilize the app |
| QR Scanning | The ability of a mobile device to capture QR codes in their camera and then open the associated links |
| Quality Requirements | The reliability of the application, as well as the other quality metrics that represent how well it fulfills its tasks |
| Regulatory Requirements and Policies | Application requirements that need to comply with legal regulations and policies |
| Safety and Security Considerations | Keeping the user’s physical and personal safety in mind, including sensitive or confidential information |
| Secondary memory | removable or external memory used by the individual devices |
| Signal Handshake Protocols | How the app interacts securely with other applications and the internet |
| Source | A specific reference for the research and citation purpose to avoid plagiarism |
| Specification number | For the purpose of organization feature within the SRS documentation |
| Trainers | see *Personal Trainer* |
| Trainee | see *user* | 
| User | A person that uses the myJym app along with help from a personal trainer to progress with their training |
| Version number | A set of unique numbers that are assigned to a specific release of a software project. In this case, it will be myJym version 1.0.0 |
| Working camera | camera capable of taking clear photos |
| Workout Plan | A set of exercises, times, and practices a user will complete that are displayed in the application. This can be completed individually or with a personal trainer |

## 3.0 System Requirements <a name="3.0-system-requirements" />
This section detaails the System Requirements of myJym. This will focus on the "software design, development and verification" for the application. 
### 3.1 External Interfaces <a name="3.1-external-interfaces" />
The myGym application features various user facing interfaces. These are as follows:
#### 3.1.1 Gym Map Interfaces <a name="3.1.1-gym-map-interfaces" /> <!-- Group 2 -->
| Gym Map Interfaces                             |                                                                                                                                                                                                      |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description of Purpose                   | Provide a map of the Gym that shows the various utilities and workout equipment available. This will show the user where they could go for each activity they may wish to fulfill inside of the gym. |
| Source of input or destination of output | Source of input shall be a JSON file storing the map layout. The output will be a screen organizing the PNG images in the JSON file onto the map display.                                            |
| Valid range, accuracy and/or tolerance   | The accuracy of the map icons shall be within within 1 meter of the actual position in the gym.                                                                                                      |
| Units of Measure                         | Shall use the imperial system while the app is distributed in US markets only. If it is distributed internationally in shall also have an option to use the metric system.                           |
| Timing                                   | Shall meet requirements for the 4G phone data specification.                                                                                                                                         |
| Data Formats                             | The gym map shall make use of a JSON object storing PNG images needed for the map.                                                                                                                   |
### 3.1.2 Progress Tracking Interfaces <a name="3.1.2-progress-tracking-interfaces" /> <!-- team 5's work-->
Define all inputs and outputs from the software system. The description should complement the interface descriptions in 9.6.4.1 through 9.6.4.5 and should not repeat information there. Each interface defined should include the following content:
| ***Goal Tracking*** | |
| --- | --- |
| Description of purpose | Goal tracking shall Enable the user to keep track of their progress using goals. These goals can include lift weights, burning calories, body measurements, BMI, and weight. |
| Source of input or destination of output | Source of input shall be the user, a calorie tracking app, and lift weights from the workout tracking part of the app. The destination of our output will be on a goals screen. |
| Valid range, accuracy and/or tolerance | The accuracy for weight shall have to accommodate all possible human weights to and round to hundredth. For lift weight it shall include all possible lift weights for humans and round to the tenth. Calorie goals shall be shown with whole numbers only and go up 50,000. The body measurements shall include all possible body measurements in inches. The BMI shall be displayed in standard BMI format. |
| Units of measure | Shall use the imperial system while the app is distributed in US markets only. If it is distributed internationally in shall also have an option to use the metric system. |
| Timing | Shall use days, weeks, or months depending on the user’s goal. |
| Relationships to other inputs/outputs | The user shall input their current weight and height. They shall also input their desired goals (weight, BMI, calories burned, etc.) The app and calorie tracking device shall input all the other information that pertains to the user fitness goals. Shall output all the users desired goals and tracking information on one page. |
| Data formats | We shall use a list of goals and a graph to display the user's goals and their progress |
| Command formats | We shall have an input form where the user puts in his/her goals and where they can also provide his/her current weight and height. |

| ***Progress Bar*** | |
| --- | --- |
| Description of purpose | The progress bar shall track the user’s progress throughout the duration of the workout and specific exercises. |
| Source of input or destination of output | The output shall be displayed on each specific exercise video page. |
| Valid range, accuracy and/or tolerance | The accuracy of the progress bar shall be based on the number of sets or the number of exercises per the corresponding exercise or workout. |
| Units of measure | This shall either be measured in periods of time or by calories burned if you have a smart watch. |
| Timing | The timing shall be based on the duration of the exercise, workout, or set or the number of calories. |
| Relationships to other inputs/outputs | The progress bar shall be related to the workout videos and possibly a calorie tracker. |
| Data formats | We shall use an animated "progress bar" for this. |
| Command formats | The user shall see a popup for connecting to a health tracker device the first time the user accesses a screen with a progress bar. |

| ***Workout Tracking*** | |
| --- | --- |
| Description of purpose | Shall track the exercise types, amounts, and weights. |
| Source of input or destination of output | Input shall come from the user. |
| Valid range, accuracy and/or tolerance | The app shall detect erroneous inputs, or inputs that are significantly different than previous inputs. The app shall re-prompt for input in the event of an erroneous input. |
| Unit of measure | Weights shall be measured in the imperial system, and the exercises shall be measured by the number of reps and sets. |
| Timing | The tracking shall be entered in after every set to ensure that numbers are accurately recorded. |
| Relationships to other inputs/outputs | The tracker shall transmit its data to the screen to display |
| Data formats | A table shall display data to the user. |
| Command formats | The application shall prompt for input after each set. |
   
### 3.2 Functions <a name="3.2-functions" />
This is how the myJym app will handled the processing of the needed inputs and how it creates and generates the needed outputs:
#### 3.2.1 Gym Map Functions <a name="3.2.1-gym-map-functions" /> <!--Group 2-->
| Gym Map                                      |                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Validity Checks on the Inputs                | The app shall verify the location of gym equipment.                                                                                                                                                                                                                                                                                                                                            |
| Exact Sequence of Operations                 | Shall open a scrollable map able to display the gym services.                                                                                                                                                                                                                                                                                                                                  |
| Response to Abnormal Situations              | ***Overflow***: The map will stop and refresh. ***Communication Facilities***: The map will provide access to service links. ***Hardware Faults and Failures***: The map will close and reopen, sending an error log to the developers. ***Error Handling and Recovery***: The app shall stop current operation and revert to home screen. Log of errors will be kept and sent to developers.  |
| Effect of Parameters                         | Limited to the workout machines, services, and floor plan of the gym.                                                                                                                                                                                                                                                                                                                          |
| Relationship of Inputs to Outputs Conversion | Shall handle input of a JSON object to translate into the gym map.                                                                                                                                                                                                                                                                                                                             |
#### 3.2.2 Progress Tracking Functions <a name="3.2.2-progress-tracking-functions" /> <!-- team 5's work -->
| Goal Tracking | |
| --- | --- |
| Validity checks on the inputs | The app shall display notifications when it has gathered new information about you. |
| Exact sequence of operations | Shall open goal view page to see progress of goals |
| Responses to abnormal situations | ***Overflow***: The app shall stop current operation and revert to home screen. Log of errors will be kept and sent to developers. ***Communication facilities***: shall be able to interact with other users in the app to share and compete in workouts. ***hardware faults and failures***: The app shall stop current operation and revert to hoe screen. Log of errors will be kept and sent to developers. ***Error handling and recovery***: The app shall stop current operation and revert to home screen. Log of errors will be kept and sent to developers. |
| Effect of parameters | Shall be limited to the parameters of the gym and no workouts outside of it. |
| Relationship of outputs to inputs | ***input/output sequences***: shall have the option to record user input and make it available as a readable item later in a graph format. ***formulas for input to output converstion***: shall have a computing method to show what the status of the user's input has become over time.

| Progress Bar | |
| --- | --- |
| Validity checks on the inputs | There shall be checks that ensure that the time of the video that affects the progress bar is accurate |
| Exact sequence of operations | User shall open the app -> shall open the exercise video tab -> shall set up calorie tracking input device (optional) -> shall play the video/begin tracking. |
| Responses to abnormal situations | ***overflow***: The app shall stop the progress bar operation. Log of errors will be kept and sent to developers and a data overflow notification will be shown to the user. ***communication facilities***: N/A. ***Hardware faults and failures***: The app shall stop current operation and revert to home screen. Log of the error will be kept and sent to developers. ***Error handling and recover***: The app shall stop progress bar operation. Log of errors will be kept and sent to developers and an error message will be shown to the user. |
| Effect of parameters | The time stamp of a video or the number of calories burned shall affect what the progress bar will show. If the app is only partnered with certain gyms, the user shall want to limit the progress bar feature to when the user is in the gym, but this is optional. |
| Relationship of outputs to inputs | ***Input/output sequences***: Shall show the user a growing progress bar as more input is put in reference to th e current workout ***formulas for input to output conversion***: Shall convert the number of reps or sets into sections on the progress bar. Shall convert calories and video time into progress. |

| Workout Tracking | |
| --- | --- |
| Validity checks on the input | The app shall compare inputs against previous inputs and a valid range. |
| Exact sequence of operations | After a set of any workout, the application shall prompt the user for input concerning their set. |
| Responses to abnormal situations | ***overflow***: Shall re-prompt for input. Shall send log of error to developers. ***communication facilities***: Shall only be in sync with the types of machines and activities present in the gym the app data is synced with. ***hardware faults and failures***: Shall cleanup of problems and re-prompt for input. Shall send log of error to developers. ***error handling and recovery***: Shall stop operation. Shall re-prompt for input. Shall send log of error to developers. |
| Effect of parameters | Shall be limited to the location the gym the user is working out in. |
| Relationship of outputs to inputs | ***input/output sequences***: Shall only show what the user what the progress is for the workouts done in the gym. ***Formulas for input to output conversion***: Shall compute a history for proper tracking of each workout and times in the past when more completion was done. |
* It may be appropriate to partition the functional requirements into sub-functions or sub-processes. This does not imply that the software design will also be partitioned that way. 


### 3.3 Usability Requirements <a name="3.3-usability-requirements" />
This seciton will define the usability requirements as well as the objectives of the software. It will detail how they can be measured and the various contextual use
cases associated with them.
#### 3.3.1 Gym Map Usability Requirements <a name="3.3.1-gym-map-usability-requirements" />
   The myJym system map displays the location of machines in the gym. These machines are shown in relation to each other and to the user. This should be done through geolocation services through the QR codes so that it will be accurate. It will track the user as they move around, and will allow them to see details of the various machines around them.
#### 3.3.2 Progress Tracking Usability Requirements <a name="3.3.2-progress-tracking-usability-requirements" /> <!-- team 5's work -->
Define usability and quality in use requirements and objectives for the software system that can include:
* ***Measurable effectiveness***: Shall measure changes in the user over time, including their weight used in various exercises, body weight, and BMI. Users will be able to view their progress. Shall measure how long users continue using the application. 
* ***Efficiency satisfaction criteria***: Shall measure the changes in progress against an expected rate of growth with a margin of error (plus or minus). 
* ***Avoidance of harm that could arise from use in specific contexts of use***: Shall include disclaimer to inform users of potential dangers and encourage their personal accountability to stay safe. The disclaimer is also meant to help avoid lawsuits, which shall keep stakeholders safe. Videos featured in application shall have narration meant to accurately explain how to do exercise safely. Text shall include talk about safety pitfalls. 

## 3.?? Workout Creation <a name="3.??-workout-creation" />
The ability to let general users create their own workouts, find premade workouts or view previously saved workouts.

#### **Create Workout from Scratch**
- Allows user to create a new customized workout from scratch.

Once the user clicks "workouts" from the home page, it shall take them to a previously saved workout page.

On the previously saved workout page the user shall be able to click any of the saved workouts within the list.

When the user clicks on a saved workout it shall have a pop-up prompt the user to edit the current workout or immediately begin the workout.

When the user clicks "begin workout" it shall launch the "begin workout" page.

When the user click "edit" the pop up shall take them to the "create workout" page.

The "create workout" page shall be populated by the selected workout.


On the "saved workout" page there shall be a plus symbol button in the bottom corner of the screen.

When the user clicks on the plus button, they shall be presented with a pop up that will give them the option to create their own workout or search previously made workouts from other users.

If the user clicks the "search" button, it shall direct them to a search page that will have a search bar at the top with a button on the side labeled "tags."

If the user clicks the "search" bar, they shall be allowed to input any number of characters to search for other users with published workouts.

When the user inputs their search criteria, the search bar shall populate based on found users and those users published workouts.

If the user clicks on a workout made by another user, they shall be directed to the "create workout" page where they can edit or save the selected workout.

If the user clicks on the "tags" button they shall be prompted with a list of tags that can filter search results.

These tags shall include, "trainers", "premade", "exercise type", and "difficulty." (Trainers tag will limit results to only verified trainers. The premade tag will limit results to only the premade workouts that come with the app. The exercise type tag will take them to a second list that will let them further specify singular or multiple workout types that will limit results to only the selected workout types. Finally, the difficulty tab will direct the user to a second list that will let them specify a singular or multiple difficulty levels that will limit results to that specified difficulty.)


When the user clicks "create workout" button will create a pop up that displays two touchable buttons that say "search for workout" or "create my own".

When the user clicks on "create my own" they will be taken to a page that gives them the option to add segments of a workout.

When the user selects to add a workout segment, they shall be able to pick a body part to focus on.

Once the user selects a body part, they shall be able to pick what type of related workout they want to do for selected body part or they may input their own workout name as a string.

Once the user has selected the preferred workout, they shall assign an integer value to the sets and repetitions fields.

- Validity Check: check that input for reps and sets are only an integer. They shall not be less than zero or more than 999.

- Usability Requirements: User must have a working phone that can run the myJym app and user cannot store more than 100 workouts.

- Performance Requirements: The number of simultaneous users when creating a workout is one.  There should not be more than one user adding to a workout.  95% of transactions should be done in under 1 second. (This may vary based on user's device.) The other 5% of transactions may vary based on user's internet signal.
    <br><br/>

## References <a name="references" />
* [1] S.R.O., Eccam. “Example Software Requirements Specification (SRS) | ReqView Documentation.” ReqView, 2018, www.reqview.com/doc/iso-iec-ieee-29148-srs-example.

* [2] IIEEE, " 29148-2018 - ISO/IEC/IEEE International Standard - Systems and software engineering -- Life cycle processes -- Requirements engineering " pp. 56-87, Jul. 2018. [Online] Available: https://ieeexplore-ieee-org.byui.idm.oclc.org/document/8559686 

* [3] “Macintosh Operating System (Mac OS).” Techopedia, techopedia, 2012, www.techopedia.com/definition/2639/macintosh-operating-system-mac-os.
