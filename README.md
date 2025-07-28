# chat-website

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : Snehal Anand

*INTENR ID* : CT04DH1332

*DOMAIN* : FULL STACK WEB DEVELOPMENT

*BATCH DURATION* : 4 week

*MENTOR NAME* : NEELA SANTOSH KUMAR

# React Firebase Chat App
This project utilizes React and Firebase to create a chat application.

# Getting Started
Follow these steps to set up and run the project locally:

# Prerequisites
Node.js and npm installed on your machine.
Firebase account.
Installation
Clone the repository:
git clone <repository_url>
Navigate to the project directory:
cd react-firebase-project
Install dependencies:
npm install
Development
Start the development server:
npm run dev
Open your browser and go to http://localhost:
Firebase Setup
Follow these steps to configure Firebase services for the project:

Create a Firebase project on the Firebase Console.

Enable Firebase Authentication and configure Google and Email/Password as Sign-In Providers.

Enable Firebase Cloud Firestore.

Add the following Firestore Security Rules:

rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
Add the following Firestore Indexes: chat_messagechatRoomId Ascending timestamp Ascending __name__ Ascending.

Enable Firebase Cloud Storage.

Add the following Cloud Storage Security Rules:

rules_version = '2';

service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write: if request.auth != null;
    }
  }
}
Copy the Firebase config keys and paste them into `src/configs/firebase.js` in your React project.
License
This project is licensed under the MIT License - see the LICENSE file for details.
## output 
