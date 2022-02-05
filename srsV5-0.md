myJym Software Requirements Specification
=========================================
Project Sponsor: Jared Barney
<br>
Project Owner: Jared Barney
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

## <b>Table of Contents</b>
* [1.0 Introduction](#1.0-introduction)
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
    * [1.5 Table of Tables](#1.5-table-of-tables)
* [2.0 References](#2.0-references)
* [3.0 Requirements](#3.0-requirements)
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
        * [3.3.8 Supporting Information](#3.3.8-supporting-information)
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
            * [3.5.1.2 video provider](#3.5.1.2-video-provider)
        * [3.5.2 Functions](#3.5.2-functions)
            * [3.5.2.1 Create Workout](#3.5.2.1-create-workout)
            * [3.5.2.2 Find Workout](#3.5.2.2-find-workout)
            * [3.5.2.3 Saved Workout](#3.5.2.3-saved-workout)
            * [3.5.2.4 Workout in Progress Page](#3.5.2.4-workout-in-progress-page)
            * [3.5.2.5 My Video Page](#3.5.2.5-my-video-page)
        * [3.5.3 Usability Requirements](#3.5.3-usability-requirements)
        * [3.5.4 Performance Requirements](#3.5.4-performance-requirements)
        * [3.5.5 Logical Database Requirements](#3.5.5-logical-database-requirements)
        * [3.5.6 Design Constraints](#3.5.6-design-constraints)
        * [3.5.7 Software System Attributes](#3.5.7-software-system-attributes)
            * [3.5.7.1 Reliability](#3.5.7.1-reliability)
            * [3.5.7.2 Security](#3.5.7.2-security)
            * [3.5.7.3 Maintainability](#3.5.7.3-maintainability)
* [4.0 Validation](#4.0-validation)
    * [4.1 My Trainer](#4.1-my-trainer)
        * [4.1.1 External Interface Verification](#4.1.1-external-interface-verification)
            * [4.1.1.1 Google Authentication Verification](#4.1.1.1-google-authentication-verification)
        * [4.1.2 Functions Verification](#4.1.2-functions-verifications)
            * [4.1.2.1 Notifications Verification](#4.1.2.1-notifications-verifications)
            * [4.1.2.2 View Trainer Profile Verification](#4.1.2.2-view-trainer-profile-verifications)
            * [4.1.2.3 Update Profile Verification](#4.1.2.3-update-profile-verifications)
            * [4.1.2.4 Search Trainer Verification](#4.1.2.4-search-trainer-verifications)
            * [4.1.2.5 Message Trainer Verification](#4.1.2.5-message-trainer-verifications)
            * [4.1.2.6 Message Users Verification](#4.1.2.6-message-users-verifications)
        * [4.1.3 Usability Requirements Verification](#4.1.3-usability-requirements-verifications)
        * [4.2.1 Map External Interfaces Verification](#4.2.1)
        * [4.2.2 Map Functions Verification](#4.2.2)
        * [4.2.3 Map Usability Requirements Verification](#4.2.3)
        * [4.2.4 Map Performance Requirements Verification](#4.2.4)
        * [4.2.5 Map Logical Database Requirements Verification](#4.2.5)
    * [4.3 MyJym Videos Verification](#4.3-myjym-videos-verification)
        * [4.3.1 External Interfaces Specification Verification](#4.3.1-external-interfaces-specifications-verification)
            * [4.3.1.1 Database Verification](#4.3.1.1-database-verification)
        * [4.3.2 Functions Verification](#4.3.2-functions-verification)
            * [4.3.2.1 My Video Verification](#4.3.2.1-my-video-verifiaction)
        * [4.3.3 Usability Requirement Verification](#4.3.3-usability-requirement-verification)
        * [4.3.4 Performance Requirements Verification](4.3.4-performance-requirements-verification)
        * [4.3.5 Logical Database Requirements Verification](#4.3.5-logical-database-requirements-verification)
        * [4.3.6 Design Constraint Verification](#4.3.6-design-constraints-verification)
        * [4.3.7 Software System Attributes Verification](#4.3.7-software-system-attributes-verification)
            * [4.3.7.1 Reliability Verification](#4.3.7.1-reliability-verification)
            * [4.3.7.2 Security Verification](#4.3.7.2-security-verification)
            * [4.3.7.3 Maintainability Verification](#4.3.7.3-maintainability-verification)
    * [4.4 Login & Homepage Verification](#4.4-login-&-homepage-verification)
        * [4.4.1 External Interfaces Verification](#4.4.1-external-interfaces-verification)
        * [4.4.2 Functions Verification](#4.4.2-functions-verification)
        * [4.4.3 Usability Requirements Verification](#4.4.3-usability-requirements-verification)
        * [4.4.4 Performance Requirements Verification](#4.4.4-performance-requirements-verification)
        * [4.4.5 Logical Database Requirements Verification](#4.4.5-logical-database-verification)
        * [4.4.6 Design Constraints Verification](#4.4.6-design-constraints-verification)
        * [4.4.7 Software System Attributes Verification](#4.4.7-software-system-attributes-verification)
            * [4.4.7.1 Reliability Verification](#4.4.7.1-reliability-verification)
            * [4.4.7.2 Availability Verification](#4.4.7.2-availability-verification)
            * [4.4.7.3 Security Verification](#4.4.7.3-security-verification)
            * [4.4.7.4 Portability Verification](#4.4.7.4-portability-verification)
    * [4.5 My Workout Verification](#4.5-my-workout-verification)
        * [4.5.1 External Interface Verification](#4.5.1-external-interface-verification)
            * [4.5.1.1 Database Verification](#4.5.1.1-database-verification)
            * [4.5.1.2 Video Provider Verification](#4.5.1.2-video-provider-verification)
        * [4.5.2 Functions Verification](#4.5.2-functions-verification)
            * [4.5.2.1 Create Workout Verification](#4.5.2.1-create-workout-verification)
            * [4.5.2.2 Find Workout Verification](#4.5.2.2-find-workout-verification)
            * [4.5.2.3 Saved Workout Verification](#4.5.2.3-saved-workout-verification)
            * [4.5.2.4 Workout in Progress Page Verification](#4.5.2.4-workout-in-progress-page-verification)
            * [4.5.2.5 My Video page Verification](#4.5.2.5-my-video-page-verification)
        * [4.5.3 Usability Requirements Verification](#4.5.3-usability-requirements-verification)
        * [4.5.4 Performance Requirements Verification](#4.5.4-performance-requirments-verification)
        * [4.5.5 Logical Database Requirements Verification](#4.5.5-logical-database-requirments-verification)
        * [4.5.6 Design Constraints Verification](#4.5.6-design-constraints-verification)
        * [4.5.7 Software System Attributes Verification](#4.5.7-software-system-attributes-verification)
            * [4.5.7.1 Reliability Verification](#4.5.7.1-reliability-verification)
            * [4.5.7.2 Security Verification](#4.5.7.2-security-verification)
            * [4.5.7.3 Maintainability Verification](#4.5.7.3-maintainability-verification)
* [References](#references)
<br><br /><br>

# <b>1.0 Introduction</b> <a name="1.0-introduction" />

<br>

## <b>1.1 Purpose</b> <a name="1.1-purpose" />
The myJym app is to help people at all levels of experience feel confident using gym equipment.  It also focuses on connecting users to personal trainers.  Additional features include work out regiments, gym maps, and ability to track fitness goals.

<br>

## <b>1.2 Scope</b> <a name="1.2-scope" />
The scope of the myJym system will be to produce the myJym application for iOS, Android, and web.  This will include everything listed in the products to be produced, what the software will do, and included core features sections.

<br>

### <b>1.2.1 Products to be Produced</b> <a name="1.2.1-proucts-to-be-produced" />
The products that the myJym app will utilize:
- server
- database
- mobile myJym app
- web based myJym app

<br>

### <b>1.2.2 What Will the Software Product Do</b> <a name="1.2.2-what-will-the-software-product-do" />
The server will allow users to connect to the database.  The database will house the information required for the app to run.  The product, the myJym app, will assist users in creating workouts, executing a workout and connecting with trainers.

<br>

### <b>1.2.3 Included Core Features</b> <a name="1.2.3-included-core-features" />
This is a table outlining the main features of the app with a brief description of what the feature is.
| Feature | Description                                                          |
|---------|----------------------------------------------------------------------|
| Login Page | The page that allows users to login with their credentials.       | 
| Home Page | The first page that users will see after logging into the app.     |
| My Trainers | Page to mediate interaction between trainers and gym goers.      |
| My Workouts | Page that allows creation and execution of workouts.             |
| My Videos | Page that has a list of links to all videos used by the app.       |
| Gym Map | A map showing the location of equipment, services, and gym features. |

<br>

### <b>1.2.4 Excluded Features</b> <a name="1.2.4-excluded-features" />
This is a table outlining what features are outside the scope of this project with a brief description of the feature as discussed in the elicitation data, and reviewed by the customer.
| Feature | Description                                                          |
|---------|----------------------------------------------------------------------|
| Nutrition Information | Not intended to recommend meal plans, diets, count calories or anything else similar. | 
| Video Platform | Not intended to have recorded workout videos to follow. |

<br>

### <b>1.3.1 Product Perspective</b> <a name="1.3.1-product-perspective" />
The myJym app interface will work with multiple internal and external services. Each interface helps in communication between system, hardware, user, and 3rd parties.

<br>

#### <b>1.3.1.1 System Interfaces</b> <a name="1.3.1.1-system-interfaces" />
The system interfaces will be the platforms that the application will be running on. The list below will be the systems used for the application. 

* The myJym app will run on mobile services. 
* The myJym app will run on web services. 
* The myJym app will connect to google authentication for login credentials. 

<br>

#### <b>1.3.1.2 User Interfaces</b> <a name="1.3.1.2-user-interfaces" />
The user interfaces will be the functionality of the app. This functionality is what the user will see when in the app.  

* The myJym app will include a built-in messaging system to allow communication between users. 
* The myJym app will include a sign-in page and a login page for the user.   
* The myJym app will have a search bar that will allow the user to search for workouts, trainers, and pages. The search bar will allow for quick searches for the user's needs. 
* The myJym app will have a settings page which will have everything in the page that the user can see and change in the app. Settings will include the user's profile and trainers they work with. 
* The myJym app will have a workout page which will allow the user to CRUD workouts. 
* The myJym app will have a myJym page which will find the gym you will be going to and a built-in map of that gym.
* The myJym app will allow the user to update their profile through the app.

<br>

#### <b>1.3.1.3 Hardware Interfaces</b> <a name="1.3.1.3-hardware-interfaces" />
A hardware interface for the myJym app will be using internet and cell services.

* Since the application will be run over the internet and cell service data, most of the hardware requirements will ensure the iOS and android devices are able to connect to the internet. Since myJym will be a fitness app, features of myJym shall require users to have the feature of location tracking for personal coach and exercise equipment tutorial videos on their mobile device. Preferably, iPhone 6 and later gen, for the purpose of app store update reasons. The version of the iOS system shall be 15.1.1, and android system shall be 11.  

<br>

#### <b>1.3.1.4 Software Interfaces</b> <a name="1.3.1.4-software-interfaces" />
Software interfaces (programming interfaces) are the languages, codes and messages that programs use to communicate with each other and to the hardware. Examples are the Windows, Mac and Linux operating systems, SMTP email, IP network protocols and the software drivers that activate the peripheral devices. 

* Specify the use of other required software products.  
    - Operating System: iOS and Android devices, and desktop applications, and the content will be operating within the mobile application.  

    - Linkage: Users shall be allowed to sign up myJym with their existing personal email address to login to their accounts.   

<br>

#### <b>1.3.1.5 Communications Interfaces</b> <a name="1.3.1.5-communications-interfaces" />
* Communication interfaces shall include communication between the users.
* Communication interfaces shall include communication between the trainers, including a means of messaging within the app. 
* Communication shall include a means of communicating with myJym to receive help.

<br>

#### <b>1.3.1.6 Memory</b> <a name="1.3.1.6-memory" />
* Primary memory shall be used to store the user’s data such as profile and user agreements

<br>

#### <b>1.3.1.7 Operations</b> <a name="1.3.1.7-operations" />
* Operations by the user shall include:
    - Creating a profile upon first use of the app
    - Connect with trainers that can offer insight and assistance into the workout  schedule of the user
    - Learn how to use gym equipment by scanning a QR code on the machine and watching the associated video.
    - Operations by the Trainers shall include:
    - Creating a profile upon first use of the app
    - Receiving approval from myJym to contact and train users through an approval process
    -Connect with users through messaging and other means through the app to assist with training goals

<br>

#### <b>1.3.1.8 Site Adaption Requirements</b> <a name="1.3.1.8-site-adaption-requirements" />
The system must be available in the following formats. 
* Android 
* IOS 
* Web application 

<br>

#### <b>1.3.1.9 Interfaces with Services</b> <a name="1.3.1.9-interfaces-with-services" />
The different services that the system will interact with. 
* Video links from a video provider links to the various workout videos must be accessible 
* The server will connect accounts to the main database to access the account information 

<br>

### <b>1.3.2 Product Functions</b> <a name="1.3.2-product-functions" />
For the product functions of the myJym application the following User Profiles and User Scenarios will be as follows:

<br>

#### <b>1.3.2.1 User Profiles</b> <a name="1.3.2.1-user-profiles" />
The following User Profiles define the target demographics for the myJym application:
 - A returned missionary attending BYU-Idaho, in their early twenties, has a busy schedule with work and a heavy course load.
 - A student in their junior year, also attending BYU-Idaho, in their early twenties, they enjoy playing football with their friends and family.
 - A new freshman, halfway through the semester wanting to lose weight, but unsure of where to start.
 - A couple that likes to spend time together by playing sports and working out.
The application will be available to all age groups and demographics; however, these groups will serve as the focus the application.

<br>

#### <b>1.3.2.2 User Scenarios</b> <a name="1.3.2.2-user-scenarios" />
The following User Scenarios serve to describe the use cases that have been elicited to be applicable to the product functions of the myJym application:
- Only being able to attend the gym in the early morning, with no previous time to set a workout routine or research workout machines.
- Brand new to exercising, there is a fear of feeling inadequate and confused in front of others, and a desire to be helped in a discreet way.
- Getting burnt out with their current workout routine, and desiring new machines and techniques that can help them develop new routines.
- A student desires additional experience with a variety of exercises including strength training, endurance training, weight loss, and cardio training to be able to better meet their fitness goals.

<br>

### <b>1.3.3 User Characteristics</b> <a name="1.3.3-user-characteristics" />
This table is for the user characteristics from the perspective of a gymgoer.
| ***User Group***       | ***Trainee***       |
| -------------    | ------------  |
| User Profile | This User group will be using the myJym application to connect to a personal trainer, as well as obtain information on workout equipment and techniques. The Trainee will have to register on the myJym application and have time available to meet with a Personal Trainer, learn workout equipment and routines|
| ***Demographic Criteria*** |
| Age | 18 - 70 |
| Income | Middle class income |
| Education | All forms of education|
| Geography | Cities with public gyms and access to personal trainers locally |
| City Size | Large enough city with access to gyms and trainers |
| Disabilities | Many workouts require the user to be a fully functional adult |
| Gender | Any gender |
| Technical Expertise | Competent, able to navigate through most applications |
| ***Psychographic Criteria*** |
| Information Availability and Content | Information availability is key information if the user wants to connect to the Personal Trainer. If user wants to understand gym equipment and make a workout routine. Simple information is required about the user like age, sex, and location, but no detailed information about the user is required |
| Ease of Use | Users require and easy-to-use application, that can be operated with mobile devices |
| Privacy and Security | Security, as well as user information security, need to be protected via encryption or password.|
| Graphic Style | Application appearance/graphics should be functional but most importantly readable, there should be no small fonts or distracting colors or images to allow easy use, as well as allow for people with disabilities and international constraints |
| Fulfillment and reliability | Reliability is essential. The application should always be functional since the ability to constantly communicate between users and trainers should be available |

<br>

This table is for the user characteristics from the perspective of a trainer.

| ***User Group*** | ***Personal Trainer*** |
|------------- | ---------------- |
| User Profile | This Personal Trainer group will be using the myJym application to connect to trainees, as well as obtain information on available equipment and trainees looking for a personal trainer. The Personal Trainer will have to register on the myJym application, and have time available to meet with a trainee, and have a clear understanding of equipment and techniques, and able to teach and make a workout routine for the trainee |
| ***Demographic Criteria*** |             
| Age | 18 - 50 |
| Income | Middle class income |
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

<br>

### <b>1.3.4 Limitations</b> <a name="1.3.4-limitations" />
The limitations of myJym are defined in the following subsections. 

<br>

#### <b>1.3.4.1 Regulatory Requirements and Policies</b> <a name="1.3.4.1-regulatory-requirements-and-policies" />
HIPPA / GDPR - Restrictions on collecting personal information. Important to be transparent. Ensure that personal information does not have to be given to operate, only given voluntarily.

<br>

#### <b>1.3.4.2 Hardware Limitations</b> <a name="1.3.4.2-hardware-limitations" />
Hardware requirements are a camera, internet access, and a smart phone. The computers of the development team are a limiting factor. 

<br>

#### <b>1.3.4.3 Interfaces to Other Applications</b> <a name="1.3.4.3-interfaces-to-other-applications" />
One limitation of interfacing with other applications would be the licensing of a third-party video service. The video service might also run ads, this hurt the user experience. The messaging service could require the user to create an account, this could deter some users from using the app. 

<br>

#### <b>1.3.4.4 Parallel Operation</b> <a name="1.3.4.4-parallel-operation" />
Calorie tracking will require the use of a smart watch or fitness tracker which not everyone will have. Bluetooth would be used to connect the devices; Bluetooth could cause problems for less tech savvy users. 

<br>

#### <b>1.3.4.5 Audit Functions</b> <a name="1.3.4.5-audit-functions" />
There are no audit functions in version 1.0 of this product.

<br>

#### <b>1.3.4.6 Control Functions</b> <a name="1.3.4.6-control-functions" />
There are no control functions for version 1.0 of this product.

<br>

#### <b>1.3.4.7 Higher-Order Language Requirements</b> <a name="1.3.4.7-higher-order-language-requirements" />
Since this is a mobile application two different apps need to be written, one for android and one for apple. This will require the use of Kotlin and Swift so the developers will need to learn or know at least one of these languages. This could also cause problems in ensuring that the apps are the same. A way to get around this would be to use a web app using Django, HTML, CSS, and JS. 

<br>

#### <b>1.3.4.8 Signal Handshake Protocols</b> <a name="1.3.4.8-signal-handshake-protocols" />
There are no signal handshake protocols for version 1.0 of this product.

<br>

#### <b>1.3.4.9 Quality Requirements</b> <a name="1.3.4.9-quality-requirements" />
There are no quality requirements for version 1.0 of this product. 

<br>

#### <b>1.3.4.10 Criticality of the Application</b> <a name="1.3.4.10-criticality-of-the-application" />
There is no criticality of the application for version 1.0 of this product.

<br>

#### <b>1.3.4.11 Safety and Security Considerations</b> <a name="1.3.4.11-safety-and-security-considerations" />
There are no safety and security consideration limitations for version 1.0 of this product.

<br>

#### <b>1.3.4.12 Physical/Mental Considerations</b> <a name="1.3.4.12-physical/mental-considerations" />
The system will need to consider the physical limitations of the gym goer. The system will need to include a liability waiver in the terms and conditions. 

<br>

#### <b>1.3.4.13 External System Limitations</b> <a name="1.3.4.13-external-system-limitations" />
The limitations of a video streaming service will apply to the app. 

<br>

## <b>1.4 Definitions:</b> <a name="1.4-definitions" />
This is a comprehensive list of needed definitions used by the myJym application:
| Word   |  Definition |
| ------ | -------     |
| Account | An arrangement allowing a user personalized access to the myJym application, requiring the use of a username and password to access. |
| Admin | The people that run the app. They will connect the user's location to the gym and create QR codes that can be scanned by the user. |
| Audit Functions | Functions of the application that allow for user feedback and error handling. |
| App | myJym mobile application. |
| Criticality of the Application | Parts of the application have dependencies that can fail because of them. The most critical parts of the application.|
| The Database | A database that will store all information needed to run the application containing the following tables: Admin, User Data, Trainer, and Workout. |
| Equipment | The machines at the student gym. |
| Email | A method of exchanging messages over the internet between electronic devices. |
| Error Message | A message stating that a condition is incorrect and requires that the condition be different. |
| Forms | Digital way to collect relevant information from the user. |
| Google | An American company that specializes in internet-related services and products. |
| Google Authentication Key | A key provided by Google to authenticate users. |
| Gym | A location with workout machines available. |
| Gymgoers | Users that go to the gym               |
| Gym Hours | The hours that all partner gyms are open. |
| Higher-Order Language Requirements | Knowledge of high-level programming languages such as Kotlin and Swift. |
| Home Page | The view which allows access to My Trainer, My Workout, My Videos, and My Gym Map views. |
| Interface | A point where two systems, subjects, organizations, etc. meet and interact. |
| Interfaces to other applications | The ability to interact with third party applications. |
| Invalid Credentials | Login credentials that do not match those associated with an account. |
| iOS | Internet Operating System or iPhone Operating System. It is the operating system used on Apple products, such as iPhone and iPad. |
| IOS 14.1 | The minimum IOS version that will be required for the project |
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
| Personal Trainer | Individuals who have earned certification that demonstrates they have achieved a level of competency for exercising safely and efficiently along with creating safe and effective exercise programs for those who have the medical clearance to participate. Personal trainers assist trainees. |
| Personal Trainer Certificate | Individuals who have earned certification that demonstrates they have achieved a level of competency for exercising safely and efficiently along with creating safe and effective exercise programs for those who have the medical clearance to participate. Personal trainers can assist trainees, and can do so while working in conjunction with the myJym app. |
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
| System Database | The system database is a database containing schemas for the layout of the gym. |
| Pixels Per Inch (PPI) | The is how the resolution of a display is measure based on the amount of pixels across one inch on the screen. |
<br>

## <b>1.5 Table of Tables</b> <a name="1.5-table-of-tables" />
| Table | Link |
|---------|----------------------------------------------------------------------|
| 1.2.3 | [1.2.3 Included Core Features](#1.2.3-included-core-features) | 
| 1.2.4 | [1.2.4 Excluded Features](#1.2.4-excluded-features) | 
| 1.3.3 | [1.3.3 User Characteristics](#1.3.3-user-characteristics) | 
| 1.4 | [1.4 Definitions](#1.4-definitions) | 
| 3.0 | [3.0 Requirements](#3.0-requirements) | 
| 4.0 | [4.0 Validation](#4.0-validation) | 

<br>
<br>

# <b>2.0 References</b> <a name="2.0-references" />
[1] S.R.O., Eccam. “Example Software Requirements Specification (SRS)  ReqView Documentation.” ReqView, 2018, www.reqview.com/doc/iso-iec-ieee-29148-srs-example.

[2] IIEEE, " 29148-2018 - ISO/IEC/IEEE International Standard - Systems and software engineering -- Life cycle processes -- Requirements engineering " pp. 56-87, Jul. 2018. [Online] Available: https://ieeexplore-ieee-org.byui.idm.oclc.org/document/8559686 

[3] “Macintosh Operating System (Mac OS).” Techopedia, techopedia, 2012, www.techopedia.com/definition/2639/macintosh-operating-system-mac-os.

[4] Brother Clements' myJym Diagram, https://github.com/voyager1winterberry/cse372-01srs/tree/main/Images/brother-clements-myjym-diagram.jpg

[5] Initial SRS sections, https://github.com/voyager1winterberry/cse372-01srs/tree/main/Images/initial-srs-sections.jpg

[6] myJym Diagram v0.5, https://github.com/voyager1winterberry/cse372-01srs/tree/main/Images/myjym-diagram-v0.5.jpg

[7] myJym Diagram v1.0, https://github.com/voyager1winterberry/cse372-01srs/tree/main/Images/myjym-diagram-v1.0.jpg

[8] myJym Diagram v2.0, https://github.com/voyager1winterberry/cse372-01srs/tree/main/Images/myjym-diagram-v2.0.png

<br>
<br>

# <b>3.0 Requirements</b> <a name="3.0-requirements" />
This section was written and ordered in the manner that was most convenient for workflow. However, the ideal order to read this section of the document is:
| Section | Title Name|
|---------|----------------------------------------------------------------------|
| 3.4 | Login Page & Homepage | 
| 3.1 | My Trainer |
| 3.5 | My Workout |
| 3.3 | My Video |
| 3.2 | My Gym Map |

<br>

## <b>3.1 My Trainer</b> <a name="3.1-my-trainer" />
The My trainer portion is a page accessible through the homepage.

<br>

### <b>3.1.1 External Interfaces</b> <a name="3.1.1-external-interfaces" />
The external interfaces section will cover 3rd party programs that will be used.

<br>

#### <b>3.1.1.1 Google Authentication</b> <a name="3.1.1.1-google-authentication" />
Google authentication will check the authentication and security of the my trainers login page.

***3.1.1.1.1*** Google Authentication API shall be used by gymgoers and trainers to login to their accounts. <br>
***3.1.1.1.2*** All users shall be able to login to their account using a google account. <br>
***3.1.1.1.3*** All users shall be able to create an account using a google account. <br>

<br>

## <b>3.1.2 Functions</b> <a name="3.1.2-functions" />
The myJym application will allow users to view the My Trainer page and receive system notifications. 

***3.1.2.1*** The myJym application shall send users Notifications. <br>
***3.1.2.2*** The My Trainer page shall allow users to view trainer profiles. <br>
***3.1.2.3*** The My Trainer page shall allow users to search for trainers. <br>
***3.1.2.4*** The My Trainer page shall allow users to update their profile. <br>
***3.1.2.5*** The My Trainer page shall allow users to message trainers. <br>
***3.1.2.6*** The My Trainer page shall allow trainers to message users. 

<br>

### <b>3.1.2.1 Notifications</b> <a name="3.1.2.1-notifications" />
Notifications will allow users to receive notifications on their device about scheduled workouts and sent messages.

***3.1.2.1.1*** A notification shall be sent to the user’s devices when a user sets a time for their workout. <br>
***3.1.2.1.2*** A notification shall be sent to the user’s device when the user receives a message. <br>

<br>

### <b>3.1.2.2 View Trainer Profile</b> <a name="3.1.2.2-view-trainer-profile" />
The trainer profile will provide a viewable page for users with the trainer's photo, short bio, video links from a video provider, a follow button, a link to workouts created by the trainer, and a button to message the trainer.

***3.1.2.2.1*** Trainer profile shall be viewable by gymgoers. <br>
***3.1.2.2.2*** Trainer profile shall display a picture of the trainer. <br>
***3.1.2.2.3*** Trainer profile shall display a short biography of the trainer. <br>
***3.1.2.2.4*** Trainer profile shall display a clickable link to the trainer’s videos on a video provider. <br>
***3.1.2.2.5*** “View Workouts” shall be an option on the Trainer profile that allows the user to view a trainer’s created workouts. <br>
***3.1.2.2.6*** “Message Trainer” shall be an option on the Trainer profile that allows the user to send a message to the trainer. <br>
***3.1.2.2.7*** Trainer profiles shall store a trainers first name <br>
***3.1.2.2.8*** Trainer profiles shall store a trainer’s last name. <br>
***3.1.2.2.9*** Trainer profiles shall store a trainer’s email. <br>
***3.1.2.2.10*** The system shall create a unique ID for each trainer. <br>
***3.1.2.2.11*** The system shall create a personal key for each trainer. <br> 

<br>

### <b>3.1.2.3 Update Profile</b> <a name="3.1.2.3-edit-profile" />
The update profile function will allow any user to make changes to their profile. 

***3.1.2.3.1*** Update Profile shall allow any user to update their own picture. <br>
***3.1.2.3.2*** Update Profile shall allow any user to update a biography text-field. <br>
***3.1.2.3.3*** Update Profile shall allow any user to update their personal video links. <br>
***3.1.2.3.4*** Update Profile shall allow any user to update their first and last name. <br>

<br>

### <b>3.1.2.4 Search Trainer</b> <a name="3.1.2.4-search-trainer" />
Search trainer will allow users to search for trainers by name, location, and workout. 

***3.1.2.4.1*** The system shall have a search bar. <br>
***3.1.2.4.2*** A search bar shall be viewable by the user. <br>
***3.1.2.4.3*** Search trainer shall allow a user to search for a trainer by name. <br>
***3.1.2.4.4*** Search trainer shall allow a user to search for a trainer by location. <br>
***3.1.2.4.5*** Search trainer shall allow a user to search for a trainer by workouts. <br>

<br>

### <b>3.1.2.5 Message Trainer</b> <a name="3.1.2.5-message-trainer" />
Message trainer will allow a user to communicate with a trainer. 

***3.1.2.5.1*** Message Trainer shall give a user the ability to send messages to a trainer. <br>
***3.1.2.5.2*** Message Trainer shall list messages in chronological order. <br>
***3.1.2.5.3*** Messages Trainer shall be able to handle messages containing text. <br>
***3.1.2.5.4*** Message Trainer shall be able to handle messages containing links. <br>

<br>

### <b>3.1.2.6 Message Users</b> <a name="3.1.2.6-message-users" />
Message Users shall allow the trainer to communicate with users. 

***3.1.2.6.1*** Message users shall give trainers the ability to send messages to users. <br>
***3.1.2.6.2*** Message users shall create a chat between trainer and users. <br>
***3.1.2.6.3*** Message users shall list messages in chronological order. <br> 
***3.1.2.6.4*** Messages Trainer shall be able to handle messages containing text. <br>
***3.1.2.6.5*** Message Trainer shall be able to handle messages containing links <br>

<br>

## <b>3.1.3 Usability Requirements</b> <a name="3.1.3-usability-requirements" />
Requirements that are part of the user experience. It is the different aspects of the system such as understandability, accessibility, task failure and more that impact how a user views and uses the system.  

***3.1.3.1*** Ease of learning. The system shall be easy to learn for both novices and users with experience from similar systems. Users familiar with similar systems shall be able to create a new account with minimal errors. <br>
***3.1.3.2*** Task efficiency. The system shall be designed to be simple to use for frequent users. Frequent users shall be given an option to be able to access their account without having to sign in each session. Tasks shall be able to be completed by the frequent user quickly and efficiently. <br>
***3.1.3.3*** Ease of remembering. The system shall be clear and well defined. Users experienced with this system shall be able to login to their account quickly. <br>
***3.1.3.4*** Understandability:  A new user shall be able to navigate to any desired option quickly and efficiently. <br>
***3.1.3.5*** Subjective satisfaction. The system shall receive a high rating by test groups when released. <br>
***3.1.3.6*** Task failure. Task failure by the system shall be kept to a minimum. <br>
***3.1.3.7*** Requirements to undo. The system should be able to allow users are able to try things and undo them. The ability to undo should be incorporated into any part of the system that stores information, or task. <br>
***3.1.3.8*** Accessibility. The system shall be created with elements that ensure that it is accessible to adults ranging from 18-40. These elements include but are not limited to: color, text, complexity, and exclusivity. <br>

<br>

## <b>3.1.4 Performance Requirements</b> <a name="3.1.4-performance-requirements" />
The performance requirements are showing the performance of unique features of my trainer page. The list will be a list of the features of my trainer page. 

***3.1.4.1*** My trainer page shall load when the user navigates to my trainer page. <br>
***3.1.4.2*** The trainer shall receive messages soon after the author sends the message. <br> 
***3.1.4.3*** The trainer shall be able to send messages after clicking the send button in the built-in messenger. <br>
***3.1.4.4*** Notifications for the trainer shall be received at the same time as when the message comes in. <br>
***3.1.4.5*** Notifications from the trainer shall be received at the same time the recipient receives the message. <br>
***3.1.4.6*** The trainer profiles on the web shall be loaded soon after the settings button has been clicked. <br>
***3.1.4.7*** The trainer profiles on the mobile app shall be loaded soon after the settings button has been clicked. <br> 
***3.1.4.8*** Trainer search results on the web shall load up soon after the search has been entered in. <br>
***3.1.4.9*** Trainer search results on the mobile app shall load up soon after the search has been entered in. <br>
 
<br>

## <b>3.1.5 Logical Database Requirements</b> <a name="3.1.5-logical-database-requirements" />

<br>

### <b>3.1.5.1 Types of Information Used by Various Functions</b> <a name="3.1.5.1-types-of-information-used-by-various-functions" /> 
The system shall include several types of data for each account.  

***3.1.5.1.1*** My Trainer shall store a trainers first name. <br>
***3.1.5.1.2*** My Trainer shall store a trainer’s last name. <br>
***3.1.5.1.3*** My Trainer shall store a trainer’s email. <br>
***3.1.5.1.4*** The system shall create a trainer ID for each trainer. <br>

<br>

### <b>3.1.5.2 Frequency of Use</b>  
Data shall not be reused between accounts. This will require all emails and primary keys to be unique to each account. 
    
***3.1.5.2.1*** Email data types shall be used for a single account. <br>  

<br>

### <b>3.1.5.3 Accessing Capabilities</b>
The following is the different access that should be given between accounts. 

***3.1.5.3.1*** Trainers shall have access to User Data first name. <br>
***3.1.5.3.2*** Trainers shall have access to User Data last name. <br>
***3.1.5.3.3*** Trainers shall have access to User Data goals. <br>
***3.1.5.3.4*** Trainers shall have access to User Data workout plan. <br>
***3.1.5.3.5*** Trainers shall have access to User Data gym. <br>

<br>

### <b>3.1.5.4 Integrity Constraints</b> 
The following are constraints and regulations on the data within the database. 

***3.1.5.4.1*** Data entries shall be possible entries. <br>
***3.1.5.4.2*** Impossible data entries shall not be allowed. <br>
***3.1.5.4.3*** Data entries shall be verified to ensure it is possible. <br>
***3.1.5.4.4*** The database shall have entity integrity. <br>

<br>

### <b>3.1.5.5 Security</b>  
The following refers to account security and the different measures that should be taken to ensure account safety.  

***3.1.5.5.1*** Trainer accounts shall utilize google sign-in to access their account. <br>
***3.1.5.5.2*** User accounts shall utilize google sign-in to access their account. <br>
***3.1.5.5.3*** Trainers shall only have one account. <br>
***3.1.5.5.4*** Gymgoers shall only have one account. <br>
***3.1.5.5.5*** Admin accounts shall have access to all accounts. <br>

<br>

## <b>3.1.6 Design Constraints</b> <a name="3.1.6-design-constraints" />
Design constraints are conditions that need to happen for a project to be successful. Design constraints help narrow choices when creating a project. 

***3.1.6.1*** The system users shall specify the requirements for My Trainer and ensure to understand these requirements meet their demands and needs. <br>
***3.1.6.2*** Users shall specify changes to the requirements. <br>
***3.1.6.3*** The system managers shall use the requirements documentation to plan a bid for the system to plan the system development process for My Trainer. <br>
***3.1.6.4*** The system engineers shall use the requirements to understand what system is being developed. <br>
***3.1.6.5*** System testing engineers shall use the requirements for the purpose of development of validation tests for the system of My Trainer. <br>
***3.1.6.6*** System maintenance managers shall use requirements to understand the system and the relationship between its parts. <br>

![Design Constraints Image](Images/DesignConstraintsImage.png)

<br>

## <b>3.1.7 Software System Attributes</b> <a name="3.1.7-software-system-attributes" />
Software Quality Attributes:  Features that facilitate the measurement of performance of a software product by Software Testing professionals, and include attributes such as availability, interoperability, correctness, reliability, learnability, robustness, maintainability, readability, extensibility, testability.

<br>

### <b>3.1.7.1 Reliability</b> <a name="3.1.7.1-reliability" />
***3.1.7.1.1*** Applications shall not have errors within the codes to cause applications to close or crash. <br>
***3.1.7.1.2*** There will be functions within the software that performs verifications to notice errors before the application break or force closes. <br>
***3.1.7.1.3*** The system shall verify the information that matches from the server and the application. <br>

<br>

### <b>3.1.7.2 Security</b> <a name="3.1.7.2-security" />
***3.1.7.2.1*** Password Protection and Encryption <br>
***3.1.7.2.2*** User account creation <br>
***3.1.7.2.3*** User information shall be available to users and those have access. <br>
***3.1.7.2.4*** User shall be required to provide email, and password for the purpose of account creation. <br>

<br>

### <b>3.1.7.3 Data Privacy</b> <a name="3.1.7.3-data-privacy" />
***3.1.7.3.1*** User’s data shall be hidden from all other users and parties. <br>
***3.1.7.3.2*** Login Information <br>
***3.1.7.3.3*** Creating an account shall be safe and secure. <br>
***3.1.7.3.4*** All users shall be allowed to login securely. <br>
***3.1.7.3.5*** Once a user logs out from the account, all user information shall be removed from the login screen. <br>

<br>

### <b>3.1.7.4 Maintainability</b> <a name="3.1.7.4-maintainability" />
***3.1.7.4.1*** Users shall be allowed to report to the administration team if they forget their password, and need to have a reset password email sent to their personal email that has been registered on their myJym account. <br>
***3.1.7.4.1*** An automatic email shall be sent to the user's email address to allow the user to reset their password. <br>

<br>

### <b>3.1.7.5 Portability</b> <a name="3.1.7.5-portability" />
***3.1.7.5.1*** System Database shall store user information. <br>
***3.1.7.5.2*** myJym application shall run on both Android and iOS mobile interface. <br>

## <b>3.1.8 Supporting Information</b> <a name="3.1.8-supporting-information" />
![Design Constraints Image](Images/SupportingInfoImage.png)

<br>

## <b>3.2 Gym Map</b> <a name="3.2-gym-map" /> <!-- Team 2 -->
The map of the gym used by the MyJym application and its requirements will be detailed in this section.

<br>

### 3.2.1 External Interfaces <a name="3.2.1-external-interfaces" />
***3.2.1.1*** The map shall utilize the System Database to obtain needed information for the map generation. <br>

<br>

***3.2.1.1*** The map search bar shall obtain user data from the **System Database**. <br>

<br>

### 3.2.2 Functions <a name="3.2.2-functions" />
Functions of the gym map and its associated features are detailed below:

<br>

#### 3.2.2.1 Map Display <a name="3.2.2.1-map-display" />
The map display will be responsible for how the various graphical display elements will be handled. 
These are as follows:<br>
***3.2.2.1.1*** The map shall organize gym equipment according to a configuration file. <br>
***3.2.2.1.2*** The map shall organize gym services according to a configuration file. <br>
***3.2.2.1.3*** When an abnormal state is encountered the map shall stop and refresh. <br>
***3.2.2.1.4*** The map shall support modification to facility locations by a system administrator. <br>
***3.2.2.1.5*** A simple tutorial of using the map shall display the first time a user opens to that view. <br>

<br>

#### 3.2.2.2 Map Search Function <a name="3.2.2.2-map-search-function" />
The map features a search bar with the following capabilities: <br>
***3.2.2.2.1*** The map search bar shall perform validation on inputs matching them to gym functions. <br>
***3.2.2.2.2*** The map shall provide a search bar used to locate gym functions. <br>
***3.2.2.2.3*** The map search bar shall be a modeless interface not restricting user input to other parts of the application. <br>
***3.2.2.2.4*** Facilities in the gym shall be searchable by name through the map search bar. <br>

<br>

#### 3.2.2.3 Map Navigation <a name="3.2.2.3-map-navigation" />
The requirements for navigating on the map are as follows: <br>
***3.2.2.3.1*** The map shall be scrollable edge to edge. <br>
***3.2.2.3.2*** The map shall support zooming, detecting when a zoom request is made. <br>
***3.2.2.3.3*** Gym function icons shall be interactable to view options related to that function. <br>

<br>

### 3.2.3 Usability Requirements <a name="3.2.3-usability-requirements" />
For the myJym app the usability requirements serve to increase the usability for the user include the ease of learning, task efficiency, ease of remembering, understandability, task failure, and accessibility. These are criteria which serve to increase the usability of myJym.

These are as follows: <br>
***3.2.3.1*** Ease of learning- The map shall be intuitive allowing the user to easily form a mental model of its workings. This will be facilitated by a clean organization for the display elements of the map. <br>
***3.2.3.2*** Task efficiency- The map shall facilitate a user quickly identifying where they should be in the gym to complete their desired activity. <br>
***3.2.3.3*** Ease of remembering. The map shall utilize simple command formats to ensure users are capable of creating a mental model of the map functionalities. <br>
***3.2.3.4*** Understandability: The user shall understand the purpose of the map. Map features shall use formats akin to those found on similar mobile applications. New users will be greeted by a tutorial upon first entering the map view. <br>
***3.2.3.5*** Task failure. When encountering a task failure, the map shall stop its operation and refresh. <br>
***3.2.3.6*** Accessibility. Map iconography shall be created based upon commonly recognized symbols. <br>

<br>

### 3.2.4 Performance Requirements <a name="3.2.4-performance-requirements" />
The performance requirements of the system for the myJym map feature will define the performance capabilities and how various conditions will impact their operation.

These are as follows: <br>
***3.2.4.1*** The map shall prioritize loading of graphical display elements prior to lower priority tasks. <br>
***3.2.4.2*** The map search functionality shall return results in higher performant step timing than** O**(n log n). <br>
***3.2.4.3*** The map shall allow interaction with elements after a predetermined time post loading. <br>

<br>

### 3.2.5 Logical Database Requirements <a name="3.2.5-logical-database-requirements" />
The data used by the gym map and its state will be detailed here as follows: <br>

<br>

#### 3.2.5.1 Types of information used by various functions <a name="3.2.5.1-types-of-information-used-by-various-functions" />
The following will be the information used by the myJym map to perform it's required functions: <br>
***3.2.5.1.1*** The map shall store the icons for the map as a data construct. <br>
***3.2.5.1.2*** The map shall use search inputs to retrieve data from the **System Database**. <br>

<br>

#### 3.2.5.2 Frequency of use <a name="3.2.5.2-frequency-of-use" />
The following will define how often the various functionalities of the myJym map will be accessed. <br>
***3.2.5.2.1*** Map icons shall be loaded into memory from the **System Database** when the view is selected. <br>
***3.2.5.2.2*** The map search functionality shall be accessible on demand.<br>

<br>

#### 3.2.5.3 Accessing Capabilities <a name="3.2.5.3-accessing-capabilities" />
The map will be able to be accessed from and have access to the following: <br>
***3.2.5.3.1*** The map shall be accessible from the home page of the myJym application. <br>
***3.2.5.3.2*** The map shall have access to the **System Database** to access gym equipment locations. <br>
***3.2.5.3.3*** The map shall have access to the **System Database** to return search results. <br>

<br>

#### 3.2.5.4 Data entities and their relationships <a name="3.2.5.4-data-entities-and-their-relationships" />
The data entities will have the following relationships: <br>
***3.2.5.4.1*** The map shall handle data for the exercise machine locations. <br>
***3.2.5.4.2*** The map shall handle data for the exercise machine images. <br>
***3.2.5.4.3*** The map shall handle data for the map search bar results. <br>

<br>

#### 3.2.5.5 Integrity Constraints <a name="3.2.5.5-integrity-constraints" />
The data stored by the map will be subject to the following integrity constraints: <br>
***3.2.5.5.1*** Map icons shall be entries to the database. <br>
***3.2.5.5.2*** Map data shall be formatted to match the conventions of the database. <br>
#### 3.2.5.6 Security <a name="3.2.5.6-security" />
The map data security will apply as follows: <br> <br>
***3.2.5.6.1*** Data used for the map shall not be accessible by other functions of myJym. <br>
### 3.2.6 Design Constraints <a name="3.2.6-design-constraints" />
The design constraints of the map, the limitations on its design, will be as follows: <br> <br>
***3.2.6.1*** The interactable map features shall provide sufficient **Pixels Per Inch** that the average human is able to cleanly select them. <br>

<br>

### 3.2.7 Software System Attributes <a name="3.2.7-software-system-attributes">
The system attributes used by the myJym app will detail the reliability and availability of the map: <br>
***3.2.7.1*** The map shall be available when the application has been opened to the home page. <br>
***3.2.7.2*** The map shall be available offline when not internet connectivity is available. <br>

<br>

#### 3.2.7.1 Reliability <a name="3.2.7.1-reliability" />
The factors of reliability for the myJym map shall be as follows: <br>
***3.2.7.1.1*** The maps delivered to the user on MyJym shall deliver accurate data based on the information in the **System Database.** <br>
***3.2.7.1.2*** The MyJym map shall be retained in memory while the myJym application is focused on a separate page. <br>

<br>

#### 3.2.7.2 Security <a name="3.2.7.2-security" />
The following act to maintain the integrity and security of the myJym map: <br>
***3.2.7.2.1*** The map shall only be editable by an admin. <br>

<br>
	
## <b>3.3 MyJym Videos</b> <a name="3.3-myjym-videos" /> <!-- team 3's work -->

This Specification section explains the MyJym application in detail, the specification goes over eight categories. Such as external interfaces, functionality, usability, performance, database, design constraints, and software system attribute requirements for the MyJym application. 

<br>

### 3.3.1 External Interfaces Specification <a name="3.3.1-external-interfaces-specifications" />
This section defines the inputs and outputs of the MyJym application.<br>

<br>

#### 3.3.1.1 Database <a name="3.3.1.1-database" />
This shows the what columns will be included to create the database. The specific column requirements are listed in section 3.5<br>
***3.3.1.1.1*** The database shall store workout title<br>
***3.3.1.1.2*** The database shall store workout video links<br>
***3.3.1.1.3*** The database shall store workout description<br>
***3.3.1.1.4*** The database shall store the image links

<br>

#### 3.3.1.2 Video Streaming <a name="3.3.1.2-video-streaming" />
The API for a video streaming website will be used to share videos on workout techniques and forms, and how to use gym exercise equipment. This will be used according to the product owner and stakeholder’s decisions.

***3.3.1.2.1*** Gymgoers shall have the ability to access workout videos

<br>
	
### 3.3.2 Functions <a name="3.3.2-functions" />
This section is responsible for explaining myJym’s ability to perform to the User’s standard. These functions are split up into sections that explain the procedure of the MyJym application in how to perform or complete tasks.

<br>

#### 3.3.2.1 My Video <a name="3.3.2.1-my-video" />
The purpose of the following section provides the capabilities of the video page. This represents an individual user for the MyJym application.<br>

***3.3.2.1.1*** The My Video page shall display a workout title.<br>
***3.3.2.1.2*** The My Video page shall display an equipment name.<br>
***3.3.2.1.3*** The My Video page shall display a workout video.<br>
***3.3.2.1.4*** The My Video page shall provide a save video button.<br>

<br>

### 3.3.3 Usability Requirements <a name="3.3.3-usability-requirement" />
This section lists the quality and use requirements for the MyJym application. Including measurable effectiveness and satisfaction criteria for the My Video feature. <br>
***3.3.3.1*** User shall be able to save a selected video<br>
***3.3.3.2*** User shall be able to view the workout video<br>
***3.3.3.3*** User shall be able to view saved videos<br>

<br>
	
### 3.3.4 Performance requirements <a name="3.3.4-performance-requirements" />
For the MyJym application to meet performance standards, there are specific requirements that are needed to be met, specified below.<br>
***3.3.4.1*** User shall be able to save a selected video<br>
***3.3.4.2*** The user shall only be able to save one video link per exercise.<br>
***3.3.4.3*** The My Video page shall support a configurable amount of workouts<br>
***3.3.4.4*** The My Video page shall support a configurable amount of workouts videos<br>

<br>

### 3.3.5 Logical Database Requirements <a name="3.3.5-logical-database-requirements" />

The MyJym database shall store all the tables that are necessary for storing information required by the application.<br>

***3.3.5.1*** The workout table shall contain an exercise title column<br>
***3.3.5.2*** The workout table shall contain a description column<br>
***3.3.5.3*** The workout table shall contain a video link column<br>
***3.3.5.4*** The workout table shall contain a workout id column that acts as a primary key<br>

<br>

### 3.3.6 Design Constraints <a name="3.3.6-design-constraints" />
This section specifies the constraints with the myJym application that would arise from project limitations, external standards, and specific requirements.<br>
***3.3.6.1*** The user shall only be able to save workout the video<br>

<br>

### 3.3.7 Software System Attributes <a name="3.3.7-software-system-attributes" />

<br>

#### 3.3.7.1 Reliability <a name="3.3.7.1-reliability" />
Specifies factors required to establish reliability of the myJym application at the time of delivery.<br>
	
***3.3.7.1.1*** The system shall exit immediately when a user finds an error.
***3.3.7.1.2*** The app shall check that locally stored user information matches what is stored in a database.

<br>

#### 3.3.7.2 Security <a name="3.3.7.2-security" />
Specifies the factors required to guarantee a defined level of availability for the myJym application in regards to the workout videos. <br>	
***3.3.7.2.1*** The user shall only be able to add approved video links to an exercise.

<br>

#### 3.3.7.3 Maintainability <a name="3.3.7.3-maintainability" />
Specifies the factors required to define a level of maintainability for the myJym application. <br>	
***3.3.7.3.1*** App administrators shall be able to remove inappropriate content.<br>

<br>
	
### 3.3.8 Supporting Information <a name="3.3.8-supporting-information" />
N/A<br>

<br>

## <b>3.4 Login & Homepage</b> <a name="3.4-login-&-homepage" /> <!-- 3.4 is Team 5's work -->
The first pages that the user will see. The user will login and then use the homepage to access the various features of the application.<br> 

<br>

### 3.4.1 External Interfaces <a name="3.4.1-external-interfaces" />
Communication with third party applications. The login page requires external interfaces to function. The following list details necessary external interfaces. 
***3.4.1.1*** The login page shall provide the ability to login to an account using login credentials.  <br>
***3.4.1.2*** The system shall send an automated password recovery email to the user on request  
<br>

<br>

### 3.4.2 Functions <a name="3.4.2-functions" />
Operations that the system can perform. The following list details operations that are necessary for the login and homepage to properly function. 
***3.4.2.1*** The home page shall provide access to My Trainer.  <br>
***3.4.2.2*** The home page shall provide access to My Workouts.  <br>
***3.4.2.3*** The home page shall provide access to My Videos.  <br>
***3.4.2.4*** The home page shall provide access to My Gym Map.<br>
***3.4.2.5*** The login page shall provide the user with the ability to recover a lost password.  <br>
***3.4.2.6*** The login page shall provide the user with the ability to create an account. <br>
***3.4.2.7*** The login page shall display an error message when invalid credentials are submitted. <br>
***3.4.2.8*** The system shall check the login credentials against the database. 
<br>

<br>

### 3.4.3 Usability Requirements <a name="3.4.3-usability-requirements" />
Requirements relating to the ease of use of the application.  
***3.4.3.1*** The login page shall inform the user of password requirements.
***3.4.3.2*** The login page shall allow the user to enter login credentials.<br>

<br>

### 3.4.4 Performance Requirements <a name="3.4.4-performance-requirements" />
Requirements relating to the performance metrics of the application. 
***3.4.4.1*** The system shall have the ability to process login credentials.<br>

<br>

### 3.4.5 Logical Database Requirements <a name="3.4.5-logical-database-requirements" />
This section will define what the database will store as the application receives data. 
***3.4.5.1*** The User Data database table shall have a Google authentication key from the Google third party login.
***3.4.5.2*** The User Data database table shall store usernames.
***3.4.5.3*** The User Data database table shall store the passwords.
***3.4.5.4*** The database shall be accessed by the login page when user credentials are submitted through the login page.
***3.4.5.5*** The database shall keep the login credentials of users confidential. <br>

<br>

### 3.4.6 Design Constraints <a name="3.4.6-design-constraints" />
The design constraints of myJym are as follows.
***3.4.6.1*** The myJym app shall be completed in its entirety by the end of Jared's Senior Project class.
***3.4.6.2*** The budget for the myJym app shall be $0.00.<br>

<br>

### 3.4.7 Software System Attributes <a name="3.4.7-software-system-attributes" />
Metrics used to describe myJym’s features.<br>
#### 3.4.7.1 Reliability <a name="3.4.7.1-reliability" />
Applications distinct types of use. 
***3.4.7.1.1*** The app shall require the compliance of personal trainers.
***3.4.7.1.2*** The app shall require an administrator.<br>

<br>

#### 3.4.7.2 Availability <a name="3.4.7.2-availability" />
When myJym will be available for use. 
<br><i>3.4.7.2.1</i><br> The myJym app shall be available on demand of the user.<br>

<br>

#### 3.4.7.3 Security <a name="3.4.7.3-security" />
Measures of what will be done to protect user’s assets 
***3.4.7.3.1*** The system shall encrypt user accounts.
***3.4.7.3.2*** The system shall use a protocol to secure online communications.<br>

<br>

#### 3.4.7.4 Portability <a name="3.4.7.4-portability" />
What will be done to distribute the application. 
***3.4.7.4.1*** The application shall be built with a programming language that can be ported to both iOS and Android.

<br>


## <b>3.5 My Workout</b> <a name="3.5-my-workout" /> <!-- team 3 and 4's stuff-->         
The workout function shall have the ability to let users create their own workouts.

The workout function shall have the ability to let users find premade workouts.

The workout function shall have the ability to let users view previously saved workouts.

<br>

### <b>3.5.1 External Interface</b> <a name="3.5.1-external-interface" />
External interfaces are any interfaces outside the main products that will be created during this project.

<br>

#### <b>3.5.1.1 Database</b> <a name="3.5.1.1-database" />
This list outlines what columns shall be included to create the database.  Specific columns and requirements of the database can be found in section 3.5.
<p class="tab">
<b><i>3.5.1.1.1</b></i> The database shall store workout <b>title</b>.<br>
<b><i>3.5.1.1.2</b></i> The database shall store workout video links.<br>
<b><i>3.5.1.1.3</b></i> The database shall store workout description.<br>
<b><i>3.5.1.1.4</b></i> The database shall store workout <b>sets</b>.<br>
<b><i>3.5.1.1.5</b></i> The database shall store workout <b>reps</b>.<br>
<b><i>3.5.1.1.6</b></i> The database shall store workout <b>tags</b>.<br>
</p>

<br>

#### <b>3.5.1.2 Video Provider</b> <a name="3.5.1.2-video provider" />
The **API** for the video provider will be used to share videos on workout techniques and forms, and how to use gym exercise equipment. This will be used according to the product owner and stakeholder’s decisions.
<p class="tab">
<b><i>3.5.1.2.1</b></i> <b>Gymgoers</b> shall have the ability to access workout videos.<br>
</p>

<br>
    
### <b>3.5.2 Functions</b> <a name="3.5.2-functions" />
This section is responsible for explaining what the myJym app is expected to perform. These functions are divided into sub-sections that explain the procedure, performance and tasks of the myJym app.

<br>

#### <b>3.5.2.1 Create Workout</b> <a name="3.5.2.1-create-workout" />
Create workout is a page within the app that allows users to create workouts to their own specifications.  The following list is what is needed to achieve that functionality.
<p class="tab">
<b><i>3.5.2.1.1</b></i> The workout creation shall allow the <b>user</b> to specify a workout name.<br>
<b><i>3.5.2.1.2</b></i> The workout creation shall allow the user to specify a muscle group to workout.<br>
<b><i>3.5.2.1.3</b></i> The workout creation shall allow the user to specify an amount of <b>reps</b>.<br>
<b><i>3.5.2.1.4</b></i> The workout creation shall allow the user to specify an amount of <b>sets</b>.<br>
<b><i>3.5.2.1.5</b></i> The workout creation shall allow the user to embed a video link.<br>
</p>

<br>

#### <b>3.5.2.2 Find Workout</b> <a name="3.5.2.2-find-workout" />
Find workout is a page within the app that allows users to find workouts that other users have already created. The following list is what is needed to achieve that functionality.
<p class="tab">
<b><i>3.5.2.2.1</b></i> The find workout page shall have the ability to search by predetermined <b>tag</b>s.<br>
<b><i>3.5.2.2.2</b></i> One of the tags that can be used to search by shall be <b>author</b>.<br>
<b><i>3.5.2.2.3</b></i> One of the tags that can be used to search by shall be <b>name of workout</b>.<br>
<b><i>3.5.2.2.4</b></i> One of the tags that can be used to search by shall be <b>length</b>.<br>
<b><i>3.5.2.2.5</b></i> One of the tags that can be used to search by shall be <b>workout type</b>.<br>
<b><i>3.5.2.2.6</b></i> One of the tags that can be used to search by shall be <b>difficulty</b>.<br>
<b><i>3.5.2.2.7</b></i> One of the tags that can be used to search by shall be <b>equipment type</b>.<br>
<b><i>3.5.2.2.8</b></i> One of the tags that can be used to search by shall be <b>muscle groups</b>.<br>
<b><i>3.5.2.2.9</b></i> The user shall have the ability to save a workout they find to their saved workouts list.<br>
</p>

<br>

#### <b>3.5.2.3 Saved Workout</b> <a name="3.5.2.3-saved-workout" />
Saved workout is a page within the app that allows users to save a workout that they created or found. The following list is what is needed to achieve that functionality.
<p class="tab">
<b><i>3.5.2.3.1</b></i> The user shall have the option to edit the workout.<br>
<b><i>3.5.2.3.2</b></i> Selecting edit workout shall redirect the user back to the create workout page with all the workout information filled in.<br>
<b><i>3.5.2.3.3</b></i> The user shall have the option to immediately start the workout.<br>
<b><i>3.5.2.3.4</b></i> Selecting start workout shall redirect the user to the workout in progress page.<br>
<b><i>3.5.2.3.5</b></i> The user shall have the option to delete a previously saved workout.<br>
</p>

<br>

#### <b>3.5.2.4 Workout in Progress Page</b> <a name="3.5.2.4-workout-in-progress-page" />
Workout in progress is a page within the app that displays the current workout in progress. The following list is what is needed to achieve that functionality.
<p class="tab">
<b><i>3.5.2.4.1</b></i> The workout in progress page shall guide the user through their workout.<br>
<b><i>3.5.2.4.2</b></i> The workout in progress page shall display the workout information for the selected workout.<br>
</p>

<br>
	
#### <b>3.5.2.5 My Video Page </b> <a name="3.5.2.5-my-video-page" />
This section defines the workout in progress function for the my workout feature.
<p class="tab">
<b><i>3.5.2.5.1</b></i> My Video page shall display a workout title. [3.3.2.1.1] (Technique: demonstration)<br>
<b><i>3.5.2.5.2</b></i> My Video page shall display an equipment name. [3.3.2.1.2] (Technique: demonstration)<br>
<b><i>3.5.2.5.3</b></i> My Video page shall display a workout video. [3.3.2.1.3] (Technique: demonstration)<br>
<b><i>3.5.2.5.4</b></i> My Video page shall provide a save video button. [3.3.2.1.4] (Technique: demonstration)<br>
</p>

<br>
	
### <b>3.5.3 Usability Requirements</b> <a name="3.5.3-usability-requirements" />
This section explains the usability and quality of the use requirements and objectives for the myJym application including measurable effectiveness and satisfaction criteria for the my workout feature.
<p class="tab">
<b><i>3.5.3.1</b></i>The user shall be able to create a workout.<br>
<b><i>3.5.3.2</b></i>The user shall be able to find a workout.<br>
<b><i>3.5.3.3</b></i>The user shall be able to save a workout.<br>
<b><i>3.5.3.4</b></i>The user shall be able to start a workout.<br>
<b><i>3.5.3.5</b></i>The user shall be able to see workout progress.<br>
</p>

<br>

### <b>3.5.4 Performance Requirements</b> <a name="3.5.4-performance-requirments" />
For the myJym application to meet performance standards there are specific requirements that need to be met. These requirements are specified below.
<p class="tab">
<b><i>3.5.4.1</b></i> The user shall only be able to save one video link for a specific exercise.<br>
<b><i>3.5.4.2</b></i> The system shall support a configurable amount of workouts.<br>
<b><i>3.5.4.3</b></i> The system shall support a configurable amount of tags per workout.<br>
</p>

<br>

### <b>3.5.5 Logical Database Requirements</b> <a name="3.5.5-logical-database-requirments" />
The myJym database shall store all the tables that are necessary for storing information required by the application.
<p class="tab">
<b><i>3.5.5.1</b></i> The workout table shall contain an exercise title column.<br>
<b><i>3.5.5.2</b></i> The workout table shall contain a tag column.<br>
<b><i>3.5.5.3</b></i> The workout table shall contain a rep column.<br>
<b><i>3.5.5.4</b></i> The workout table shall contain a set column.<br>
<b><i>3.5.5.5</b></i> The workout table shall contain a description column.<br>
<b><i>3.5.5.6</b></i> The workout table shall contain a video link column.<br>
<b><i>3.5.5.7</b></i> The workout table shall contain a workout id column that acts as a **primary key**.<br>
</p>

<br>

### <b>3.5.6 Design Constraints</b> <a name="3.5.6-design-constraints" />
This section specifies the constraints with the myJym application that would arise from project limitations, external standards, and specific requirements.
<p class="tab">
<b><i>3.5.6.1</b></i> The user shall only be able to add approved video links from a video provider to an exercise.<br>
<b><i>3.5.6.2</b></i> The user shall only be able to input an integer into the rep field.<br>
<b><i>3.5.6.3</b></i> The user shall only be able to input an integer into the set field.<br>
<b><i>3.5.6.4</b></i> The user shall have to add a title to the workouts they create.<br>
</p>

<br>

### <b>3.5.7 Software System Attributes</b> <a name="3.5.7-software-system-attributes" />
This section specifies the required attributes of the myJym application explaining the reliability, security, and maintainability.

<br>

#### <b>3.5.7.1 Reliability</b> <a name="3.5.7.1-reliability" />
Specifies factors required to establish reliability of the myJym application at the time of delivery.
<p class="tab">
<b><i>3.5.7.1.1</b></i> The system shall exit immediately when user finds an error.<br>
<b><i>3.5.7.1.2</b></i> The app shall check that locally stored user information matches what is stored in database.<br>
</p>

<br>

#### <b>3.5.7.2 Security</b> <a name="3.5.7.2-security" />
Specifies the factors required to guarantee a defined level of availability for the myJym application in regards to the workout videos.
<p class="tab">
<b><i>3.5.7.2.1</b></i> The user shall only be able to add approved video links from a video provider to an exercise.<br>
</p>

<br>

#### <b>3.5.7.3 Maintainability</b> <a name="3.5.7.3-maintainability" />
Specifies the factors required to define a level of maintainability for the myJym application.
<p class="tab">
<b><i>3.5.7.3.1</b></i> App administrators shall be able to remove <b>inappropriate</b> content.
</p>

<br>

### <b>3.8.3 Supporting Information</b>
Not applicable for the my workout feature.

<br>
<br>

# <b>4.0 Validation</b> <a name="4.0-validation" />
This section will validate that all features from section 3 will be in working order.    

It was written in the same workflow order as section 3. Thus, the ideal order to read this section of the document is:
| Section | Title Name|
|---------|----------------------------------------------------------------------|
| 4.4 | Login Page & Homepage | 
| 4.1 | My Trainer |
| 4.5 | My Workout |
| 4.3 | My Video |
| 4.2 | My Gym Map |   

<br>

## <b>4.1 My Trainer</b> <a name="4.1-my-trainer" />

<!-- team 1's stuff--> 
### <b>4.1.1 External Interfaces Verification</b> <a name="4.1.1-external-interface-verification" />
This section will define the verification for the external interfaces for the My Trainer section.
<p class="tab">
<b><i>4.1.1.1</b></i> Verify the My trainer portion is a page accessible through the homepage. [3.1.1.1] (Technique: demonstration) <br>
</p>

<br>

#### <b>4.1.1.1 Google Authentication Verification</b> <a name="4.1.1.1-google-authentication-verification" />
Verify the google authentication.
<p class="tab">
<b><i>4.1.1.1.1</b></i> Verify that google authentication API shall be used by users to login to their accounts. [3.1.1.1.1] (Technique: demonstration) <br>
<b><i>4.1.1.1.2</b></i> Verify that all users shall be able to login to their account using a google account. [3.1.1.1.2] (Technique: demonstration) <br>
<b><i>4.1.1.1.3</b></i> Verify that all users shall be able to create an account using a google account. [3.1.1.1.3] (Technique: demonstration) <br>
</p>

<br> 

### <b>4.1.2 Functions Verification</b> <a name="4.1.2-functions-verifications" />
This section will verify all the functions of the my trainer page.

<p class="tab">
<b><i>4.1.2.1</b></i> Verify the myJym application shall send users Notifications. [3.1.2.1.1] (Technique: demonstration) <br>
<b><i>4.1.2.2</b></i> Verify the My Trainer page shall allow users to view trainer profiles. [3.1.2.1.2] (Technique: demonstration) <br>
</p>

<br>

#### <b>4.1.2.1 Notifications Verification</b> <a name="4.1.2.1-notifications-verifications" />
This section defines the verification for notifications.
<p class="tab">
<b><i>4.1.2.1.1</b></i> Verify the myJym application shall send users Notifications. [3.1.2.1.1] (Technique: demonstration) <br>
<b><i>4.1.2.1.2</b></i> Verify the My Trainer page shall allow users to view trainer profiles. [3.1.2.1.2] (Technique: demonstration) <br>
</p>

<br>

#### <b>4.1.2.2 View Trainer Profile Verification</b> <a name="4.1.2.2-view-trainer-profile-verifications" />
This section defines the verification for viewing trainer profiles.
<p class="tab">
<b><i>4.1.2.2.1</b></i> Verify the trainer profile shall be viewable by gymgoers. [3.1.2.2.1] (Technique: demonstration) <br>
<b><i>4.1.2.2.2</b></i> Verify the trainer profile shall display a picture of the trainer. [3.1.2.2.2] (Technique: demonstration) <br>
<b><i>4.1.2.2.3</b></i> Verify the trainer profile shall display a short biography of the trainer. [3.1.2.2.3] (Technique: demonstration) <br>
<b><i>4.1.2.2.4</b></i> Verify the trainer profile shall display a clickable link to the trainer’s videos on a video provider. [3.1.2.2.4] (Technique: demonstration) <br>
<b><i>4.1.2.2.5</b></i> Verify the “View Workouts” shall be an option on the Trainer profile that allows the user to view a trainer’s created workouts. [3.1.2.2.5] (Technique: demonstration) <br>
<b><i>4.1.2.2.6</b></i> Verify the “Message Trainer” shall be an option on the Trainer profile that allows the user to send a message to the trainer. [3.1.2.2.6] (Technique: demonstration) <br>
<b><i>4.1.2.2.7</b></i> Verify trainer profiles shall store a trainers first name [3.1.2.2.7] (Technique: demonstration) <br>
<b><i>4.1.2.2.8</b></i> Verify trainer profiles shall store a trainer’s last name. [3.1.2.2.8] (Technique: demonstration) <br>
<b><i>4.1.2.2.9</b></i> Verify trainer profiles shall store a trainer’s email. [3.1.2.2.9] (Technique: demonstration) <br>
<b><i>4.1.2.2.10</b></i> Verify the system shall create a unique ID for each trainer. [3.1.2.2.10] (Technique: demonstration) <br>
<b><i>4.1.2.2.11</b></i> Verify the system shall create a personal key for each trainer. [3.1.2.2.11] (Technique: demonstration) <br>
</p>

<br>

#### <b>4.1.2.3 Update Profile Verification</b> <a name="4.1.2.3-update-profile-verifications" />
This section defines the verification for updating profiles.
<p class="tab">
<b><i>4.1.2.3.1</b></i> Verify update Profile shall allow any user to update their own picture. [3.1.2.3.1] (Technique: demonstration) <br>
<b><i>4.1.2.3.2</b></i> Verify update Profile shall allow any user to update a biography text-field. [3.1.2.3.2] (Technique: demonstration) <br>
<b><i>4.1.2.3.3</b></i> Verify update Profile shall allow any user to update their personal YouTube link. [3.1.2.3.3] (Technique: demonstration) <br>
<b><i>4.1.2.3.4</b></i> Verify update Profile shall allow any user to update their first and last name. [3.1.2.3.4] (Technique: demonstration) <br>
</p>

<br>

#### <b>4.1.2.4 Search Trainer Verification</b> <a name="4.1.2.4-search-trainer-verifications" />
This section defines the verification for searching trainers.
<p class="tab">
<b><i>4.1.2.4.1</b></i> Verify the system shall have a search bar. [3.1.2.4.1] (Technique: demonstration) <br>
<b><i>4.1.2.4.2</b></i> Verify a search bar shall be viewable by the user. [3.1.2.4.2] (Technique: demonstration) <br>
<b><i>4.1.2.4.3</b></i> Verify search trainer shall allow a user to search for a trainer by name. [3.1.2.4.3] (Technique: demonstration) <br>
<b><i>4.1.2.4.4</b></i> Verify search trainer shall allow a user to search for a trainer by location. [3.1.2.4.4] (Technique: demonstration) <br>
<b><i>4.1.2.4.5</b></i> Verify search trainer shall allow a user to search for a trainer by workouts. [3.1.2.4.5] (Technique: demonstration) <br>
</p>

<br>

#### <b>4.1.2.5</b> Message Trainer Verification<a name="4.1.2.5-message-trainer-verifications" />
This section defines the verification for messaging trainers.
<p class="tab">
<b><i>4.1.2.5.1</b></i> Verify message Trainer shall give a user the ability to send messages to a trainer. [3.1.2.5.1] (Technique: demonstration) <br>
<b><i>4.1.2.5.2</b></i> Verify message Trainer shall list messages in chronological order. [3.1.2.5.2] (Technique: demonstration) <br>
<b><i>4.1.2.5.3</b></i> Verify messages Trainer shall be able to handle messages containing text. [3.1.2.5.3] (Technique: demonstration) <br>
<b><i>4.1.2.5.4</b></i> Verify message Trainer shall be able to handle messages containing links.  [3.1.2.5.4] (Technique: demonstration) <br>
</p>

<br>

#### <b>4.1.2.6 Message Users Verification</b> <a name="4.1.2.6-message-users-verifications" />
This section defines the verification for messaging users.
<p class="tab">
<b><i>4.1.2.6.1</b></i> Verify message users shall give trainers the ability to send messages to users. [3.1.2.6.1] (Technique: demonstration) <br>
<b><i>4.1.2.6.2</b></i> Verify message users shall create a chat between trainer and users. [3.1.2.6.2] (Technique: demonstration) <br>
<b><i>4.1.2.6.3</b></i> Verify message users shall list messages in chronological order. [3.1.2.6.3] (Technique: demonstration) <br>
<b><i>4.1.2.6.4</b></i> Verify messages Trainer shall be able to handle messages containing text. [3.1.2.6.4] (Technique: demonstration) <br>
<b><i>4.1.2.6.5</b></i> Verify message Trainer shall be able to handle messages containing links [3.1.2.6.5] (Technique: demonstration) <br>
</p>

<br>

### <b>4.1.3 Usability Requirements Verification</b> <a name="4.1.3-usability-requirements-verifications" />
This section defines the verification for usability requirements.
<p class="tab">
<b><i>4.1.3.1</b></i> Verify the system is easy to learn for both novices and users with experience from similar systems through user testing. [3.1.3.1] (Technique: demonstration) <br>
<b><i>4.1.3.2</b></i> Verify users familiar with similar systems is able to create a new account with minimal errors through user testing. [3.1.3.2] (Technique: demonstration) <br>
<b><i>4.1.3.3</b></i> Verify the system is designed to be simple to use for frequent users through user testing. [3.1.3.3] (Technique: demonstration) <br>
<b><i>4.1.3.4</b></i> Verify that frequent users are given an option to be able to access their account without having to sign in each session. [3.1.3.4] (Technique: demonstration) <br>
<b><i>4.1.3.5</b></i> Verify tasks are able to be completed by the frequent user quickly and efficiently through user testing. [3.1.3.5] (Technique: demonstration) <br>
<b><i>4.1.3.6</b></i> Verify the system is clear and well defined through user surveying. [3.1.3.6] (Technique: demonstration) <br>
<b><i>4.1.3.7</b></i> Verify users experienced with this system are able to login to their account quickly(within 5 seconds of opening the app) through user testing. [3.1.3.7] (Technique: demonstration) <br>
<b><i>4.1.3.8</b></i> Verify a new user is able to navigate to any desired option quickly and efficiently through user testing. [3.1.3.8] (Technique: demonstration) <br>
<b><i>4.1.3.9</b></i> Verify the system receives a high rating by test groups. [3.1.3.9] (Technique: demonstration) <br>
<b><i>4.1.3.10</b></i> Verify task failure by the system is kept to a minimum through user testing. [3.1.3.10] (Technique: demonstration) <br>
<b><i>4.1.3.11</b></i> Verify the system is able to allow users to try things and undo them through user testing. [3.1.3.11] (Technique: demonstration) <br>
<b><i>4.1.3.12</b></i> Verify the ability to undo is incorporated into any part of the system that stores information, including tasks. [3.1.3.12] (Technique: demonstration) <br>
<b><i>4.1.3.13</b></i> Verify the system is created with elements that ensure that it is accessible to adults ranging from 18-40. [3.1.3.13] (Technique: demonstration) <br>
</p>

<br>

### <b>4.1.4 Performance Requirements Verification</b> <a name="4.1.4-performance-requirments-verification" />
This section defines the verification performance requirements.
<p class="tab">
<b><i>4.1.4.1</b></i> Verify that my trainer page shall load when the user navigates to my trainer page. [3.1.4.1] (Technique: test) <br>
<b><i>4.1.4.2</b></i> Verify that the trainer shall receive messages soon after the author sends the message. [3.1.4.2] (Technique: test) <br>
<b><i>4.1.4.3</b></i> Verify that the trainer shall be able to send messages after clicking the send button in the built-in messenger. [3.1.4.3] (Technique: test) <br>
<b><i>4.1.4.4</b></i> Verify that notifications for the trainer shall be received at the same time as when the message comes in. [3.1.4.4] (Technique: test) <br>
<b><i>4.1.4.5</b></i> Verify that notifications from the trainer shall be received at the same time the recipient receives the message. [3.1.4.5] (Technique: test) <br>
<b><i>4.1.4.6</b></i> Verify that the trainer profiles on the web shall be loaded soon after the settings button has been clicked. [3.1.4.6] (Technique: test) <br>
<b><i>4.1.4.7</b></i> Verify that the trainer profiles on the mobile app shall be loaded soon after the settings button has been clicked. [3.1.4.7] (Technique: test) <br>
<b><i>4.1.4.8</b></i> Verify that the trainer search results on the web shall load up soon after the search has been entered in. [3.1.4.8] (Technique: test) <br>
<b><i>4.1.4.9</b></i> Verify that the trainer search results on the mobile app shall load up soon after the search has been entered in. [3.1.4.9] (Technique: test) <br>
</p>

<br>

### <b>4.1.5 Logical Database Requirements Verification</b> <a name="4.1.5-logical-database-requirments-verification" />
This will verify all of the items for logical databases.

<br>

#### <b>4.1.5.1 Types of information used by various functions verification</b> <a name="4.1.5.1-types-of-information-used-by-various-functions-verifications" />
This section defines the verification for types of information used by various functions.
<p class="tab">
<b><i>4.1.5.1.1</b></i> Verify My Trainer shall store a trainers first name [3.1.5.1.1] (Technique: demonstration) <br>
<b><i>4.1.5.1.2</b></i> Verify My Trainer shall store a trainer’s last name. [3.1.5.1.2] (Technique: demonstration) <br>
<b><i>4.1.5.1.3</b></i> Verify My Trainer shall store a trainer’s email. [3.1.5.1.3] (Technique: demonstration) <br>
<b><i>4.1.5.1.4</b></i> Verify The system shall create a trainer ID for each trainer. [3.1.5.1.4] (Technique: demonstration) <br>
</p>

<br>

#### <b>4.1.5.2 Frequency of use verification</b> <a name="4.1.5.2-frequency-of-use-verifications" />
This section defines the verification for frequency of use.
<p class="tab">
<b><i>4.1.5.2.1</b></i> Verify Email data types shall be used for a single account. [3.1.5.2.1] (Technique: demonstration) <br>
</p> 

<br>

#### <b>4.1.5.3 Accessing Capabilities verification</b> <a name="4.1.5.3-accessing-capabilities-verifications" />
This section defines the verification for accessing capabilities.
<p class="tab">
<b><i>4.1.5.3.1</b></i> Verify Trainers shall have access to User first name. [3.1.5.3.1] (Technique: demonstration) <br>
<b><i>4.1.5.3.2</b></i> Verify Trainers shall have access to User last name. [3.1.5.3.2] (Technique: demonstration) <br>
<b><i>4.1.5.3.3</b></i> Verify Trainers shall have access to User goals. [3.1.5.3.3] (Technique: demonstration) <br>
<b><i>4.1.5.3.4</b></i> Verify Trainers shall have access to User workout plan. [3.1.5.3.4] (Technique: demonstration) <br>
<b><i>4.1.5.3.5</b></i> Verify Trainers shall have access to User gym. [3.1.5.3.5] (Technique: demonstration) <br>
</p>

<br>

#### <b>4.1.5.4 Integrity Constraints verification</b> <a name="4.1.5.4-integrity-constraints-verifications" />
This section defines the verification for integrity constraints.
<p class="tab">
<b><i>4.1.5.4.1</b></i> Verify Data entries shall be possible entries. [3.1.5.4.1] (Technique: demonstration) <br>
<b><i>4.1.5.4.2</b></i> Verify Impossible data entries shall not be allowed. [3.1.5.4.2] (Technique: demonstration) <br>
<b><i>4.1.5.4.3</b></i> Verify Data entries shall be verified to ensure it is possible. [3.1.5.4.3] (Technique: demonstration) <br>
<b><i>4.1.5.4.4</b></i> Verify The database shall have entity integrity. [3.1.5.4.4] (Technique: demonstration) <br>
</p>

<br>

#### <b>4.1.5.5 Security verification</b> <a name="4.1.5.5-security-verifications" />
This section defines the verification for security.
<p class="tab">
<b><i>4.1.5.5.1</b></i> Verify Trainer accounts shall utilize google sign-in to access their account. [3.1.5.5.1] (Technique: demonstration) <br>
<b><i>4.1.5.5.2</b></i> Verify User accounts shall utilize google sign-in to access their account. [3.1.5.5.2] (Technique: demonstration) <br>
<b><i>4.1.5.5.3</b></i> Verify Trainers shall only have one account. [3.1.5.5.3] (Technique: demonstration) <br>
<b><i>4.1.5.5.4</b></i> Verify Gymgoers shall only have one account. [3.1.5.5.4] (Technique: demonstration) <br>
<b><i>4.1.5.5.5</b></i> Verify Admin accounts shall have access to all accounts [3.1.5.5.5] (Technique: demonstration) <br>
</p>

<br>

### <b>4.1.6 Design Constraints Requirements Verification</b> <a name="4.1.6-design-constraints-requirements-verification" />
This section will verify the design constraints requirements.
<p class="tab">
<b><i>4.1.6.1</b></i> Verify system users shall specify the requirements for My Trainer and ensure to understand these requirements meet their demands and needs. [3.1.6.1] (Technique: demonstration) <br>
<b><i>4.1.6.2</b></i> Verify users shall specify changes to the requirements.  [3.1.6.2] (Technique: demonstration) <br>
<b><i>4.1.6.3</b></i> Verify system managers shall use the requirements documentation to plan a bid for the system to plan the system development process for My Trainer. [3.1.6.3] (Technique: demonstration) <br>
<b><i>4.1.6.4</b></i> Verify system engineers shall use the requirements to understand what system is being developed. [3.1.6.4] (Technique: demonstration) <br>
<b><i>4.1.6.5</b></i> Verify System testing engineers shall use the requirements for the purpose of development of validation tests for the system of My Trainer. [3.1.6.5] (Technique: demonstration) <br>
<b><i>4.1.6.6</b></i> Verify System maintenance managers shall use requirements to understand the system and the relationship between its parts. [3.1.6.6] (Technique: demonstration) <br>
<p>

<br>

### <b>4.1.7 Software System Attributes Verification</b> <a name="4.1.7-software-system-attributes-verification" />
This section will verify all things under software system attributes.

<br>

#### <b>4.1.7.1 Reliability Verification</b> <a name="4.1.7.1-reliability-verification" />
<p class="tab">
<b><i>4.1.7.1.1</b></i> Verify applications shall not have errors within the codes to cause applications to close or crash. [3.1.7.1.1] (Technique: inspection) <br>
<b><i>4.1.7.1.2</b></i> Verify there will be functions within the software that perform verifications to notice errors before the application is crashed. [3.1.7.1.2] (Technique: inspection) <br>
<b><i>4.1.7.1.3</b></i> Verify the system shall verify the information that is matched between the server and the application. [3.1.7.1.3] (Technique: inspection) <br>
</p>

<br>

#### <b>4.1.7.2 Security</b> <a name="4.1.7.2-security-verification" />
<p class="tab">
<b><i>4.1.7.2.1</b></i> Verify user shall have password protection and encryption. [3.1.7.2.1] (Technique: inspection) <br>
<b><i>4.1.7.2.2</b></i> Verify the user account creation process shall be safe and secure. [3.1.7.2.2] (Technique: inspection) <br>
<b><i>4.1.7.2.3</b></i> Verify user’s account and personal information shall be hidden from all other unauthorized users and parties. [3.1.7.2.3] (Technique: inspection) <br>
<b><i>4.1.7.2.4</b></i> Verify users shall be required to provide an email and password during the account creation process. [3.1.7.2.4] (Technique: inspection) <br>
</p>

<br>

#### <b>4.1.7.3 Data privacy</b> <a name="4.1.7.3-data-privacy-verification" />
<p class="tab">
<b><i>4.1.7.3.1</b></i> Verify that user data shall be hidden from all other users and parties. [3.1.7.3.1] (Technique: inspection) <br>
<b><i>4.1.7.3.2</b></i> Verify login information [3.1.7.3.2] (Technique: inspection) <br>
<b><i>4.1.7.3.3</b></i> Verify creating an account shall be safe. [3.1.7.3.3] (Technique: inspection) <br>
<b><i>4.1.7.3.4</b></i> Verify all users shall be allowed to login securely. [3.1.7.3.4] (Technique: inspection) <br>
<b><i>4.1.7.3.5</b></i> Verify once a user logs out from the account, all user information shall be removed from the login screen.  [3.1.7.3.5] (Technique: inspection) <br> 
</p>

<br>

#### <b>4.1.7.4 Maintainability</b> <a name="4.1.7.4-maintainability-verification" />
<p class="tab">
<b><i>4.1.7.4.1</b></i> Verify users shall be allowed to report to the administration team if they forget their password, and need to have a reset password email sent to their personal email that has been registered on their myJym account. [3.1.7.4.1] (Technique: inspection) <br>
<b><i>4.1.7.4.2</b></i> Verify an automatic email shall be sent to the user's email address to allow the user to reset their password. [3.1.7.4.2] (Technique: inspection) <br>
</p>

<br>

#### <b>4.1.7.5 Portability</b> <a name="4.1.7.5-maintainability-verification" />
<p class="tab">
<b><i>4.1.7.5.1</b></i> Verify system Database shall store user information. [3.1.7.5.1] (Technique: inspection) <br>
<b><i>4.1.7.5.2</b></i> Verify myJym application shall run on both Android and iOS mobile interface. [3.1.7.5.2] (Technique: inspection) <br>
</p>

<br>

### <b>4.1.8 Supporting Information Verification</b> <a name="4.1.8-supporting-information-verification" />
N/A

<br>
<br>

<!-- Team 2> -->
## <b> 4.2 Gym Map Verification </b> <a name=4.2>
This section details the verification for the Gym Map (SRS 3.2) section. <br>

<br>

### <b>4.2.1 Map External Interfaces Verification</b> <a name="4.2.1" />
This section defines the verification for the gym map external interface requirements.
<p class="tab">
<b><i>4.2.1.1</b></i> Verify that the map utilizes the System Database to generate the map. (Technique: Inspection) [3.2.1.1] <br>
<b><i>4.2.1.2</b></i> Verify that the map search bar obtains user data from the System Database. (Technique: Inspection) [SRS 3.2.1.2] <br>

<br>

### <b>4.2.2 Map Functions Verification </b> <a name="4.2.2" />
This section defines the verification for the gym map functions.
<p class="tab">

<br>

### <b>4.2.2.1 Map Display Verification</b> <a name="4.2.2" />
This section defines the verification for the gym map display.
<p class="tab">
<b><i>4.2.2.1.1</b></i> Verify the map organizes gym equipment according to a layout file. (Technique: Inspection) [3.2.2.1.1] <br>
<b><i>4.2.2.1.2</b></i> Verify the map organizes gym services according to a layout file. (Technique: Inspection) [3.2.2.1.2] <br>
<b><i>4.2.2.1.3</b></i> Verify the map properly refreshes when an error occurs. (Technique: Test) [3.2.2.1.2] <br>
<b><i>4.2.2.1.4</b></i> Verify an administrator can modify the map layout. (Technique: Demonstration) [3.2.2.1.4] <br>
<b><i>4.2.2.1.5</b></i> Verify a map tutorial opens when the map is first opened. (Technique: Demonstration) [3.2.2.1.5] <br>

<br>

### <b>4.2.2.2 Map Search Verification </b> <a name="4.2.2" />
This section defines the verification for the gym map functions.
<p class="tab">
<b><i>4.2.2.2.1</b></i> Verify that the map search bar performs validation on inputs matching them to gym functions. (Technique: Inspection)[3.2.2.2.1] <br>
<b><i>4.2.2.2.2</b></i> Verify that the search bar has functionality to locate gym functions. (Technique: Demonstration) [3.2.2.2.2] <br>
<b><i>4.2.2.2.3</b></i> Verify that the map search bar is a modeless interface allowing for interaction with other page elements while it is open. (Technique: Inspection) [3.2.2.2.3] <br>
<b><i>4.2.2.2.4</b></i> Verify that facilities in the gym are searchable by name through the map search bar. (Technique: Demonstration) [3.2.2.2.4] <br>

<br>
	
### <b> 4.2.2.3 Map Navigation Verification</b> 
This section describes the verification for the map navigation.
<p class="tab">
<b><i>4.2.2.3.1</b></i> Verify that the map has a scrollable edge. (Technique: Demonstration)  [3.2.2.3.1] <br>
<b><i>4.2.2.3.2</b></i> Verify that the map supports zooming, detecting when a zoom request is made. (Technique: Demonstration) [3.2.2.3.2] <br>
<b><i>4.2.2.3.3</b></i>  Verify that gym function icons are interactable to view options related to that function. (Technique: Demonstration) [3.2.2.3.3] <br>

<br>

### <b>4.2.3 Map Usability Requirements Verification </b> <a name="4.2.3" />
This section defines the verification for the gym map usability requirements.
<p class="tab">
<b><i>4.2.3.1</b></i>  Verify the map is intuitive so the user can easily form a mental model of its workings. (Technique: Inspection) [3.2.3.1] <br>
<b><i>4.2.3.2</b></i>  Verify a gym goer can quickly identify where they should be in the gym to complete their desired activity. (Technique: Demonstration) [3.2.3.2] <br>
<b><i>4.2.3.3</b></i>  Verify that map uses simple, intelligent command formats. (Technique: Demonstration) [3.2.3.4]<br>
<b><i>4.2.3.4</b></i>  Verify the map icons and interfaces use simple command formats to ensure users understand map functionalities. (Technique: Inspection) [3.2.3.4] <br>
<b><i>4.2.3.5</b></i>  Verify when a task failure occurs the map stops its operation and refreshes. (Technique: Test) [3.2.3.5] <br>
<b><i>4.2.3.6</b></i>  Verify map iconography is consistent with commonly recognized symbols. (Technique: Inspection) [3.2.3.6] <br>

<br>

### <b>4.2.4 Map Performance Requirements Verification </b> <a name="4.2.4" />
This section defines the verification for the gym map performance requirements.
<p class="tab">
<b><i>4.2.4.1</b></i>  Verify the map prioritizes loading the graphical display elements prior to lower priority tasks. (Technique: Inspection) [3.2.4.1] <br>
<b><i>4.2.4.2</b></i>  Verify the map search functionality returns results in higher algorithm efficiency than** O**(n log n). (Technique: Test) [3.2.4.2] <br>
<b><i>4.2.4.3</b></i>  Verify the map allows for interaction with elements after a predetermined time post loading. (Technique: Test) [3.2.4.3] <br>

<br>

### <b>4.2.5 Map Logical Database Requirements Verification </b> <a name="4.2.5" />
This section defines the verification for the gym map logical database requirements.
<p class="tab">

<br>

### <b>4.2.5.1 Type of Information Used by Various Functions Verification </b> <a name="4.2.5.1" />
This section defines the verification for the types of information used by functions of the gym map:
<p class="tab">
<b><i>4.2.5.1.1</b></i>  Verify the icons are stored as a valid data construct. (Technique: Test) [3.2.5.1.1] <br>
<b><i>4.2.5.1.2</b></i>  Verify the map retrieves the search data correctly. (Technique: Test) [3.2.5.1.2] <br>
	
<br>

### <b>4.2.5.2 Frequency of Use Verification </b> <a name="4.2.5.2" />
This section defines the verification for the frequency of use:
<p class="tab">
<b><i>4.2.5.2.1</b></i>  Verify the map icons are loaded into memory from the **System Database** when the view is selected. (Technique: Test) [3.2.5.2.1] <br>
<b><i>4.2.5.2.2</b></i>  Verify the map search functionality is accessible on demand. (Technique: Demonstration) [3.2.5.2.2] <br>

<br>

### <b>4.2.5.3 Accessing Capabilities Verification </b> <a name="4.2.5.3" />
This section defines the verification for the accessing capabilities of the gym map:
<p class="tab">
<b><i>4.2.5.3.1</b></i>  Verify that the map is accessible from the homepage of the myJym application. (Technique: Demonstration) [3.2.5.2.1] <br>
<b><i>4.2.5.3.2</b></i>  Verify the map has access to the **System Database** to access gym equipment locations. (Technique: Inspection) [3.2.5.2.2] <br>

<br>
	
### <b>4.2.5.4 Data Entity Relationships Verification </b> <a name="4.2.2.5.4" />
This section defines the verification for data entity relationships of the gym map:
<p class="tab">
<b><i>4.2.5.4.1</b></i>  Verify that the map has access to the **System Database** to return search results. (Technique: Inspection) [3.2.5.3.1] <br>
<b><i>4.2.5.4.2</b></i>  Verify that the map handles data for the exercise machine locations. (Technique: Inspection) [3.2.5.3.2] <br>
<b><i>4.2.5.4.3</b></i>  Verify that the map handles data for the exercise machine images. (Technique: Inspection) [3.2.5.3.3] <br>

<br>

### <b>4.2.5.5 Integrity Constraints Verification </b> <a name="4.2.5.5" />
This section defines the verification for the gym map integrity constraints:
<p class="tab">
<b><i>4.2.5.5.1</b></i>  Verify that the map handles data for the map search bar results. (Technique: Inspection) [3.2.5.4.1] <br>
<b><i>4.2.5.5.2</b></i>  Verify that map icons are entries to the database. (Technique: Inspection) [3.2.5.4.2] <br>
<b><i>4.2.5.5.3</b></i>  Verify that map data is formatted to match the conventions of the database. (Technique: Inspection) [3.2.5.4.3] <br>

<br>
	
### <b>4.2.5.6 Security Verification </b> <a name="4.2.5.6" />
This section defines the verification for the gym map security:
<p class="tab">
<b><i>4.2.5.6.1</b></i>  Verify that data used for the map is only accessible by the functions of myJym. (Technique: Test) [3.2.5.6.1] <br>

<br>
	
### <b>4.2.5.7 Design Constraints Verification </b> <a name="4.2.5.7" />
This section defines the verification for the gym map design constraints:
<p class="tab">
<b><i>4.2.5.7.1</b></i> Verify that the interactable map features provides sufficient **Pixels Per Inch** that the average human is able to cleanly select them. (Technique: Inspection) [3.2.6.1] <br>

<br>
	
### <b>4.2.5.8 Software System Attributes Verification </b> <a name="4.2.5.8" />
This section defines the verification for the gym map software system attributes:
<p class="tab">
<b><i>4.2.5.8.1</b></i> Verify that the map is available when the application has been opened to the home page. (Technique: Demonstration)  [3.2.7.1] <br>
<b><i>4.2.5.8.2</b></i> Verify that the map is available offline when no internet connectivity is available. (Technique: Demonstration) [3.2.7.2] <br>

<br>
	
### <b>4.2.5.8.1 Reliability Verification </b> <a name="4.2.5.8.1" />
This section defines the verification for the gym map software system attributes reliability:
<p class="tab">
<b><i>4.2.5.8.1.1</b></i> Verify that the maps delivered to the user on MyJym delivers accurate data based on the information in the **System Database.** (Technique: Inspection) [3.2.7.1.1] <br>
<b><i>4.2.5.8.1.2</b></i> Verify that the MyJym map is retained in memory while the myJym application is focused on a separate page. (Technique: Test) [3.2.7.1.2] <br>

<br>
	
### <b>4.2.5.8.2 Security Verification </b> <a name="4.2.2" />
This section defines the verification for the gym map software systems security:
<p class="tab">
<b><i>4.2.5.8.2.1</b></i> Verify that the map only be editable by an admin. (Technique: Inspection) [3.2.7.2.1] <br><br> <!-- End team 2 -->

<br>

## <b>4.3 MyJym Videos Verification</b> <a name="4.3-myjym-videos-verification" /> <!-- team 3's work -->

Verify the MyJym Videos requirements

<br>

### 4.3.1 External Interfaces Specification Verification <a name="4.3.1-external-interfaces-specifications-verification" />
Verify that the section defines the inputs and outputs of the MyJym application.<br>

<br>

#### 4.3.1.1 Database Verification <a name="4.3.1.1-database-verification" />
Verify that this shows the what columns will be included to create the database. The specific column requirements are listed in section 3.5<br>
***4.3.1.1.1*** Verify that the database shall store workout title<br>
***4.3.1.1.2*** Verify that the database shall store workout video links<br>
***4.3.1.1.3*** Verify that the database shall store workout description<br>
***4.3.1.1.4*** Verify that the database shall store the image links

<br>

#### 4.3.1.2 Video Streaming Verification <a name="4.3.1.2-video-streaming-verification" />
Verify that the API for a video streaming website will be used to share videos on workout techniques and forms, and how to use gym exercise equipment. This will be used according to the product owner and stakeholder’s decisions.

***4.3.1.2.1*** Verify that Gymgoers shall have the ability to access workout videos

<br>
	
### 4.3.2 Functions Verification <a name="4.3.2-functions-verification" />
Verify that this section is responsible for explaining myJym’s ability to perform to the User’s standard. These functions are split up into sections that explain the procedure of the MyJym application in how to perform or complete tasks.

<br>

#### 4.3.2.1 My Video Verification <a name="4.3.2.1-my-video-verifiaction" />

***4.3.2.1.1*** Verify that the My Video page shall display a workout title.<br>
***4.3.2.1.2*** Verify that the My Video page shall display an equipment name.<br>
***4.3.2.1.3*** Verify that the My Video page shall display a workout video.<br>
***4.3.2.1.4*** Verify that the My Video page shall provide a save video button.<br>

<br>

### 4.3.3 Usability Requirement Verification <a name="4.3.3-usability-requirement-verification" />
Verify that this section lists the quality and use requirements for the MyJym application. Including measurable effectiveness and satisfaction criteria for the My Video feature. <br>
***4.3.3.1*** Verify that user shall be able to save a selected video<br>
***4.3.3.2*** Verify that user shall be able to view the workout video<br>
***4.3.3.3*** Verify that user shall be able to view saved videos<br>

<br>
	
### 4.3.4 Performance Requirements Verification <a name="4.3.4-performance-requirements-verification" />
Verify that for the MyJym application to meet performance standards, there are specific requirements that are needed to be met, specified below.<br>
***4.3.4.1*** Verify that user shall be able to save a selected video<br>
***4.3.4.2*** Verify that the user shall only be able to save one video link per exercise.<br>
***4.3.4.3*** Verify that the My Video page shall support a configurable amount of workouts<br>
***4.3.4.4*** Verify that the My Video page shall support a configurable amount of workouts videos<br>

<br>

### 4.3.5 Logical Database Requirements Verification <a name="4.3.5-logical-database-requirements-verification" />

Verify that the MyJym database shall store all the tables that are necessary for storing information required by the application.<br>

***4.3.5.1*** Verify that the workout table shall contain an exercise title column<br>
***4.3.5.2*** Verify that the workout table shall contain a description column<br>
***4.3.5.3*** Verify that the workout table shall contain a video link column<br>
***4.3.5.4*** Verify that the workout table shall contain a workout id column that acts as a primary key<br>

<br>

### 4.3.6 Design Constraint Verification <a name="4.3.6-design-constraints-verification" />
Verify that this section specifies the constraints with the myJym application that would arise from project limitations, external standards, and specific requirements.<br>
***4.3.6.1*** Verify that the user shall only be able to save workout the video<br>

<br>

### 4.3.7 Software System Attributes Verification <a name="4.3.7-software-system-attributes-verification" />

<br>

#### 4.3.7.1 Reliability Verification <a name="4.3.7.1-reliability-verification" />
Verify that factors required to establish reliability of the myJym application at the time of delivery.<br>
	
***4.3.7.1.1*** Verify that the system shall exit immediately when a user finds an error. <br>
***4.3.7.1.2*** Verify that the app shall check that locally stored user information matches what is stored in a database. <br>

<br>

#### 4.3.7.2 Security Verification <a name="4.3.7.2-security-verification" />
Verify that the factors required to guarantee a defined level of availability for the myJym application in regards to the workout videos. <br>	
***4.3.7.2.1*** Verify that the user shall only be able to add approved video links to an exercise. <br>

<br>

#### 4.3.7.3 Maintainability Verification <a name="4.3.7.3-maintainability-verification" />
Verify that the factors required to define a level of maintainability for the myJym application. <br>	
***4.3.7.3.1*** Verify that App administrators shall be able to remove inappropriate content. <br>

<br>	
	
## <b>4.4 Login & Homepage Verification</b>
<a name="4.4-login-&-homepage-verification" />
Verify the Login & Homepage requirements

<br>

#### 4.4.1 External Interfaces Verification <a name="4.4.1-external-interfaces-verification" />
Verification of the interfaces that the application will output to the user. <br>
***4.4.1.1*** Verify that the login page shall provide the ability to login to an account using login credentials. (Technique: Test)[3.4.1.1]<br>
What: Attempt to login to an account using both valid and invalid credentials and verify that the happy path is achieved.<br> 
***4.4.1.2*** Verify that the system shall send an automated password recovery email to the user on request. (Technique: Test)[3.4.1.2]<br>
What: Attempt to recover a password and confirm that the recovery email is sent. <br>

<br>

#### 4.4.2 Functions Verification <a name="4.4.2-functions-verification" />
Verification of the different functionalities within the application.<br>
***4.4.2.1*** Verify that the home page shall provide access to My Trainer. (Technique: Inspection)[3.4.2.1]<br>
What: The application shall take the user to the My Trainer page after the My Trainer button has been selected while on the home page.<br>
***4.4.2.2*** Verify that the home page shall provide access to My Workouts. (Technique: Test)[3.4.2.2]<br>
What: The application shall take the user to the My Workouts page after the My Workouts button has been pressed while on the home page.<br>
***4.4.2.3*** Verify that the home page shall provide access to My Videos. (Technique: Test)[3.4.2.3]<br>
What: The application shall take the user to the My Videos page after the My Videos button has been pressed while on the home page.<br>
***4.4.2.4*** Verify that the home page shall provide access to My Gym Map. (Technique: Test)[3.4.2.4]<br>
What: The application shall take the user to the My Gym Map page after the My Gym Map button has been while on the home page.<br>
***4.4.2.5*** Verify that the login page shall provide the user with the ability to recover a lost password. (Technique: Test)[3.4.2.5]<br>
What: The application shall provide the user with a temporary password when requested. The password will go through email and shall only become the current active password when it is used on the app after the user views it in their email. The user will then be required to set a new password immediately after logging in.<br>
***4.4.2.6*** Verify that the login page shall provide the user with the ability to create an account. (Technique: Test)[3.4.2.6]<br>
What: The application shall allow the user to create an account with their individual credentials and access the apps features.<br>
***4.4.2.7*** Verify that the login page shall display an error message when invalid credentials are submitted. (Technique: Test)[3.4.2.7]<br>
What: When a user attempts to log in with invalid credentials, the login page shall display an error message that the credentials were invalid and re-prompt for valid credentials.<br>
***4.4.2.8*** Verify that the system shall check the login credentials against the database. (Technique: Test)[3.4.2.8]<br>
What: The user shall only be able to login and view the home page after they provide valid login credentials.<br>

<br>

#### 4.4.3 Usability Requirements Verification <a name="4.4.3-usability-requirements-verification" />
Verification of the requirements related to usability.<br>
***4.4.3.1*** Verify that the signup page shall inform the user of password requirements. (Technique: Test)[3.4.3.1]<br>
What: When creating an account verify that the message for password requirements appears.<br>
***4.4.3.2*** Verify that the login page shall allow the user to enter login credentials (Technique: Test)[3.4.3.2]<br>
What: Attempt to enter login credentials on the login page.<br>

<br>

#### 4.4.4 Performance Requirements Verification <a name="4.4.4-performance-requirements-verification" />
Verification of the system's ability to process user requests.<br>
***4.4.4.1*** Verify that the system shall have the ability to process login credentials. (Technique: Test)[3.4.4.1]<br>
What: The system shall store the login credentials by allowing the user to re-login multiple times.<br>

<br>

#### 4.4.5 Logical Database Requirements Verification <a name="4.4.5-logical-database-requirements-verification" />
Verification of the operation of the database.<br>
***4.4.5.1*** Verify that the User Data database table shall have a Google authentication key from the Google third party login. (Technique: Inspection)[3.4.5.1]<br>
What: Inspect the User Data table to ensure that it can collect and store google authentication keys.<br>
***4.4.5.2*** Verify that the User Data database table shall store usernames (Technique: Inspection)[3.4.5.2]<br>
What: Inspect the User Data table to ensure that it can collect and store usernames.<br>
***4.4.5.3*** Verify that the User Data database table shall store the passwords (Technique: Inspection)[3.4.5.3]<br>
What: Inspect the User Data table to ensure that it can collect and store passwords.<br>
***4.4.5.4*** Verify that the database shall be accessed by the login page when user credentials are submitted through the login page. (Technique: Test)[3.4.5.4]<br>
What: Have the tester attempt to login with a valid and invalid credentials. Check if the system allows valid credentials to login and doesn't allow invalid credentials to login.<br>
***4.4.5.5*** Verify that the database shall keep the login credentials of users confidential. (Technique: Test)[3.4.5.5]<br>
What: Have a "hacker" try to access personal information in the database. Run this test until the database is secure from all attacks.<br>

<br>

#### 4.4.6 Design Constraints Verification <a name="4.4.6-design-constraints-verification" />
Verification of the metrics set to limit the application.<br>
***4.4.6.1*** Verify that the myJym app shall be completed in its entirety by the end of Jared's Senior Project class. (Technique: Demo)[3.4.6.1]<br>
What: Show that the myJym app is completed within the given timeframe.<br>
***4.4.6.2*** Verify that the budget for the myJym app shall be $0.00. (Technique: Demo)[3.4.6.2]<br>
What: Show that there has been no money spent on the development of the application.<br>

<br>

#### 4.4.7 Software System Attributes Verification <a name="4.4.7-software-system-attributes-verification" />
Verification of the software system attribute requirements

<br>

##### 4.4.7.1 Reliability Verification <a name="4.4.7.1-reliability-verification" />
Verification of the dependability of the application.<br>
***4.4.7.1.1*** Verify that the app shall require the compliance of personal trainers. (Technique: Demo)[3.4.7.1.1]<br>
What: Demonstrate the compliance of personal trainers in the use of the application.<br>
***4.4.7.1.2*** Verify that the app shall require the administrator. (Technique: Demo)[3.4.7.1.2]<br>
What: Demonstrate the administrator requirements in the use of the application.<br>

<br>

##### 4.4.7.2 Availability Verification <a name="4.4.7.2-availability-verification" />
Verification of the systems uptime for users.<br>
***4.4.7.2.1*** Verify that the myJym app shall be available on demand of the user. (Technique: Demo)[3.4.7.2.1]<br>
What: Access the myJym application at various times to ensure that it is available whenever needed.<br>

<br>

##### 4.4.7.3 Security Verification <a name="4.4.7.3-security-verification" />
Verification of the applications ability to protect user assets.<br>
***4.4.7.3.1*** Verify that the system shall encrypt user accounts. (Technique: Inspection)[3.4.7.3.1]<br>
What: Inspect the code to ensure that the user account information is properly encrypted.<br>
***4.4.7.3.2*** Verify that the system shall use a protocol to secure online communications. (Technique: Inspection)[3.4.7.3.2]<br>
What: Inspect code to ensure that a protocol is properly used to secure online communication.<br>

<br>

##### 4.4.7.4 Portability Verification <a name="4.4.7.4-portability-verification" />
Verification of the applications ability to work on different operating systems.<br>
***4.4.7.4.1*** Verify that the application shall be built with a programming language that can be ported to both iOS and Android. (Technique: Inspection)[3.4.7.4.1]<br>
What: Inspect the code to ensure that it can be ported to iOS and Android.<br>

<br>

## <b>4.5 My Workout Verification</b> <a name="4.5-my-workout-verification" />

<br>

<!-- team 3 and 4's stuff--> 
### <b>4.5.1 External Interface Verification</b> <a name="4.5.1-external-interface-verification" />
This section defines the verification for external interfaces for the myJym application.

<br>

#### <b>4.5.1.1 Database Verification</b> <a name="4.5.1.1-database-verification" />
This section defines the verification for the database for the my workout function.
<p class="tab">
<b><i>4.5.1.1.1</b></i> Verify that the database shall store workout <b>title</b>. [3.5.1.1.1] (Technique: inspection)<br>
<b><i>4.5.1.1.2</b></i> Verify that the database shall store workout video links. [3.5.1.1.2] (Technique: inspection)<br>
<b><i>4.5.1.1.3</b></i> Verify that the database shall store workout description. [3.5.1.1.3] (Technique: inspection)<br>
<b><i>4.5.1.1.4</b></i> Verify that the database shall store workout <b>sets</b>. [3.5.1.1.4] (Technique: inspection)<br>
<b><i>4.5.1.1.5</b></i> Verify that the database shall store workout <b>reps</b>. [3.5.1.1.5] (Technique: inspection)<br>
<b><i>4.5.1.1.6</b></i> Verify that the database shall store workout <b>tags</b>. [3.5.1.1.6] (Technique: inspection)<br>
</p>

<br>

#### <b>4.5.1.2 Video Provider Verification</b> <a name="4.5.1.2-video provider-verification" />
This section defines the verification for the video provider integration for the my workout function.
<p class="tab">
<b><i>4.5.1.2.1</b></i> Verify that the <b>gymgoers</b> shall have the ability to access workout videos. [3.5.1.2.1] (Technique: demonstration)<br>
</p>

<br>
    
### <b>4.5.2 Functions Verification</b> <a name="4.5.2-functions-verification" />
This section defines the verification for functionality for the my workout feature.

<br> 

#### <b>4.5.2.1 Create Workout Verification</b> <a name="4.5.2.1-create-workout-verification" />
This section defines the verification for the create workout function for the my workout feature.
<p class="tab">
<b><i>4.5.2.1.1</b></i> Verify that the workout creation shall allow the <b>user</b> to specify a workout name. [3.5.2.1.1] (Technique: demonstration)<br>
<b><i>4.5.2.1.2</b></i> Verify that the workout creation shall allow the user to specify a muscle group to workout. [3.5.2.1.2] (Technique: demonstration)<br>
<b><i>4.5.2.1.3</b></i> Verify that the workout creation shall allow the user to specify an amount of <b>reps</b>. [3.5.2.1.3] (Technique: demonstration)<br>
<b><i>4.5.2.1.4</b></i> Verify that the workout creation shall allow the user to specify an amount of <b>sets</b>. [3.5.2.1.4] (Technique: demonstration)<br>
<b><i>4.5.2.1.5</b></i> Verify that the workout creation shall allow the user to embed a video link. [3.5.2.1.5] (Technique: demonstration)<br>
</p>

<br>

#### <b>4.5.2.2 Find Workout Verification</b> <a name="4.5.2.2-find-workout-verification" />
This section defines the verification for the find workout function for the my workout feature.
<p class="tab">
<b><i>4.5.2.2.1</b></i> Verify that the find workout page shall have the ability to search by predetermined <b>tag</b>s. [3.5.2.2.1] (Technique: demonstration)<br>
<b><i>4.5.2.2.2</b></i> Verify that one of the tags that can be used to search by shall be <b>author</b>. [3.5.2.2.2] (Technique: demonstration)<br>
<b><i>4.5.2.2.3</b></i> Verify that one of the tags that can be used to search by shall be <b>name of workout</b>. [3.5.2.2.3] (Technique: demonstration)<br>
<b><i>4.5.2.2.4</b></i> Verify that one of the tags that can be used to search by shall be <b>length</b>. [3.5.2.2.4] (Technique: demonstration)<br>
<b><i>4.5.2.2.5</b></i> Verify that one of the tags that can be used to search by shall be <b>workout type</b>. [3.5.2.2.5] (Technique: demonstration)<br>
<b><i>4.5.2.2.6</b></i> Verify that one of the tags that can be used to search by shall be <b>difficulty</b>. [3.5.2.2.6] (Technique: demonstration)<br>
<b><i>4.5.2.2.7</b></i> Verify that one of the tags that can be used to search by shall be <b>equipment type</b>. [3.5.2.2.7] (Technique: demonstration)<br>
<b><i>4.5.2.2.8</b></i> Verify that one of the tags that can be used to search by shall be <b>muscle groups</b>. [3.5.2.2.8] (Technique: demonstration)<br>
<b><i>4.5.2.2.9</b></i> Verify that the user shall have the ability to save a workout they find to their saved workouts list. [3.5.2.2.9] (Technique: demonstration)<br>
</p>

<br>

#### <b>4.5.2.3 Saved Workout Verification</b> <a name="4.5.2.3-saved-workout-verification" />
This section defines the verification for the saved workout function for the my workout feature.
<p class="tab">
<b><i>4.5.2.3.1</b></i> Verify that the user shall have the option to edit the workout. [3.5.2.3.1] (Technique: demonstration)<br>
<b><i>4.5.2.3.2</b></i> Verify that selecting edit workout shall redirect the user back to the create workout page with all the workout information filled in. [3.5.2.3.2] (Technique: demonstration)<br>
<b><i>4.5.2.3.3</b></i> Verify that the user shall have the option to immediately start the workout. [3.5.2.3.3] (Technique: demonstration)<br>
<b><i>4.5.2.3.4</b></i> Verify that selecting start workout shall redirect the user to the workout in progress page. [3.5.2.3.4] (Technique: demonstration)<br>
<b><i>4.5.2.3.5</b></i> Verify that the user shall have the option to delete a previously saved workout. [3.5.2.3.5] (Technique: demonstration)<br>
</p>

<br>

#### <b>4.5.2.4 Workout in Progress Page Verification</b> <a name="4.5.2.4-workout-in-progress-page-verification" />
This section defines the verification for the workout in progress function for the my workout feature.
<p class="tab">
<b><i>4.5.2.4.1</b></i> Verify that the workout in progress page shall guide the user through their workout. [3.5.2.4.1] (Technique: demonstration)<br>
<b><i>4.5.2.4.2</b></i> Verify that the workout in progress page shall display the workout information for the selected workout. [3.5.2.4.2] (Technique: demonstration)<br>
</p>

<br>

#### <b>4.5.2.5 My Video Page Verification</b> <a name="4.5.2.5-my-video-page-verification" />
This section defines the verification for the workout in progress function for the my workout feature.
<p class="tab">
<b><i>4.5.2.5.1</b></i> Verify that the My Video page shall display a workout title. [3.3.2.1.1] (Technique: demonstration)<br>
<b><i>4.5.2.5.2</b></i> Verify that the My Video page shall display an equipment name. [3.3.2.1.2] (Technique: demonstration)<br>
<b><i>4.5.2.5.3</b></i> Verify that the My Video page shall display a workout video. [3.3.2.1.3] (Technique: demonstration)<br>
<b><i>4.5.2.5.4</b></i> Verify that the My Video page shall provide a save video button. [3.3.2.1.4] (Technique: demonstration)<br>
</p>

<br>

### <b>4.5.3 Usability Requirements Verification</b> <a name="4.5.3-usability-requirements-verification" />
This section defines the verification for the usability requirements for the my workout feature.
<p class="tab">
<b><i>4.5.3.1</b></i> Verify that the user shall be able to create a workout. [3.5.3.1] (Technique: demonstration)<br>
<b><i>4.5.3.2</b></i> Verify that the user shall be able to find a workout. [3.5.3.2] (Technique: demonstration)<br>
<b><i>4.5.3.3</b></i> Verify that the user shall be able to save a workout. [3.5.3.3] (Technique: demonstration)<br>
<b><i>4.5.3.4</b></i> Verify that the user shall be able to start a workout. [3.5.3.4] (Technique: demonstration)<br>
<b><i>4.5.3.5</b></i> Verify that the user shall be able to see workout progress. [3.5.3.5] (Technique: demonstration)<br>
</p>

<br>

### <b>4.5.4 Performance Requirements Verification</b> <a name="4.5.4-performance-requirments-verification" />
This section defines the verification for the performance requirements for the my workout feature.
<p class="tab">
<b><i>4.5.4.1</b></i> Verify that the user shall only be able to save one video link for a specific exercise. [3.5.4.1] (Technique: test)<br>
<b><i>4.5.4.2</b></i> Verify that the system shall support a configurable amount of workouts. [3.5.4.2] (Technique: test)<br>
<b><i>4.5.4.3</b></i> Verify that the system shall support a configurable amount of tags per workout. [3.5.4.3] (Technique: test)<br>
</p>

<br>

### <b>4.5.5 Logical Database Requirements Verification</b> <a name="4.5.5-logical-database-requirments-verification" />
This section defines the verification for the logical database requirements for the my workout feature.
<p class="tab">
<b><i>4.5.5.1</b></i> Verify that the workout table shall contain an exercise title column. [3.5.5.1] (Technique: inspection)<br>
<b><i>4.5.5.2</b></i> Verify that the workout table shall contain a tag column. [3.5.5.2] (Technique: inspection)<br>
<b><i>4.5.5.3</b></i> Verify that the workout table shall contain a rep column. [3.5.5.3] (Technique: inspection)<br>
<b><i>4.5.5.4</b></i> Verify that the workout table shall contain a set column. [3.5.5.4] (Technique: inspection)<br>
<b><i>4.5.5.5</b></i> Verify that the workout table shall contain a description column. [3.5.5.5] (Technique: inspection)<br>
<b><i>4.5.5.6</b></i> Verify that the workout table shall contain a video link column. [3.5.5.6] (Technique: inspection)<br>
<b><i>4.5.5.7</b></i> Verify that the workout table shall contain a workout id column that acts as a <b>primary key</b>. [3.5.5.7] (Technique: inspection)<br>
</p>

<br>

### <b>4.5.6 Design Constraints Verification</b> <a name="4.5.6-design-constraints-verification" />
This section defines the verification for the design constraints for the my workout feature. 
<p class="tab">
<b><i>4.5.6.1</b></i> Verify that the user shall only be able to add approved video links from a video provider to an exercise. [3.5.6.1] (Technique: demonstration)<br>
<b><i>4.5.6.2</b></i> Verify that the user shall only be able to input an integer into the rep field. [3.5.6.2] (Technique: demonstration)<br>
<b><i>4.5.6.3</b></i> Verify that the user shall only be able to input an integer into the set field. [3.5.6.3] (Technique: demonstration)<br>
<b><i>4.5.6.4</b></i> Verify that the user shall have to add a title to the workouts they create. [3.5.6.4] (Technique: demonstration)<br>
</p>

<br>

### <b>4.5.7 Software System Attributes Verification</b> <a name="4.5.7-software-system-attributes-verification" />
This section defines the verification for the software system attributes for the my workout feature.

<br>

#### <b>4.5.7.1 Reliability Verification</b> <a name="4.5.7.1-reliability-verification" />
This section defines the verification for the reliability of the my workout feature.
<p class="tab">
<b><i>4.5.7.1.1</b></i> Verify that the system shall exit immediately when user finds an error. [3.5.7.1.1] (Technique: demonstration)<br>
<b><i>4.5.7.1.2</b></i> Verify that the app shall check that locally stored user information matches what is stored in database. [3.5.7.1.2] (Technique: inspection)<br>
</p>

<br>

#### <b>4.5.7.2 Security Verification</b> <a name="4.5.7.2-security-verification" />
This section defines the verification for the security of the my workout feature.
<p class="tab">
<b><i>4.5.7.2.1</b></i> Verify that the user shall only be able to add approved video links from a video provider to an exercise. [3.5.7.2.1] (Technique: demonstration)<br>
</p>

<br>

#### <b>4.5.7.3 Maintainability Verification</b> <a name="4.5.7.3-maintainability-verification" />
This section defines the verification for the maintainability of the my workout feature.
<p class="tab">
<b><i>4.5.7.3.1</b></i> Verify that the app administrators shall be able to remove <b>inappropriate</b> content. [3.5.7.3.1] (Technique: demonstration)<br>
</p>

<br>

### <b>4.8.3 Supporting Information Verification</b>
Not applicable for the my workout feature.
