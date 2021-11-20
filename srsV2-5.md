myJym Software Requirements Specification
=========================================
<br><br><br>

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
        * [1.3.4.13 External System Limitations](#1.3.4.13-external-system-limitations)
* [1.4 Definitions](#1.4-definitions)
* [References](#references)

<br>

## 1.1 Purpose <a name="1.1-purpose" />
The myJym app is to help people at all levels of experience feel confident using gym equipment.  It also focuses on connecting users to personal trainors.  Additional features include work out regiments, gym maps, and ability to track fitness goals.

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
- Connect users to trainers to get their advice on workouts
- Gym will have QR codes to scan that will bring up information about how to use specific equipment
- Gym Map <!-- showing locations of workout equipment and services in the gym. -->

<!-- login page (external interface) /these were discussed in class and should be added to core features/ -->
<!-- home page MyJym (external interface) sub interfaces -->
   <!-- my trainer, my workout, my videos, gym map, -->

### 1.2.4 Possible Features <a name="1.2.4-possible-features" />
- Have a social media aspect for trainers to get recognized.

### 1.2.5 Excluded Features <a name="1.2.5-excluded-features" />
- Not a nutrition app. It is not supposet to recommend meal plans, diets, count calories or anything else along those lines.
- Not a video platform. Not intended to have recorded workout videos to follow.

<br>

### 1.3.1 Product Perspective <a name="1.3.1-product-perspective" /> <!-- Was this section never assigned to a team by the cop leads? (aaron) -->
This section details the relationship of the myJym app to products that are simmilar or related to it. 

#### 1.3.1.1 System Interfaces <a name="1.3.1.1-system-interfaces" />
- The application shall run on the most recent **iOS**. 
- The application shall run on the most recent **macOS**.  
- The application shall be connected to a database to store data.  
- The application shall be using google authentication. 

#### 1.3.1.2 User Interfaces <a name="1.3.1.2-user-interfaces" />
* The application shall have a **GUI**.
    - The GUI shall contain interactive buttons. 
    - The GUI shall contain an onscreen keyboard. 
    - The GUI shall contain a built-in messaging system. 
    - The GUI shall contain a sign-in page. 
    - The GUI shall contain a log in menu. 
    - The GUI shall contain interactive forms. 
    - The GUI shall contain a navigation bar. 
    - The GUI shall contain a search bar. 
    - The GUI shall contain a settings page. 
    - The GUI shall contain hyperlinks to workout videos. 
    - The GUI shall contain a find workout page. 
    - The GUI shall contain a create workout page. 
    - The GUI shall contain a my Gym page. 
    - The my Gym page shall have a search for gym option. 
    - The my Gym page shall have the option to see the home gym of user. 
    - The my Gym page shall have a map of where equipment is in the gym. 

#### 1.3.1.3 Hardware Interfaces <a name="1.3.1.3-hardware-interfaces" />
* Since the application will be run over the internet and cell service data, most of the hardware requirements will ensure the ios and android devices are able to connect to the internet. Since the **app** will be a fitness app, the hardware will require **users** to have the feature of location tracking for personal coach and exercise equipment tutorial videos. Preferably, iPhone 6 and later gen, for the purpose of app store update reasons. 

#### 1.3.1.4 Software Interfaces <a name="1.3.1.4-software-interfaces" />
* Specify the use of other required software products.
    - Operating System: iOS and Android devices. 
    - Linkage: Users shall be allowed to sign up myJam with their existing social media email accounts. (Facebook, Gmail, etc.)  

#### 1.3.1.5 Communications Interfaces <a name="1.3.1.5-communications-interfaces" />
* Communication interfaces shall include communication between the users.
* Communication interfaces shall include communication between the **trainers**, including a means of messaging within the app. 
*Communication shall include a means of communicating with myJym to receive help.

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
#### 1.3.4.13 External System Limitations <a name="1.3.4.13-external-system-limitations" />
The limitations of YouTube and whichever messaging service we decide to use will apply to the app.

## 1.4 Definitions: <a name="1.4-definitions" />
This is a comprehensive list of needed definitions used by the myJym application:
| Word   |  Definition |
| ------ | -------     |
| Account | An arrangement allowing a user personalized access to the myJym application, requiring the use of a username and password to access. |
| Admin | The people that run the app. They will connect the user's location to the gym and create QR codes that can be scanned by the user. |
| Android 11 | The minimum android version that will be required for the project. |
| Audit Functions | Functions of the application that allow for user feedback and error handling. |
| App | myJym mobile application. |
| Client | see *user* |
| Control Functions | The interface with which the user will interact with and control the app. |
| Criticality of the Application | Parts of the application have dependencies that can fail because of them. The most critical parts of the application.|
| The Database | A database that will store all information needed to run the application contraining the following tables: Admin, UserData, Trainer, and WorkOut. |
| Equipment | The machines at the student gym. |
| Email | A method of exchanging messages over the internet between electronic devices. |
| Embedded Video | Embedded Videos: Videos in applications that play a video inside of the app without having to go to the place containing the original video. |
| Error Message | A message stating that a condition is incorrect and requires that the condition be different. |
| Forms | Digital way to collect relevant information from the user. |
| Google | An American company that specializes in internet-related services and products. |
| Google Authentication Key | A key provided by Google to authenticate users. |
| GUI | GUI (Graphical User Interface) is a user interface that includes graphical elements, such as windows, icons, and buttons. The purpose is to appeal to the user using visuals. |
| Gym | A location with workout machines available. |
| Gym Hours | The hours that all partner gyms are open. |
| Hardware Limitations | Physical technological factors that might limit or slow the progress of the app and its construction. |
| Higher-Order Language Requirements | Knowledge of high-level programming languages such as Kotlin and Swift. |
| Home Page | The view which allows access to myTrainer, myWorkout, myVideos, and myGymMap views. |
| Interface | A point where two systems, subjects, organizations, etc. meet and interact. |
| Interfaces to other applications | The ability to interact with third party applications. |
| Invalid Credentials | Login credentials that do not match those associated with an account. |
| iOS | Internet Operating System or iPhone Operating System. It is the operating system used on Apple products, such as iPhone and iPad. |
| IOS 14.1 | The minimum IOS version that will be required for the project |
| Jared's Senior Project Class | A project class that the project sponsor will be taking at some point in the future. |
| Login Credentials | The username and password associated with an account. |
| Login Page | A view that requests that the user login. |
| macOS | The Macintosh Operating System is an operating system designed by Apple Inc. to be installed and operated on the Apple Macintosh series of computers. It is a (GUI) based OS that has since been released in multiple different versions. |
| Mnemonic | The device that uses patterns of letters, associations to assist users to remember a specific feature and its functionality. |
| Mobile Application (myJym) | The application that will be used to allow communication/digital connection between the user and personal trainer. It will also hold the data and information about the equipment available through QR codes. |
| Modal Income | Is the income amount that divides the population into two groups, half having the income above average and the other half below the average. |
| The myJym app | An application that provides a variety of features for the purpose of making the gym a more approachable experience. |
| Name | The name of the software’s feature. Generally, the name of the feature needs to be self-explanatory and easy to understand. |
| Parallel Operation | The ability of an application to run in parallel to other applications without getting in their way or being interrupted by them. |
| Partner Gyms | These are gyms that are partnered with the myJym app. |
| Password | A key word or phrase associated with an account. |
| Password Recovery Email | An email the gym-goer and/or trainer provides with account creation to recover their account if they forget their password. |
| Personal Trainer | Individuals who have earned certification that demonstrates they have achieved a level of competency for exercising safely and efficiently along with creating safe and effective exercise programs for those who have the medical clearance to participate. Personal trainers assist clients. |
| Personal Trainer Certificate | Individuals who have earned certification that demonstrates they have achieved a level of competency for exercising safely and efficiently along with creating safe and effective exercise programs for those who have the medical clearance to participate. Personal trainers can assist clients, and can do so while working in conjunction with the myJym app. |
| Physical/mental considerations | Considerations that pertain to the physical and mental health of the application. |
| Primary memory | Memory utilized by the app on the individual devices |
| Profile | A personalized account created by the user that will be associated with them and required to utilize the app. |
| QR Scanning | The ability of a mobile device to capture QR codes in their camera and then open the associated links. |
| Quality Requirements | The reliability of the application, as well as the other quality metrics that represent how well it fulfills its tasks. |
| Regulatory Requirements and Policies | Application requirements that need to comply with legal regulations and policies. |
| Safety and Security Considerations | Keeping the user’s physical and personal safety in mind, including sensitive or confidential information |
| Secondary memory | removable or external memory used by the individual devices. |
| Signal Handshake Protocols | How the app interacts securely with other applications and the internet. |
| Source | A specific reference for the research and citation purpose to avoid plagiarism. |
| Specification number | For the purpose of organization feature within the SRS documentation. |
| The System | The backend code that processes the server requests to send or return data as requested by the server through the user's requests. |
| Trainers | see *Personal Trainer* |
| Trainee | see *user* | 
| User | A person that uses the myJym app along with help from a personal trainer to progress with their training. |
| The UserData Database Table | A table in the database that contains user information, such as: username, password, weight, height, goals, W/O_Plan, email, and user_gym. |
| Username | A unique name identifying an account. |
| Version number | A set of unique numbers that are assigned to a specific release of a software project. In this case, it will be myJym version 1.0.0. |
| Working camera | camera capable of taking clear photos. |
| Workout Plan | A set of exercises, times, and practices a user will complete that are displayed in the application. This can be completed individually or with a personal trainer. |

## 3.4 Homepage <a name="3.4-homepage" />

## 3.5 Login Page <a name="3.5-login-page" />