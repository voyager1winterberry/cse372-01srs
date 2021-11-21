## 3.1 My Trainer
* ### 3.1.1 External Interfaces
    * #### 3.1.1.1 Google Authentication
        * Google Authentication API shall be used by gymgoers and trainers to login to their accounts.
        * All users shall be able to login to their account using a google account.
        * All users shall be able to create an account using a google google account.

* ### 3.1.2 Functions
    * #### 3.1.2.1 myJym
        The myJym application will allow users to view the My Trainer page and receive system notifications.

        * The myJym application shall have a My Trainer page.
        * The myJym application shall send users Notifications. 
    * #### 3.1.2.1 Notifications
        Notifications will allow users to receive notifications/alerts.

        * A notification will be created when a user sets a time for their workout.
        * A notification will be created when a user receives a message.
    * #### 3.1.2.2 My Trainer
        My trainer will allow users to search for trainers, see trainer profiles, and message trainers.

        * My Trainer page shall display a Trainer Profile.
        * My Trainer page shall have a Search Trainer bar.

    * #### 3.1.2.3 View Trainer Profile
        The trainer profile will provide a viewable page for users with the trainer's photo, short bio, links to youtube channels, a follow button, a link to workouts created by the trainer, and a button to message the trainer.

        * Trainer profile shall be viewable by gymGoers.
        * Trainer profile shall display a picture of the trainer.
        * Trainer profile shall display a short biography of the trainer.
        * Trainer profile shall display a clickable link to the trainer’s youtube channel.
        * “Follow Trainer” shall be an option on the Trainer profile.
        * “View Workouts” shall be an option on the Trainer profile.
        * “Message Trainer” shall be an option on the Trainer profile.

    * #### 3.1.2.4 Edit Profile
        The edit profile function will allow any user to make changes to their profile.
        * The Edit Profile page shall allow any user to edit their own picture.
        * The Edit Profile page shall allow any user to be able to edit their password.
        * The Edit Profile page shall allow any user to include a biography text-field.
        * The Edit Profile page shall allow any user to edit their account configuration.
        * The Edit Profile page shall allow any user to edit their personal youtube link.
        
    * #### 3.1.2.5 Search Trainer
        Search trainer will allow users to view and input into a search bar to find trainers.
        * A search bar shall be viewable by the gymgoer.
        * A gymgoer shall be able to input into the search bar.
        * Search trainer shall enable the ability to find trainers matching input into search bar.

    * #### 3.1.2.6 Message Trainer
        Message trainer will allow a user to communicate with a trainer.
        * Message Trainer shall give a user the ability to send messages to a trainer. 
        * Message Trainer shall create a chat between a user and a trainer. 
        * Message Trainer shall list messages in chronological order. 
        * Message Trainer shall be able to send the message. 
        * Messages Trainer shall be able to handle messages containing text.
        * Message Trainer shall be able to handle messages containing images.
        * Message Trainer shall be able to handle messages containing links.
        * Message Trainer shall be able to handle messages containing video.

    * #### 3.1.2.7 Message Users
        Message Users shall allow the trainer to communicate with users. 
        * Message users shall give trainers the ability to send messages to users. 
        * Message users shall create a chat between trainer and users. 
        * Message users shall give trainers the ability to send messages to any number of chosen users. 
        * Message users shall list messages in chronological order. 
        * Message users shall be able to send the message. 

* ### 3.1.3 Usability Requirements
    * Ease of learning. The system shall be easy to learn for both novices and users with experience from similar systems. Users familiar with similar systems shall be able to create a new account and access the account within an average of 5 minutes.

    * Task efficiency. The system shall be efficient for the frequent user. Frequent users shall be given an option to be able to access their account without having to sign in each session. Tasks shall be able to be completed by the frequent user within an average of 25 seconds. 

    * Ease of remembering. The system shall be easy to remember for the casual user. Users experienced with this system shall be able to login to their account within an average of 1 minute. 

    * Understandability: The user shall understand what the system does. The system shall keep every option available on the user interface to similar sizes so that no option is larger than the others. A new user shall be able to navigate to any desired option within an average of 30 seconds. A total of 99% of users shall be able to perform any given task. 

    * Subjective satisfaction. The user shall feel satisfied with the system. The system shall receive an average rating of 7 out of 10 by test groups, with 10 being the highest and 1 the lowest. 

    * Task failure. Task failure by the system shall be kept to an absolute minimum. Task failure shall be limited to at most, .2 per user.  

    * Requirements to undo. A safe environment shall be incorporated into the system where users are able to try things and undo them. The ability to undo should be incorporated into any part of the system that stores information, or task.

    * Accessibility. The system will be created with elements that ensure that it is accessible by the widest range of people as possible. These elements include but are not limited to: color, text, complexity, and exclusivity. 

* ### 3.1.4 Performance Requirements
    * The mytrainer page shall display views after a predetermined time.
    * The trainer shall receive messages after a predetermined time.
    * The trainer shall compose messages after a predetermined time.
    * Notifications for the trainer shall be received after a predetermined time.
    * 90% of trainer profiles shall be loaded up in less than 5 s.
    * 95% of trainer search results shall load up in 1 s.
    * Trainer workout videos shall be processed in less than 5 s using hyperlinks.
    * 90% of setting trainer availability info shall be processed in 1 s.

* ### 3.1.5 Logical Database Requirements
    * #### 3.1.5.1 Types of information used by various functions
        * MyTrainer shall store a trainers first name
        * MyTrainer shall store a trainer’s last name.
        * MyTrainer shall store a trainer’s email.
        * The system shall create a trainer_ID for each trainer.
        * The system shall create a personal key for each trainer.

    * #### 3.1.5.2 Frequency of use
        * Email data types shall be used for a single account.
        * Primary keys shall be used on a single account.

    * #### 3.1.5.3 Accessing Capabilities
	    * Trainers shall have access to UserData first_name.
	    * Trainers shall have access to UserData last_name.
	    * Trainers shall have access to UserData goals.
	    * Trainers shall have access to UserData W/O_plan.
	    * Trainers shall have access to UserData gym.

    * #### 3.1.5.4 Data entities and their relationships
        * MyTrainer shall have a data type for first_name.
        * MyTrainer shall have a data type for last_name
        * MyTrainer shall have a data type for email.
        * MyTrainer shall have a data type for trainer_ID.
        * MyTrainer shall have a personal key for each trainer.

    * #### 3.1.5.5 Integrity Constraints
	    * Data entries shall be possible entries.
	    * Data entries shall be verified by the system.
	    * Data entries shall have valid references.
	    * Trainers shall have unique primary keys.
	    * The system shall have entity integrity.

    * #### 3.1.5.6 Security
	    * Trainer accounts shall utilize google sign-in to access their account.
	    * Trainers shall only have one account.
	    * Admin accounts shall have access to all accounts

    * #### 3.1.5.7 Data retention requirements
		* Data shall be retained for 2(two) years.
		* Data shall be retained in a database.
		* Trainer accounts shall be accessible for 2(two) years after inactivity.

* ### 3.1.6 Design Constraints
    ![Design Constraints Image](Images/DesignConstraintsImage.png)

* ### 3.1.7 Software System Attributes
    * #### 3.1.7.1 Reliability 
        * Applications shall not have errors within the codes to cause applications to close or crash. 
        * There will be functions within the software that performs verifications to notice errors before the application break or force closes.  
        * The system shall verify the information that matches from the server and the application. 

    * #### 3.1.7.2 Security
        * Password Protection and Encryption 
        * User account creation 
            * User information shall be available to users and those have access. 
            * User shall be required to provide email, and password for the purpose of account creation. 

        * #### 3.1.7.3 Data Privacy
            * User’s data shall be hidden from all other users and parties. 
            * Login Information 
            * Creating an account shall be safe and secure. 
            * All users shall be allowed to login securely. 
            * Once a user logs out from the account, all user information shall be removed from the login screen. 
        * #### 3.1.7.4 Maintainability
            * Users shall be allowed to report to the administration team if they forget their password, and need to have a reset password email sent to their personal email that has been registered on their myJym account. 
            * An automatic email shall be sent to the user's email address to allow the user to reset their password. 
        * #### 3.1.7.5 Portability
            * System Database shall store user information. 
            * myJym application shall run on both Android and iOS mobile interface.

* ### 3.1.8 Supporting Information
    ![Design Constraints Image](Images/SupportingInfoImage.png)

    *  Description of the problems to be solved by the software:
    A problem that this software will solve is to give users the ability to connect with trainers.Trainers will be able to provide information to users about workouts and feedback on workout plans. Trainers will be able to access user data to be able to help them choose workout plans and give them the motivation to meet their goals.