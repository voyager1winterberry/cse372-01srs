# MyJym Software Requirements Specification

## Table of Contents
* [1.0 Purpose](#1.0-purpose)
    * [1.1 Scope](#1.1-scope)
        * [1.1.1 Included Core Features](#1.1.1-included-core-features) 
        * [1.1.2 Possible Features](#1.1.2-possible-features)
        * [1.1.3 Excluded Features](#1.1.3-excluded-features)
        * [1.3.1 Product Perspective](#1.3.1-product-perspective)
[1.3.1.1 System Interfaces](#1.3.1.1-system-interfaces)
            * [1.3.1.2 User Interfaces](#1.3.1.2-user-interfaces)
            * [1.3.1.3 Hardware Interfaces](#1.3.1.3-hardware-interfaces)
            * [1.3.1.4 Software Interfaces](1.3.1.4-software-interfaces)
             

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

## Definitions
| Word   |  Definition |
|------- | -------     |
|Android 11: | The minimum android version that will be required for the project.|
| App: | myJym mobile application. |
|Embedded Video: | Embedded Videos: Videos in applications that play a video inside of the app without having to go to the place containing the original video.|
|Forms: | Digital way to collect relevant information from the user. |
|GUI: | GUI (Graphical User Interface) is a user interface that includes graphical elements, such as windows, icons, and buttons. The purpose is to appeal to the user using visuals.|
| Interface| A point where two systems, subjects, organizations, etc. meet and interact.|
|iOS:| Internet Operating System or iPhone Operating System. It is the operating system used on Apple products, such as iPhone and iPad.|
|IOS 14.1: | The minimum IOS version that will be required for the project. |
|macOS: | The Macintosh Operating System is an operating system designed by Apple Inc. to be installed and operated on the Apple Macintosh series of computers. It is a (GUI) based OS that has since been released in multiple different versions. |
|Mnemonic: | The device that uses patterns of letters, associations to assist users to remember a specific feature and its functionality. |
|Name: | The name of the software’s feature. Generally, the name of the feature needs to be self-explanatory and easy to understand. |
|Primary memory: | Memory utilized by the app on the individual devices. |
|Profile: | A personalized account created by the user that will be associated with them and required to utilize the app. |
|QR Scanning: | the ability of a mobile device to capture QR codes in their camera and then open the associated links. |
|Secondary memory: | removable or external memory used by the individual devices. |
|Source: | A specific reference for the research and citation purpose to avoid plagiarism. |
|Specification number: | For the purpose of organization feature within the SRS documentation.|
|Trainers: | Individuals that work in conjunction with the app to provide a means of providing feedback and encouraging users with workout goals. Trainers will use the app as a way of communicating with the users. | 
|Users: | Clients that will use the app to progress with their training and receive help and support from trainers |
|Version number: | A set of unique numbers that are assigned to a specific release of a software project. In this case, it will be myJym version 1.0.0 |
|Working camera: | camera capable of taking clear photos. |


## References
* [1] S.R.O., Eccam. “Example Software Requirements Specification (SRS) | ReqView Documentation.” ReqView, 2018, www.reqview.com/doc/iso-iec-ieee-29148-srs-example.

* [2] IIEEE, " 29148-2018 - ISO/IEC/IEEE International Standard - Systems and software engineering -- Life cycle processes -- Requirements engineering " pp. 56-87, Jul. 2018. [Online] Available: https://ieeexplore-ieee-org.byui.idm.oclc.org/document/8559686 

* [3] “Macintosh Operating System (Mac OS).” Techopedia, techopedia, 2012, www.techopedia.com/definition/2639/macintosh-operating-system-mac-os.
