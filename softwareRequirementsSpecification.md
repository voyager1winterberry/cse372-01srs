# myJym Software Requirements Specification

## Table of Contents
* [1.0 Purpose](#1.0-purpose)
* [1.1 Scope](#1.1-scope)
    * [1.1.1 Included Core Features](#1.1.1-included-core-features) 
    * [1.1.2 Possible Features](#1.1.2-possible-features)
    * [1.1.3 Excluded Features](#1.1.3-excluded-features)
* [1.3.1 Product Perspective](#1.3.1-product-perspective)
    * [1.3.1.1 System Interfaces](#1.3.1.1-system-interfaces)
    * [1.3.1.2 User Interfaces](#1.3.1.2-user-interfaces)
    * [1.3.1.3 Hardware Interfaces](#1.3.1.3-hardware-interfaces)
    * [1.3.1.4 Software Interfaces](#1.3.1.4-software-interfaces)
             
<br>

## 1.0 Purpose
The myJym app is to help people at all levels of experience feel confident using gym equipment.  It also focuses on connects users to personal trainors.  Additional features include work out regiments, gym maps, and abbility to track fitness goals.

## 1.1 Scope
### 1.1.1 Included Core Features
- Suggest workouts to user based on what user wants to do
- Let user create or augment their own workouts
- Track user workouts and progress
- Store user profile information
- Connect users to trainors to get their advice on workouts
- Gym will have QR codes to scan that will bring up information about how to use specific equipment

### 1.1.2 Possible Features
- Map that shows location of specific equipment
- Have social media aspect for trainors to get recognized

### 1.1.3 Excluded Features
- Not a nutrition app. It is not supposet to recommend meal plans, diets, count calories or anything else along those lines.
- Not a video platform. Not supposet to have recorded workout videos to follow.


### 1.3.1 Product Perspective

#### 1.3.1.1 System Interfaces
- The application will be running on the most recent **iOS** and **macOS**. It will also be connected with a database to store information.

#### 1.3.1.2 User Interfaces
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

#### 1.3.1.3 Hardware Interfaces
* Since the application will be run over the internet and cell service data, most of the hardware requirements will ensure the ios and android devices are able to connect to the internet. Since the **app** will be a fitness app, the hardware will require **users** to have the feature of location tracking for personal coach and exercise equipment tutorial videos. Preferably, iPhone 6 and later gen, for the purpose of app store update reasons. 

#### 1.3.1.4 Software Interfaces
* Specify the use of other required software products.
    - Operating System: iOS and Android devices. 
    - Linkage: Users are allowed to sign up myJam with their existing social media or email accounts. (Facebook, Gmail, etc) 

#### 1.3.1.5 Communications Interfaces
* Communication interfaces shall include communication between the users and **trainers**, including a means of messaging within the app. Communication shall also include a means of communicating with myJym for issues or to receive help.

#### 1.3.1.6 Memory
* **Primary memory** shall be used to store the user’s data such as **profile** and user agreements. **Secondary memory** will not be utilized.

#### 1.3.1.7 Operations
* Operations by the user shall include:
    - Creating a profile upon first use of the app
    - Connect with trainers that can offer insight and assistance into the workout  schedule of the user
    - Learn how to use gym equipment by scanning a QR code on the machine and watching the associated video.
    - Operations by the Trainers shall include:
    - Creating a profile upon first use of the app
    - Receiving approval from myJym to contact and train users through an approval process
    -Connect with users through messaging and other means through the app to assist with training goals

#### 1.3.1.8 Site Adaption Requirements
* **Android**
* **IOS**
* Web application

#### 1.3.1.9 Interfaces with Services
* (No knowledge of whether we plan to use cloud-based services or Saas)

### 1.3.2 Product Functions
#### 1.3.2.1 User Profiles:
 - A returned missionary attending BYU-Idaho, in their early twenties, has a busy schedule with work and a heavy course load.
 - A student in their junior year, also attending BYU-Idaho, in their early twenties, they enjoy playing football with their friends and family.
 - A new freshman, halfway through the semester wanting to lose weight, but unsure of where to start.
 - A couple that likes to spend time together by playing sports and working out.

#### 1.3.2.2 User Scenarios:
- Only being able to attend the gym in the early morning, with no previous time to set a workout routine or research workout machines.
- Brand new to exercising, there is a fear of feeling inadequate and confused in front of others, and a desire to be helped in a discreet way.
- Getting burnt out with their current workout routine, and desiring new machines and techniques that can help them develop new routines.
- Having exercised mostly through cardio before, a student wants to begin using machines to grow individual muscles and know what they can do to have a more efficient workout.

### 1.3.4 Limitations
#### 1.3.4.1 Regulatory Requirements and Policies
HIPPA / GDPR - Restrictions on collecting personal information. Important to be transparent. Ensure that personal information does not have to be given to operate, only given voluntarily. Personal trainers need to be qualified and licensed.
#### 1.3.4.2 Hardware Limitations (e.g. signal timing requirements)
Hardware requirements are a camera, internet access, and a mobile device. Development limitations are the fact that it is a school project, so computers and coding software will have to be provided by the developers and the school.
#### 1.3.4.3 Interfaces to Other Applications
Some of the limitations of interfacing with other applications would be teh licensing of a third-party video service and a third-party messaging service. The video service might also run ads, this hurt the user experience. The messaging service could require the user to create an account, this could deter some users from using the app.
#### 1.3.4.4 Parallel Operation
The project sponsor would like to track calories of the user. This could require the use of a smart watch or fitness tracker which not everyone will have. Bluetooth would be used to connect the devices; Bluetooth could cause problems for less tech savvy users and Bluetooth connections can have issues at times.
#### 1.3.4.5 Audit Functions
Bug report tool/ user feedback. We may not get relevant data from the user feedback, and we will need a team of people to handle user feedback.
#### 1.3.4.5 Control Functions
The skills and knowledge of the student developers will limit how well the control functions of the app are written and used.
#### 1.3.4.6 Higher-Order Language Requirements
Since this is a mobile application two different apps need to be written, one for android and one for apple. This will require the use of Kotlin and Swift so the developers will need to learn or know at least one of these languages. This could also cause problems in ensuring that the apps are the same. A way to get around this would be to use a web app.
#### 1.3.4.7 Signal Handshake Protocols
Finding people who have knowledge of single handshake protocols will be a challenge.
#### 1.3.4.8 Quality Requirements (e.g. reliability)
The app needs to be easily accessible, needs to be efficient process and handling data. Lack of experience could result in reduced quality.
#### 1.3.4.9 Criticality of the Application
Most of the app is dependent upon personal trainers and YouTube. If either of these fail it could cause major problems in the app.
#### 1.3.4.10 Safety and Security Considerations
We need to protect user data, especially if the app stores payment information. We will have to find someone who can work on security.
#### 1.3.4.11 Physical/Mental Considerations
We will need to consider the physical limitations of the person using the app. We will need to include a liability waiver in the terms and conditions.
#### 1.3.4.12 Limitations That Are Sourced From Other Systems, Including Real-time Requirements From the Controlled System Through Interface
The limitations of YouTube and whichever messaging service we decide to use will apply to the app.

## 1.4 Definitions:

| Word   |  Definition |
|------- | -------     |
|Android 11:| The minimum android version that will be required for the project.|
|Audit Functions:| Functions of the application that allow for user feedback and error handling.|
|App:| myJym mobile application.|
|Control Functions:| The interface with which the user will interact with and control the app.|
|Criticality of the Application:| Parts of the application have dependencies that can fail because of them. The most critical parts of the application.|
|Embedded Video: | Embedded Videos: Videos in applications that play a video inside of the app without having to go to the place containing the original video.|
|Forms:| Digital way to collect relevant information from the user.|
|Hardware Limitations: | Physical technological factors that might limit or slow the progress of the app and its construction.|
|Higher-Order Language Requirements:| Knowledge of high-level programming languages such as Kotlin and Swift.|
|GUI:| GUI (Graphical User Interface) is a user interface that includes graphical elements, such as windows, icons, and buttons. The purpose is to appeal to the user using visuals.|
|Interface| A point where two systems, subjects, organizations, etc. meet and interact.|
|Interfaces to other applications:| The ability to interact with third party applications.|
|iOS:| Internet Operating System or iPhone Operating System. It is the operating system used on Apple products, such as iPhone and iPad.|
|IOS 14.1:| The minimum IOS version that will be required for the project. |
|macOS:| The Macintosh Operating System is an operating system designed by Apple Inc. to be installed and operated on the Apple Macintosh series of computers. It is a (GUI) based OS that has since been released in multiple different versions. |
|Mnemonic:| The device that uses patterns of letters, associations to assist users to remember a specific feature and its functionality.|
|Name:| The name of the software’s feature. Generally, the name of the feature needs to be self-explanatory and easy to understand.|
|Parallel Operation:| The ability of an application to run in parallel to other applications without getting in their way or being interrupted by them.|
|Physical/mental considerations:| Considerations that pertain to the physical and mental health of the application.|
|Primary memory:| Memory utilized by the app on the individual devices.|
|Profile:| A personalized account created by the user that will be associated with them and required to utilize the app.|
|QR Scanning:| The ability of a mobile device to capture QR codes in their camera and then open the associated links.|
|Quality Requirements:| The reliability of the application, as well as the other quality metrics that represent how well it fulfills its tasks.|
|Regulatory Requirements and Policies:| Application requirements that need to comply with legal regulations and policies.|
|Safety and Security Considerations:| Keeping the user’s physical and personal safety in mind, including sensitive or confidential information.|
|Secondary memory:| removable or external memory used by the individual devices.|
|Signal Handshake Protocols:| How the app interacts securely with other applications and the internet.|
|Source:| A specific reference for the research and citation purpose to avoid plagiarism.|
|Specification number:| For the purpose of organization feature within the SRS documentation.|
|Trainers:| Individuals that work in conjunction with the app to provide a means of providing feedback and encouraging users with workout goals. Trainers will use the app as a way of communicating with the users.| 
|Users:| Clients that will use the app to progress with their training and receive help and support from trainers|
|Version number:| A set of unique numbers that are assigned to a specific release of a software project. In this case, it will be myJym version 1.0.0 |
|Working camera:| camera capable of taking clear photos.|


## References
* [1] S.R.O., Eccam. “Example Software Requirements Specification (SRS) | ReqView Documentation.” ReqView, 2018, www.reqview.com/doc/iso-iec-ieee-29148-srs-example.

* [2] IIEEE, " 29148-2018 - ISO/IEC/IEEE International Standard - Systems and software engineering -- Life cycle processes -- Requirements engineering " pp. 56-87, Jul. 2018. [Online] Available: https://ieeexplore-ieee-org.byui.idm.oclc.org/document/8559686 

* [3] “Macintosh Operating System (Mac OS).” Techopedia, techopedia, 2012, www.techopedia.com/definition/2639/macintosh-operating-system-mac-os.
