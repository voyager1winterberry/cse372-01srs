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
* [3.1 My Trainer](#3.1-my-trainer)
    * [3.1.1 External Interfaces](#3.1.1-external-interfaces)
        * [3.1.1.1 Google Authentication](#3.1.1.1-google-authentication)
    * [3.1.2 Functions](#3.1.2-functions)
        * [3.1.2.1 myJym](#3.1.2.1-myJym)
        * [3.1.2.2 My Trainer](#3.1.2.2-my-trainer)
        * [3.1.2.3-view-trainer-profile](#3.1.2.3-view-trainer-profile)
        * [3.1.2.4 Edit Profile](#3.1.2.4-edit-profile)
        * [3.1.2.5 Search Trainer](#3.1.2.5-search-trainer)
        * [3.1.2.6 Message Trainer](#3.1.2.6-message-trainer)
        * [3.1.2.7 Message Users](#3.1.2.7-message-users)
    * [3.1.3 Usability Requirements](#3.1.3-usability-requirements)
    * [3.1.4 Performance Requirements](#3.1.4-performance-requirements)
    * [3.1.5 Logical Database Requirements](#3.1.5-logical-database-requirements)
        * [3.1.5.1 Types of information used by various functions](#3.1.5.1-types-of-information-used-by-various-functions)
        * [3.1.5.2 Frequency of use](#3.1.5.2-frequency-of-use)
        * [3.1.5.3 Accessing Capabilities](#3.1.5.3-accessing-capabilities)
        * [3.1.5.4 Data entities and their relationships](#3.1.5.4-data-entities-and-their-relationships)
        * [3.1.5.5 Integrity Constraints](#3.1.5.5-integrity-constraints)
        * [3.1.5.6 Security](#3.1.5.6-security)
        * [3.1.5.7 Data retention requirements](#3.1.5.7-data-retention-requirements)
    * [3.1.6 Design Constraints](#3.1.6-design-constraints)
    * [3.1.7 Software System Attributes](#software-system-attributes)
        * [3.1.7.1 Reliability](#3.1.7.1-reliability)
        * [3.1.7.2 Security](#3.1.7.2-security)
        * [3.1.7.3 Data Privacy](#3.1.7.3-data-privacy)
        * [3.1.7.4 Maintainability](#3.1.7.4-maintainability)
        * [3.1.7.5 Portability](#3.1.7.5-portability)
    * [3.1.8 Supporting Information](#3.1.8-supporting-information)
* [3.2 Gym Map](#3.2-gym-map)
    * [3.2.1 External Interfaces](#3.2.1-external-interfaces)
    * [3.2.2 Functions](#3.2.2-functions)
        * [3.2.2.1 Map Display](#3.2.2.1-map-display)
        * [3.2.2.2 Map Search Function](#3.2.2.2-map-search-function)
        * [3.2.2.3 Map Navigation](#3.2.2.3-map-navigation)
    * [3.2.3 Usability Requirements](#3.2.3-usability-requirements)
    * [3.2.4 Performance Requirements](#3.2.4-performance-requirements)
    * [3.2.5 Logical Database Requirements](#3.2.5-logical-database-requirements)
        * [3.2.5.1 Types of information used by various functions](#3.2.5.1-types-of-information-used-by-various-functions)
        * [3.2.5.2 Frequency of use](#3.2.5.2-frequency-of-use)
        * [3.2.5.3 Accessing Capabilities](#3.2.5.3-accessing-capabilities)
        * [3.2.5.4 Data entities and their relationships](#3.2.5.4-data-entities-and-their-relationships)
        * [3.2.5.5 Integrity Constraints](#3.2.5.5-integrity-constraints)
        * [3.2.5.6 Security](#3.2.5.6-security)
    * [3.2.6 Design Constraints](#3.2.6-design-constraints)
    * [3.2.7 Software System Attributes](#3.2.7-software-system-attributes)
        * [3.2.7.1 Reliability](#3.2.7.1-reliability)
        * [3.1.7.2 Security](#3.1.7.2-security)
* [3.5 Login & Homepage](#3.5-login-&-homepage)
    * [3.5.1 External Interfaces](#3.5.1-external-interfaces)
    * [3.5.2 Functions](#3.5.2-functions)
    * [3.5.3 Usability Requirements](#3.5.3-usability-requirements)
    * [3.5.4 Performance Requirements](#3.5.4-performance-requirements)
    * [3.5.5 Logical Database Requirements](#3.5.5-logical-database-requirements)
    * [3.5.6 Design Constraints](#3.5.6-design-constraints)
    * [3.5.7 Software System Attributes](#3.5.7-software-system-attributes)
        * [3.5.7.1 Reliability](#3.5.7.1-reliability)
        * [3.5.7.2 Availability](#3.5.7.2-availability)
        * [3.5.7.3 Security](#3.5.7.3-security)
        * [3.5.7.4 Portability](#3.5.7.4-portability)
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
* Communication shall include a means of communicating with myJym to receive help.

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
| User | A person that uses the myJym app along with help from a personal trainer to progress with their training |
| Version number | A set of unique numbers that are assigned to a specific release of a software project. In this case, it will be myJym version 1.0.0 |
| Working camera | camera capable of taking clear photos |
| Workout Plan | A set of exercises, times, and practices a user will complete that are displayed in the application. This can be completed individually or with a personal trainer |

<br>

## 3.1 My Trainer <a name="3.1-my-trainer" />
* ### 3.1.1 External Interfaces <a name="3.1.1-external-interfaces" />
    * #### 3.1.1.1 Google Authentication <a name="3.1.1.1-google-authentication" />
        * Google Authentication API shall be used by gymgoers and trainers to login to their accounts.
        * All users shall be able to login to their account using a google account.
        * All users shall be able to create an account using a google google account.

* ### 3.1.2 Functions <a name="3.1.2-functions" />
    * #### 3.1.2.1 myJym <a name="3.1.2.1-myJym>
        The myJym application will allow users to view the My Trainer page and receive system notifications.

        * The myJym application shall have a My Trainer page.
        * The myJym application shall send users Notifications. 
    * #### 3.1.2.1 Notifications <a name="3.1.2.1-notifications" />
        Notifications will allow users to receive notifications/alerts.

        * A notification will be created when a user sets a time for their workout.
        * A notification will be created when a user receives a message.
    * #### 3.1.2.2 My Trainer <a name="3.1.2.2-my-trainer" />
        My trainer will allow users to search for trainers, see trainer profiles, and message trainers.

        * My Trainer page shall display a Trainer Profile.
        * My Trainer page shall have a Search Trainer bar.

    * #### 3.1.2.3 View Trainer Profile <a name="3.1.2.3-view-trainer-profile" />
        The trainer profile will provide a viewable page for users with the trainer's photo, short bio, links to youtube channels, a follow button, a link to workouts created by the trainer, and a button to message the trainer.

        * Trainer profile shall be viewable by gymGoers.
        * Trainer profile shall display a picture of the trainer.
        * Trainer profile shall display a short biography of the trainer.
        * Trainer profile shall display a clickable link to the trainer’s youtube channel.
        * “Follow Trainer” shall be an option on the Trainer profile.
        * “View Workouts” shall be an option on the Trainer profile.
        * “Message Trainer” shall be an option on the Trainer profile.

    * #### 3.1.2.4 Edit Profile <a name="3.1.2.4-edit-profile" />
        The edit profile function will allow any user to make changes to their profile.
        * The Edit Profile page shall allow any user to edit their own picture.
        * The Edit Profile page shall allow any user to be able to edit their password.
        * The Edit Profile page shall allow any user to include a biography text-field.
        * The Edit Profile page shall allow any user to edit their account configuration.
        * The Edit Profile page shall allow any user to edit their personal youtube link.
        
    * #### 3.1.2.5 Search Trainer <a name="3.1.2.5-search-trainer" />
        Search trainer will allow users to view and input into a search bar to find trainers.
        * A search bar shall be viewable by the gymgoer.
        * A gymgoer shall be able to input into the search bar.
        * Search trainer shall enable the ability to find trainers matching input into search bar.

    * #### 3.1.2.6 Message Trainer <a name="3.1.2.6-message-trainer" />
        Message trainer will allow a user to communicate with a trainer.
        * Message Trainer shall give a user the ability to send messages to a trainer. 
        * Message Trainer shall create a chat between a user and a trainer. 
        * Message Trainer shall list messages in chronological order. 
        * Message Trainer shall be able to send the message. 
        * Messages Trainer shall be able to handle messages containing text.
        * Message Trainer shall be able to handle messages containing images.
        * Message Trainer shall be able to handle messages containing links.
        * Message Trainer shall be able to handle messages containing video.

    * #### 3.1.2.7 Message Users <a name="3.1.2.7-message-users" />
        Message Users shall allow the trainer to communicate with users. 
        * Message users shall give trainers the ability to send messages to users. 
        * Message users shall create a chat between trainer and users. 
        * Message users shall give trainers the ability to send messages to any number of chosen users. 
        * Message users shall list messages in chronological order. 
        * Message users shall be able to send the message. 

* ### 3.1.3 Usability Requirements <a name="3.1.3-usability-requirements" />
    * Ease of learning. The system shall be easy to learn for both novices and users with experience from similar systems. Users familiar with similar systems shall be able to create a new account and access the account within an average of 5 minutes.

    * Task efficiency. The system shall be efficient for the frequent user. Frequent users shall be given an option to be able to access their account without having to sign in each session. Tasks shall be able to be completed by the frequent user within an average of 25 seconds. 

    * Ease of remembering. The system shall be easy to remember for the casual user. Users experienced with this system shall be able to login to their account within an average of 1 minute. 

    * Understandability: The user shall understand what the system does. The system shall keep every option available on the user interface to similar sizes so that no option is larger than the others. A new user shall be able to navigate to any desired option within an average of 30 seconds. A total of 99% of users shall be able to perform any given task. 

    * Subjective satisfaction. The user shall feel satisfied with the system. The system shall receive an average rating of 7 out of 10 by test groups, with 10 being the highest and 1 the lowest. 

    * Task failure. Task failure by the system shall be kept to an absolute minimum. Task failure shall be limited to at most, .2 per user.  

    * Requirements to undo. A safe environment shall be incorporated into the system where users are able to try things and undo them. The ability to undo should be incorporated into any part of the system that stores information, or task.

    * Accessibility. The system will be created with elements that ensure that it is accessible by the widest range of people as possible. These elements include but are not limited to: color, text, complexity, and exclusivity. 

* ### 3.1.4 Performance Requirements <a name="3.1.4-performance-requirements" />
    * The mytrainer page shall display views after a predetermined time.
    * The trainer shall receive messages after a predetermined time.
    * The trainer shall compose messages after a predetermined time.
    * Notifications for the trainer shall be received after a predetermined time.
    * 90% of trainer profiles shall be loaded up in less than 5 s.
    * 95% of trainer search results shall load up in 1 s.
    * Trainer workout videos shall be processed in less than 5 s using hyperlinks.
    * 90% of setting trainer availability info shall be processed in 1 s.

* ### 3.1.5 Logical Database Requirements <a name="3.1.5-logical-database-requirements" />
    * #### 3.1.5.1 Types of information used by various functions <a name="3.1.5.1-types-of-information-used-by-various-functions" />
        * MyTrainer shall store a trainers first name
        * MyTrainer shall store a trainer’s last name.
        * MyTrainer shall store a trainer’s email.
        * The system shall create a trainer_ID for each trainer.
        * The system shall create a personal key for each trainer.

    * #### 3.1.5.2 Frequency of use <a name="3.1.5.2-frequency-of-use" />
        * Email data types shall be used for a single account.
        * Primary keys shall be used on a single account.

    * #### 3.1.5.3 Accessing Capabilities <a name="3.1.5.3-accessing-capabilities" />
	    * Trainers shall have access to UserData first_name.
	    * Trainers shall have access to UserData last_name.
	    * Trainers shall have access to UserData goals.
	    * Trainers shall have access to UserData W/O_plan.
	    * Trainers shall have access to UserData gym.

    * #### 3.1.5.4 Data entities and their relationships <a name="3.1.5.4-data-entities-and-their-relationships" />
        * MyTrainer shall have a data type for first_name.
        * MyTrainer shall have a data type for last_name
        * MyTrainer shall have a data type for email.
        * MyTrainer shall have a data type for trainer_ID.
        * MyTrainer shall have a personal key for each trainer.

    * #### 3.1.5.5 Integrity Constraints <a name="3.1.5.5-integrity-constraints" />
	    * Data entries shall be possible entries.
	    * Data entries shall be verified by the system.
	    * Data entries shall have valid references.
	    * Trainers shall have unique primary keys.
	    * The system shall have entity integrity.

    * #### 3.1.5.6 Security <a name="3.1.5.6-security" />
	    * Trainer accounts shall utilize google sign-in to access their account.
	    * Trainers shall only have one account.
	    * Admin accounts shall have access to all accounts

    * #### 3.1.5.7 Data retention requirements <a name="3.1.5.7-data-retention-requirements" />
		* Data shall be retained for 2(two) years.
		* Data shall be retained in a database.
		* Trainer accounts shall be accessible for 2(two) years after inactivity.

* ### 3.1.6 Design Constraints
    ![Design Constraints Image](Images/DesignConstraintsImage.png)

* ### 3.1.7 Software System Attributes <a name="3.1.7-software-system-attributes" />
    * #### 3.1.7.1 Reliability <a name="3.1.7.1-reliability" />
        * Applications shall not have errors within the codes to cause applications to close or crash. 
        * There will be functions within the software that performs verifications to notice errors before the application break or force closes.  
        * The system shall verify the information that matches from the server and the application. 

    * #### 3.1.7.2 Security <a name="3.1.7.2-security" />
        * Password Protection and Encryption 
        * User account creation 
            * User information shall be available to users and those have access. 
            * User shall be required to provide email, and password for the purpose of account creation. 

        * #### 3.1.7.3 Data Privacy <a name="3.1.7.3-data-privacy" />
            * User’s data shall be hidden from all other users and parties. 
            * Login Information 
            * Creating an account shall be safe and secure. 
            * All users shall be allowed to login securely. 
            * Once a user logs out from the account, all user information shall be removed from the login screen. 
        * #### 3.1.7.4 Maintainability <a name="3.1.7.4-maintainability" />
            * Users shall be allowed to report to the administration team if they forget their password, and need to have a reset password email sent to their personal email that has been registered on their myJym account. 
            * An automatic email shall be sent to the user's email address to allow the user to reset their password. 
        * #### 3.1.7.5 Portability
            * System Database shall store user information. 
            * myJym application shall run on both Android and iOS mobile interface.

* ### 3.1.8 Supporting Information <a name="3.1.8-supporting-information" />
    ![Design Constraints Image](Images/SupportingInfoImage.png)

    *  Description of the problems to be solved by the software:
    A problem that this software will solve is to give users the ability to connect with trainers.Trainers will be able to provide information to users about workouts and feedback on workout plans. Trainers will be able to access user data to be able to help them choose workout plans and give them the motivation to meet their goals.

## 3.2 Gym Map <a name="3.2-gym-map" /> <!-- Team 2 -->
The map of the gym used by the MyJym application and it's requirements will be detailed in this section.
* ### 3.2.1 External Interfaces <a name="3.2.1-external-interfaces" />
    * The map shall utilize the System Database to obtain needed information for the map generation.
    * The map search bar shall obtain user data from the System Database.
* ### 3.2.2 Functions <a name="3.2.2-functions" />
Functions of the gym map and it's associated features are detailed below:
* #### 3.2.2.1 Map Display <a name="3.2.2.1-map-display" />
    * The map shall organize gym equipment according to a JSON file detailing their locations.
    * The map shall organize gym services according to a JSON file detailing their locations.
    * When an abnormal state is encountered the map shall stop and refresh.
    * The map shall support modification to facility locations by a system administrator.
    * A simple tutorial of using the map shall display the first time a user opens to that view.
* #### 3.2.2.2 Map Search Function <a name="3.2.2.2-map-search-function" />
    * The map search bar shall perform validation on inputs matching them to gym functions.
    * The map shall provide a search bar used to locate gym functions.
    * The map search bar shall be a modeless interface not restricting user input to other parts of the application.
    * Facilities in the gym shall be searchable by name through the map search bar.
* #### 3.2.2.3 Map Navigation <a name="3.2.2.3-map-navigation" />
    * The map shall be scrollable edge to edge responding to user input.
    * The map shall support zooming detecting when a zoom request is made by the user.
    * Gym function icons shall be interactable to view options related that function.
* ### 3.2.3 Usability Requirements
    * Ease of learning. The map shall be intuive allowing the user to easily form a mental model of its workings.
    * Task efficiency. The map shall facilitate a user quickly identifying where they should be in the gym to complete their desired activity.
    * Ease of remembering. The map shall utilize simple command formats to ensure users are capable creating a mental model of the map functionalities. 
    * Understandability: The user shall understand the purpose of the map. Map features shall use formats akin to those found on simmilar mobile applications. New users will be greeted by a tutorial upon first entering the map view.
    * Task failure. When encountering a task failure the map shall stop its operation and refresh.
    * Accessibility. Map iconography shall be created based upon commonly recognized symbols. 
* ### 3.2.4 Performance Requirements
    * The map shall prioritize loading of graphical display elements prior to lower priority tasks.
    * The map search functionality shall return results in higher performant step timing than** O**(n log n).
    * The map shall allow interaction with elements after a perdetmined time post loading.
* ### 3.2.5 Logical Database Requirements
The data used by the gym map and it's state will be detailed here.
* #### 3.2.5.1 Types of information used by various functions
    * The map shall store the icons for the map as a JSON data construct.
    * The map shall store the possible search results for the map search in the System Database as a table.
* #### 3.2.5.2 Frequency of use
    * Map icons shall be loaded into memory when the view is selected.
    * Map icons shall be discharged from memory when the view is released by the operating system.
* #### 3.2.5.3 Accessing Capabilities <a name="3.2.5.3-accessing-capabilities" />
    * The map shall have access to the schema of equipment in the gym.
    * The map shall have access to the schema for user data.
* #### 3.2.5.4 Data entities and their relationships <a name="3.2.5.4-data-entities-and-their-relationships" />
    * The map shall handle storing of icons as tables in the database.
    * The map shall handle storing of possible search results as key-value pairs.
* #### 3.2.5.5 Integrity Constraints <a name="3.2.5.5-integrity-constraints" />
    * Map icons shall be possible entries.
    * Map entries shall have valid references.
    * Primary keys shall be used to distinguish unique data for the map.
* #### 3.2.5.6 Security <a name="3.2.5.6-security" />
    * Map data shalled be transmitted via end-to-end encryption.
* ### 3.2.6 Design Constraints <a name="3.2.6-design-constraints" />
    * The interactable map features shall provide sufficient **Pixels Per Inch** that the average human is able to cleanly select them.
* ### 3.2.7 Software System Attributes <a name="3.2.7-software-system-attributes">
The myGym map will hold to certain reliability and security guidelines which are detailed below:
* #### 3.2.7.1 Reliability <a name="3.2.7.1-reliability" />
    * The maps delivered to the user on MyJym shall deliver accurate data based on the information entered by the admin to the database.
    * MyJym map data shall be available throughout the time that the user uses MyJym.
* #### 3.2.7.2 Security <a name="3.2.7.2-security" />
    * The map shall not be editable by any unauthorized party. 


## 3.5 Login & Homepage <a name="3.5-login-&-homepage" /> <!-- 3.5 is Team 5's work -->
* ### 3.5.1 External Interfaces <a name="3.5.1-external-interfaces" />
    * The login page shall provide the ability to login through Google.
    * The system shall send an automated password recovery email to the user on request
* ### 3.5.2 Functions <a name="3.5.2-functions" />
    * The home page shall provide access to myTrainer.
    * The home page shall provide access to myWorkouts.
    * The home page shall provide access to myVideos.
    * The home page shall provide access to myGymMap.
    * The login page shall provide the user with the ability to recover a lost password.
    * The login page shall provide the user with the ability to create an account.
    * The login page shall display an error message when invalid credentials are submitted.
    * The system shall check the login credentials against the database.
* ### 3.5.3 Usability Requirements <a name="3.5.3-usability-requirements" />
    * The login page shall inform the user of password requirements.
    * The login page shall allow the user to enter login credentials.
* ### 3.5.4 Performance Requirements <a name="3.5.4-performance-requirements" />
    * The system shall have the ability to process login credentials.
* ### 3.5.5 Logical Database Requirements <a name="3.5.5-logical-database-requirements" />
    * The UserData database table shall have a Google authentication key from the Google third party login.
    * The UserData database table shall store usernames.
    * The UserData database table shall store the passwords.
    * The database shall be accessed by the login page when user credentials are submitted through the login page.
    * The database shall keep the login credentials of users confidential.
* ### 3.5.6 Design Constraints <a name="3.5.6-design-constraints" />
    * The myJym app shall be completed in its entirety by the end of Jared's Senior Project class.
    * The budget for the myJym app shall be $0.00.
* ### 3.5.7 Software System Attributes <a name="3.5.7-software-system-attributes" />
    * #### 3.5.7.1 Reliability <a name="3.5.7.1-reliability" />
        * The app shall require the compliance of personal trainers.
        * The app shall require an administrator.
    * #### 3.5.7.2 Availability <a name="3.5.7.2-availability" />
        * The myJym app shall be available during all gym hours.
    * #### 3.5.7.3 Security <a name="3.5.7.3-security" />
        * The system shall encrypt user accounts.
        * The system shall use a protocol to secure online communications.
    * #### 3.5.7.4 Portability <a name="3.5.7.4-portability" />
        * * The application shall be built with a programming language that can be ported to both iOS and Android.

<br>

## References <a name="references" />
* [1] S.R.O., Eccam. “Example Software Requirements Specification (SRS) | ReqView Documentation.” ReqView, 2018, www.reqview.com/doc/iso-iec-ieee-29148-srs-example.

* [2] IIEEE, " 29148-2018 - ISO/IEC/IEEE International Standard - Systems and software engineering -- Life cycle processes -- Requirements engineering " pp. 56-87, Jul. 2018. [Online] Available: https://ieeexplore-ieee-org.byui.idm.oclc.org/document/8559686 

* [3] “Macintosh Operating System (Mac OS).” Techopedia, techopedia, 2012, www.techopedia.com/definition/2639/macintosh-operating-system-mac-os.





