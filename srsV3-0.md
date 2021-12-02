myJym Software Requirements Specification
=========================================
Project Sponsor: Jared Barnes
<br>
Project Owner: Brother Clements
=========================================
Date: 11/20/21
=========================================
<br><br><br>

| Authors:     |                  |                   |                         |                  |
|-------------------|------------------|-------------------|-------------------------|------------------|
| Ales, Grant       | Collins, Daniel   | Crowson, Avery    | Dean, Joshua            | Elzinga, Jacob   |
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
    * [1.2.4 Possible Features](#1.2.4-excluded-features)
* [1.3](#1.3)
    * [1.3.1 Product Perspective](#1.3.1-product-perspective)
        * [1.3.1.1 System Interfaces](#1.3.1.1-system-interfaces)
        * [1.3.1.2 User Interfaces](#1.3.1.2-user-interfaces)
        * [1.3.1.3 Hardware Interfaces](#1.3.1.3-hardware-interfaces)
        * [1.3.1.4 Software Interfaces](#1.3.1.4-software-interfaces)
        * [1.3.2 Product Functions](#1.3.2-product-functions)
            * [1.3.2.1 User Profiles](#1.3.2.1-user-profiles)
            * [1.3.2.2 User Scenarios](#1.3.2.2-user-scenarios)
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
        * [3.1.2.2 Notifications](#3.1.2.2-notifications)
        * [3.1.2.3 My Trainer](#3.1.2.3-my-trainer)
        * [3.1.2.4 View Trainer Profile](#3.1.2.4-view-trainer-profile)
        * [3.1.2.5 Edit Profile](#3.1.2.5-edit-profile)
        * [3.1.2.6 Search Trainer](#3.1.2.6-search-trainer)
        * [3.1.2.7 Message Trainer](#3.1.2.7-message-trainer)
        * [3.1.2.8 Message Users](#3.1.2.8-message-users)
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
    * [3.1.7 Software System Attributes](#3.1.7-software-system-attributes)
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
        * [3.2.7.2 Security](#3.2.7.2-security)
* [3.3 MyJym Videos](#3.3-myjym-videos)
    * [3.3.1 External Interfaces Specification](#3.3.1-external-interfaces-specification)
        * [3.3.1.1 Database](#3.3.1.1-database)
        * [3.3.1.2 Video Streaming](#3.3.1.2-video-streaming)	
    * [3.3.2 Functions](#3.3.2-functions)
        * [3.3.2.1 My Video](#3.3.2.1-my-video)
    * [3.3.3 Usability Requirement](#3.3.3-usability-requirement)	
    * [3.3.4 Performance requirements](#3.3.4-performance-requirements)
    * [3.3.5 Logical Database Requirements](#3.3.5-logical-database-requirements)
    * [3.3.6 Design Constraints](#3.3.6-design-constraints)
    * [3.3.7 Software System Attributes](#3.3.7-software-system-attributes)
        * [3.3.7.1 Reliability](#3.3.7.1-reliability)
        * [3.3.7.2 Security](#3.3.7.2-security)
        * [3.3.7.3 Maintainability](#3.3.7.3-maintainability)
* [3.4 Login & Homepage](#3.4-login-&-homepage)
    * [3.4.1 External Interfaces](#3.4.1-external-interfaces)
    * [3.4.2 Functions](#3.4.2-functions)
    * [3.4.3 Usability Requirements](#3.4.3-usability-requirements)
    * [3.4.4 Performance Requirements](#3.4.4-performance-requirements)
    * [3.4.5 Logical Database Requirements](#3.4.5-logical-database-requirements)
    * [3.4.6 Design Constraints](#3.4.6-design-constraints)
    * [3.4.7 Software System Attributes](#3.4.7-software-system-attributes)
        * [3.4.7.1 Reliability](#3.4.7.1-reliability)
        * [3.4.7.2 Availability](#3.4.7.2-availability)
        * [3.4.7.3 Security](#3.4.7.3-security)
        * [3.4.7.4 Portability](#3.4.7.4-portability)
* [3.5 My Workout](#3.5-my-workout)
    * [3.5.1 External Interface](#3.5.1-external-interface)
        * [3.5.1.1 Database](#3.5.1.1-database)
        * [3.5.1.2 YouTube](#3.5.1.2-Youtube)
    * [3.5.2 Functions](#3.5.2-functions)
        * [3.5.2.1 Create Workout](#3.5.2.1-create-workout)
        * [3.5.2.2 Find Workout](#3.5.2.2-find-workout)
        * [3.5.2.3 Saved Workout](#3.5.2.3-saved-workout)
        * [3.5.2.4 Workout in Progress Page](#3.5.2.4-workout-in-progress-page)
    * [3.5.3 Usability Requirements](#3.5.3-usability-requirements)
    * [3.5.4 Performance Requiremnts](#3.5.4-performance-requirements)
    * [3.5.5 Logical Database Requirements](#3.5.5-logical-database-requirements)
    * [3.5.6 Design Constraints](#3.5.6-design-constraints)
    * [3.5.7 Software System Attributes](#3.5.7-software-system-attributes)
        * [3.5.7.1 Reliability](#3.5.7.1-reliability)
        * [3.5.7.2 Security](#3.5.7.2-security)
        * [3.5.7.3 Maintainability](#3.5.7.3-maintainability)
* [References](#references)
<br><hr /><br>

## 1.1 Purpose <a name="1.1-purpose" />
The myJym app is to help people at all levels of experience feel confident using gym equipment.  It also focuses on connecting users to personal trainers.  Additional features include work out regiments, gym maps, and ability to track fitness goals.

<br>

## 1.2 Scope <a name="1.2-scope" />
The scope outlines what will and will not be included in the project.

### 1.2.1 Products to be Produced <a name="1.2.1-proucts-to-be-produced" />
The products to be produced is all the main programs that will be needed to make the product work.
The myJym app will utilize:
- server
- database
- mobile myJym app
- web based myJym app

### 1.2.2 What Will the Software Product Do <a name="1.2.2-what-will-the-software-product-do" />
This is a description of what the product to be produced will do.
- The product, the myJym app, will assist users in creating workouts, working out and connecting with trainers.

### 1.2.3 Included Core Features <a name="1.2.3-included-core-features" />
This is a table outlining the main features of the app with a brief description of what the feature is.
<!-- Suggested format for updating features (Aaron) -->
| Feature | Description                                                          |
|---------|----------------------------------------------------------------------|
| Login Page | The page that allows users to login with their credentials.       | 
| Home Page | The first page that users will see after loging into the app.      |
| My Trainers | Page to mediate interaction between trainers and gym goers.      |
| My Workouts | Page that allows creation and execution of workouts.             |
| My Videos | Page that has a list of links to all videos used by the app.       |
| Gym Map | A map showing the location of equipment, services, and gym features. |

<!-- login page (external interface) /these were discussed in class and should be added to core features/ -->
<!-- home page MyJym (external interface) sub interfaces -->
   <!-- my trainer, my workout, my videos, gym map, -->

### 1.2.4 Excluded Features <a name="1.2.4-excluded-features" />
This is a table outlining what feautures are outside the scope of this project with a breif description of the feature.
| Feature | Description                                                          |
|---------|----------------------------------------------------------------------|
| Nutrition Information | Not intended to recommend meal plans, diets, count calories or anything else similar. | 
| Video Platform | Not intended to have recorded workout videos to follow. |

<br>

### 1.3.1 Product Perspective <a name="1.3.1-product-perspective" /> <!-- Was this section never assigned to a team by the cop leads? (aaron) -->
This section details the relationship of the myJym app to products that are simmilar or related to it. 

#### 1.3.1.1 System Interfaces <a name="1.3.1.1-system-interfaces" />
The system interfaces will be the systems that the application will be running on. The list below will be the systems used for the application. 

* The myJym app will run on mobile services. 
* The myJym app will run on web services. 
* The myJym app will connect to google authentication for login credentials. 

#### 1.3.1.2 User Interfaces <a name="1.3.1.2-user-interfaces" />
The user interfaces will be the functionality of the app. This functionality is what the user will see when in the app.  

* The myJym app will include a built-in messaging system to allow communication between users. 

* The myJym app will include a sign-in page and a login page for the user. 

* The myJym app will use the current systems keyboard to allow user input.  

* The myJym app will have interactive buttons that will do different things according to the buttons pressed. These buttons will change the current page, modify workouts, and work with myJym’s built-in messaging. 

* The myJym app will have a search bar that will allow the user to search for anything regarding the application such as different workouts. The search bar will allow for quick searches for the user's needs. 

* The myJym app will have a settings page which will have everything in the page that the user can see and change in the app. Settings will include the user's profile and trainers they work with. 

* The myJym app will have a workout page which will allow the user to create, delete, modify, and save workouts. 

* The mJym app will have a myGym page which will find the gym you will be going to and a built-in map of that gym.

#### 1.3.1.3 Hardware Interfaces <a name="1.3.1.3-hardware-interfaces" />
A hardware interface specifies the plugs, sockets, cables and electrical signals that pass through each line between the CPU and a peripheral device or communications network. 

* Since the application will be run over the internet and cell service data, most of the hardware requirements will ensure the ios and android devices are able to connect to the internet. Since myJym will be a fitness app, features of myJym shall require users to have the feature of location tracking for personal coach and exercise equipment tutorial videos on their mobile device. Preferably, iPhone 6 and later gen, for the purpose of app store update reasons. The version of the iOS system shall be 15.1.1, and android system shall be 11.  

#### 1.3.1.4 Software Interfaces <a name="1.3.1.4-software-interfaces" />
Software interfaces (programming interfaces) are the languages, codes and messages that programs use to communicate with each other and to the hardware. Examples are the Windows, Mac and Linux operating systems, SMTP email, IP network protocols and the software drivers that activate the peripheral devices. 

* Specify the use of other required software products.  
    - Operating System: iOS and Android devices, and desktop applications, and the content will be operating within the mobile application.  

    - Linkage: Users shall be allowed to sign up myJym with their existing personal email address to login to their accounts.   

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
The system must be available in the following formats. 
* Android 
* IOS 
* Web application 

#### 1.3.1.9 Interfaces with Services <a name="1.3.1.9-interfaces-with-services" />
The different services that the system will interact with. 
* YouTube links to the various workout videos must be accessible 
* The server will connect accounts to the main database to access the account information 

### 1.3.2 Product Functions <a name="1.3.2-product-functions" />
For the product functions of the myJym application the following User Profiles and User Scenarios will be as follows:

#### 1.3.2.1 User Profiles <a name="1.3.2.1-user-profiles" />
The following User Profiles define the target demographics for the myJym application:
 - A returned missionary attending BYU-Idaho, in their early twenties, has a busy schedule with work and a heavy course load.
 - A student in their junior year, also attending BYU-Idaho, in their early twenties, they enjoy playing football with their friends and family.
 - A new freshman, halfway through the semester wanting to lose weight, but unsure of where to start.
 - A couple that likes to spend time together by playing sports and working out.
The application will be available to all age groups and demographics, however these groups will serve as the focus the application.


#### 1.3.2.2 User Scenarios <a name="1.3.2.2-user-scenarios" />
The following User Scenarios serve to describe the use cases that have been elicited to be applicable to the product functions of the myJym application:
- Only being able to attend the gym in the early morning, with no previous time to set a workout routine or research workout machines.
- Brand new to exercising, there is a fear of feeling inadequate and confused in front of others, and a desire to be helped in a discreet way.
- Getting burnt out with their current workout routine, and desiring new machines and techniques that can help them develop new routines.
- A student desires additional experience with a variety of exercises including strength training, endurance training, weight loss, and cardio training to be able to better meet their fitness goals.

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
| Client | see *trainee* |
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
| Trainee | A gym-goer being trained by a personal trainer. | 
| User | A gym-goer and/or a trainer. |
| User-admin | User that acts as an administrator. |
| User-trainer | User who instructs gym-goers. |
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
    * #### 3.1.2.1 myJym <a name="3.1.2.1-myJym" />
        The myJym application will allow users to view the My Trainer page and receive system notifications.

        * The myJym application shall have a My Trainer page.
        * The myJym application shall send users Notifications. 
    * #### 3.1.2.2 Notifications <a name="3.1.2.2-notifications" />
        Notifications will allow users to receive notifications/alerts.

        * A notification will be created when a user sets a time for their workout.
        * A notification will be created when a user receives a message.
    * #### 3.1.2.3 My Trainer <a name="3.1.2.3-my-trainer" />
        My trainer will allow users to search for trainers, see trainer profiles, and message trainers.

        * My Trainer page shall display a Trainer Profile.
        * My Trainer page shall have a Search Trainer bar.

    * #### 3.1.2.4 View Trainer Profile <a name="3.1.2.4-view-trainer-profile" />
        The trainer profile will provide a viewable page for users with the trainer's photo, short bio, links to youtube channels, a follow button, a link to workouts created by the trainer, and a button to message the trainer.

        * Trainer profile shall be viewable by gymGoers.
        * Trainer profile shall display a picture of the trainer.
        * Trainer profile shall display a short biography of the trainer.
        * Trainer profile shall display a clickable link to the trainer’s youtube channel.
        * “Follow Trainer” shall be an option on the Trainer profile.
        * “View Workouts” shall be an option on the Trainer profile.
        * “Message Trainer” shall be an option on the Trainer profile.

    * #### 3.1.2.5 Edit Profile <a name="3.1.2.5-edit-profile" />
        The edit profile function will allow any user to make changes to their profile.
        * The Edit Profile page shall allow any user to edit their own picture.
        * The Edit Profile page shall allow any user to be able to edit their password.
        * The Edit Profile page shall allow any user to include a biography text-field.
        * The Edit Profile page shall allow any user to edit their account configuration.
        * The Edit Profile page shall allow any user to edit their personal youtube link.
        
    * #### 3.1.2.6 Search Trainer <a name="3.1.2.6-search-trainer" />
        Search trainer will allow users to view and input into a search bar to find trainers.
        * A search bar shall be viewable by the gymgoer.
        * A gymgoer shall be able to input into the search bar.
        * Search trainer shall enable the ability to find trainers matching input into search bar.

    * #### 3.1.2.7 Message Trainer <a name="3.1.2.7-message-trainer" />
        Message trainer will allow a user to communicate with a trainer.
        * Message Trainer shall give a user the ability to send messages to a trainer. 
        * Message Trainer shall create a chat between a user and a trainer. 
        * Message Trainer shall list messages in chronological order. 
        * Message Trainer shall be able to send the message. 
        * Messages Trainer shall be able to handle messages containing text.
        * Message Trainer shall be able to handle messages containing images.
        * Message Trainer shall be able to handle messages containing links.
        * Message Trainer shall be able to handle messages containing video.

    * #### 3.1.2.8 Message Users <a name="3.1.2.8-message-users" />
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

* ### 3.1.6 Design Constraints <a name="3.1.6-design-constraints" />
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
        * #### 3.1.7.5 Portability <a name="3.1.7.5-portability" />
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
* ### 3.2.3 Usability Requirements <a name="3.2.3-usability-requirements" />
    * Ease of learning. The map shall be intuive allowing the user to easily form a mental model of its workings.
    * Task efficiency. The map shall facilitate a user quickly identifying where they should be in the gym to complete their desired activity.
    * Ease of remembering. The map shall utilize simple command formats to ensure users are capable creating a mental model of the map functionalities. 
    * Understandability: The user shall understand the purpose of the map. Map features shall use formats akin to those found on simmilar mobile applications. New users will be greeted by a tutorial upon first entering the map view.
    * Task failure. When encountering a task failure the map shall stop its operation and refresh.
    * Accessibility. Map iconography shall be created based upon commonly recognized symbols. 
* ### 3.2.4 Performance Requirements <a name="3.2.4-performance-requirements" />
    * The map shall prioritize loading of graphical display elements prior to lower priority tasks.
    * The map search functionality shall return results in higher performant step timing than** O**(n log n).
    * The map shall allow interaction with elements after a perdetmined time post loading.
* ### 3.2.5 Logical Database Requirements <a name="3.2.5-logical-database-requirements" />
The data used by the gym map and it's state will be detailed here.
* #### 3.2.5.1 Types of information used by various functions <a name="3.2.5.1-types-of-information-used-by-various-functions" />
    * The map shall store the icons for the map as a JSON data construct.
    * The map shall store the possible search results for the map search in the System Database as a table.
* #### 3.2.5.2 Frequency of use <a name="3.2.5.2-frequency-of-use" />
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

	
## 3.3 MyJym Videos  <a name="3.3-myjym-videos" />

This Specification section explains the MyJym application in detail, the specification goes over eight categories. Such as external interfaces, functionality, usability, performance, database, design constraints, and software system attribute requirements for the MyJym application. 

### 3.3.1 External Interfaces Specification <a name="3.3.1-external-interfaces-specifications" />
#### 3.3.1.1 Database <a name="3.3.1.1-database" />
* The MyJym application will use a database to store workout information, Specific columns and requirements of the database can be found in section 3.5.

* The database shall store workout title

* The database shall store workout video links

* The database shall store workout description

* The database shall store the image links
 
#### 3.3.1.2 Video Streaming <a name="3.3.1.2-video-streaming" />
* The API for a video streaming website will be used to share videos on workout techniques and forms, and how to use gym exercise equipment. This will be used according to the product owner and stakeholder’s decisions.

* Gymgoers shall have the ability to access workout videos
	
### 3.3.2 Functions <a name="3.3.2-functions" />
* This section is responsible for explaining MyJym’s ability to perform to the User’s standard. These functions are split up into sections that explain the procedure of the MyJym application in how to perform or complete tasks.

#### 3.3.2.1 My Video <a name="3.3.2.1-my-video" />
* The purpose of the following section provides the capabilities of the video page. This represents an individual user for the MyJym application.
* The My Video page shall display a workout title.

* The My Video page shall display an equipment name.

* The My Video page shall display a workout video.

* The My Video page shall provide a save video button.

### 3.3.3 Usability Requirement <a name="3.3.3-usability-requirement" />
* User shall be able to save a selected video
* User shall be able to view the workout video
* User shall be able to view saved videos
	
### 3.3.4 Performance requirements <a name="3.3.4-performance-requirements" />
For the MyJym application to meet performance standards, there are specific requirements that are needed to be met, specified below.
* User shall be able to save a selected video
* The user shall only be able to save one video link per exercise.
* The My Video page shall support a configurable amount of workouts
* The My Video page shall support a configurable amount of workouts videos

### 3.3.5 Logical Database Requirements <a name="3.3.5-logical-database-requirements" />
The MyJym database shall store all the tables that are necessary for storing information required by the application.
* The workout table shall contain an exercise title column
* The workout table shall contain a description column
* The workout table shall contain a video link column
* The workout table shall contain a workout id column that acts as a primary key

### 3.3.6 Design Constraints <a name="3.3.6-design-constraints" />
* The user shall only be able to save workout video

### 3.3.7 Software System Attributes <a name="3.3.7-software-system-attributes" />
#### 3.3.7.1 Reliability <a name="3.3.7.1-reliability" />
* The system shall exit immediately when a user finds an error.
* The app shall check that locally stored user information matches what is stored in a database.
#### 3.3.7.2 Security <a name="3.3.7.2-security" />
* The user shall only be able to add approved video links to an exercise.
#### 3.3.7.3 Maintainability <a name="3.3.7.3-maintainability" />
* App administrators shall be able to remove inappropriate content.

## 3.4 Login & Homepage <a name="3.4-login-&-homepage" /> <!-- 3.4 is Team 5's work -->
### 3.4.1 External Interfaces <a name="3.4.1-external-interfaces" />
***3.4.1.1*** The login page shall provide the ability to login through Google.<br>
***3.4.1.2*** The system shall send an automated password recovery email to the user on request
### 3.4.2 Functions <a name="3.4.2-functions" />
***3.4.2.1*** The home page shall provide access to myTrainer.<br>
***3.4.2.2*** The home page shall provide access to myWorkouts.<br>
***3.4.2.3*** The home page shall provide access to myVideos.<br>
***3.4.2.4*** The home page shall provide access to myGymMap.<br>
***3.4.2.5*** The login page shall provide the user with the ability to recover a lost password.<br>
***3.4.2.6*** The login page shall provide the user with the ability to create an account.<br>
***3.4.2.7*** The login page shall display an error message when invalid credentials are submitted.<br>
***3.4.2.8*** The system shall check the login credentials against the database.
### 3.4.3 Usability Requirements <a name="3.4.3-usability-requirements" />
#### 3.4.3.1 
The login page shall inform the user of password requirements.
#### 3.4.3.2 
The login page shall allow the user to enter login credentials.
### 3.4.4 Performance Requirements <a name="3.4.4-performance-requirements" />
#### 3.4.4.1
The system shall have the ability to process login credentials.
### 3.4.5 Logical Database Requirements <a name="3.4.5-logical-database-requirements" />
***3.4.5.1*** The UserData database table shall have a Google authentication key from the Google third party login.<br>
***3.4.5.2*** The UserData database table shall store usernames.<br>
***3.4.5.3*** The UserData database table shall store the passwords.<br>
***3.4.5.4*** The database shall be accessed by the login page when user credentials are submitted through the login page.
***3.4.5.5*** The database shall keep the login credentials of users confidential.
### 3.4.6 Design Constraints <a name="3.4.6-design-constraints" />
***3.4.6.1*** The myJym app shall be completed in its entirety by the end of Jared's Senior Project class.
***3.4.6.2*** The budget for the myJym app shall be $0.00.
### 3.4.7 Software System Attributes <a name="3.4.7-software-system-attributes" />
#### 3.4.7.1 Reliability <a name="3.4.7.1-reliability" />
        * The app shall require the compliance of personal trainers.
        * The app shall require an administrator.
    * #### 3.4.7.2 Availability <a name="3.4.7.2-availability" />
        * The myJym app shall be available during all gym hours.
    * #### 3.4.7.3 Security <a name="3.4.7.3-security" />
        * The system shall encrypt user accounts.
        * The system shall use a protocol to secure online communications.
    * #### 3.4.7.4 Portability <a name="3.4.7.4-portability" />
        * * The application shall be built with a programming language that can be ported to both iOS and Android.

<br>

## 3.5 My Workout <a name="3.5-my-workout" /> <!-- team 3 and 4's stuff-->
	
	
	
W.3.0.3.1 The workout function shall have the ability to let users create their own workouts.

W.3.0.3.2 The workout function shall have the ability to let users find premade workouts.

W.3.0.3.3 The workout function shall have the ability to let users view previously saved workouts.

<br>

### 3.5.1 External Interface <a name="3.5.1-external-interface" />
#### 3.5.1.1 Database <a name="3.5.1.1-database" />
* The database shall store workout **title**.
* The database shall store workout video links.
* The database shall store workout description.
* The database shall store workout **sets**.
* The database shall store workout **reps**.
* The database shall store workout **tags**.

#### 3.5.1.2 YouTube <a name="3.5.1.2-youtube" />

* The **API** for YouTube will be used to share videos on workout techniques and forms, and how to use gym exercise equipment. This will be used according to the product owner and stakeholder’s decisions.
* **Gymgoers** shall have the ability to access workout videos.
	
### 3.5.2 Functions <a name="3.5.2-functions" />
This section is responsible for explaining MyJym’s ability to perform to the User’s standard. These functions are split up into sections that explain the procedure of the MyJym application in how to perform or complete tasks.

#### 3.5.2.1 Create Workout <a name="3.5.2.1-create-workout" />
* The workout creation shall allow the **user** to specify a workout name.
* The workout creation shall allow the user to specify a muscle group to workout.
* The workout creation shall allow the user to specify an amount of **reps**.
* The workout creation shall allow the user to specify an amount of **sets**.
* The workout creation shall allow the user to embed a video link.

#### 3.5.2.2 Find Workout <a name="3.5.2.2-find-workout" />
* The find workout page shall have the ability to search by predetermined **tag**s.
* One of the tags that can be used to search by shall be **author**.
* One of the tags that can be used to search by shall be **name of workout**.
* One of the tags that can be used to search by shall be **length**.
* One of the tags that can be used to search by shall be **workout type**.
* One of the tags that can be used to search by shall be **difficulty**.
* One of the tags that can be used to search by shall be **equipment type**.
* One of the tags that can be used to search by shall be **muscle groups**.
* The user shall have the ability to save a workout they find to their saved workouts list.

#### 3.5.2.3 Saved Workout <a name="3.5.2.3-saved-workout" />
* The user shall have the option to edit the workout.
* Selecting edit workout shall redirect the user back to the create workout page with all the workout information filled in.
* The user shall have the option to immediatly start the workout.
* Selecting start workout shall redirect the user to the workout in progress page.
* The user shall have the option to delete a previously saved workout.

#### 3.5.2.4 Workout in Progress Page <a name="3.5.2.4-workout-in-progress-page" />
* The workout in progress page shall guide the user through their workout.
* The workout in progress page shall display the workout information for the selected workout.

### 3.5.3 Usability Requirements <a name="3.5.3-usability-requirements" />
<!--Workouts-->
* The user shall be able to create a workout.
* The user shall be able to find a workout.
* The user shall be able to save a workout.
* The user shall be able to start a workout.
* The user shall be able to see workout progress.

### 3.5.4 Performance Requiremnts <a name="3.5.4-performance-requirments" />
* The user shall only be able to save one video link for a specific exercise.
* The system shall support a configurable amount of workouts.
* The system shall support a configurable amount of tags per workout.

### 3.5.5 Logical Database Requirements <a name="3.5.5-logical-database-requirments" />
<!--Workout Table-->
* The workout table shall contain an exercise title column.
* The workout table shall contain a tag column.
* The workout table shall contain a rep column.
* The workout table shall contain a set column.
* The workout table shall contain a discription column.
* The workout table shall contain a video link column.
* The workout table shall contain a workout id column that acts as a **primary key**.

### 3.5.6 Design Constraints <a name="3.5.6-design-constraints" />
* The user shall only be able to add aproved YouTube links to an exercise.
* The user shall only be able to input an integer into the rep field.
* The user shall only be able to input an integer into the set field.
* The user shall have to add a title to the workouts they create.

### 3.5.7 Software System Attributes <a name="3.5.7-software-system-attributes" />
#### 3.5.7.1 Reliability <a name="3.5.7.1-reliability" />
* The system shall exit immediatly when user finds an error.
* The app shall check that locally stored user information matches what is stored in database.

#### 3.5.7.2 Security <a name="3.5.7.2-security" />
*  The user shall only be able to add aproved YouTube links to an exercise.

#### 3.5.7.3 Maintainability <a name="3.5.7.3-maintainability" />
* App administrators shall be able to remove **inapropriate** content.

<!--3.8.3 Supporting Information
- N/A-->

<br>

## References <a name="references" />
* [1] S.R.O., Eccam. “Example Software Requirements Specification (SRS)  ReqView Documentation.” ReqView, 2018, www.reqview.com/doc/iso-iec-ieee-29148-srs-example.

* [2] IIEEE, " 29148-2018 - ISO/IEC/IEEE International Standard - Systems and software engineering -- Life cycle processes -- Requirements engineering " pp. 56-87, Jul. 2018. [Online] Available: https://ieeexplore-ieee-org.byui.idm.oclc.org/document/8559686 

* [3] “Macintosh Operating System (Mac OS).” Techopedia, techopedia, 2012, www.techopedia.com/definition/2639/macintosh-operating-system-mac-os.

* [4] https://github.com/voyager1winterberry/cse372-01srs/blob/main/refDocs/Week10Assignments.docx
