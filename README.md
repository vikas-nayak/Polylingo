Multi Lingual Chat using React Js, Firebase-v9 and Material UI with Google & Github Login
=====================================

Live [demo](https://euphonious-rabanadas-f7e242.netlify.app/)

![Chat](https://github.com/vikas-nayak/Multilingual-Chat-App-Frontend/assets/102694776/e99b542d-458a-4b8e-9c56-14788b35e317)
![Select Language](https://github.com/vikas-nayak/Multilingual-Chat-App-Frontend/assets/102694776/a552f817-9841-49c5-bb06-8cb79d48fd6a)
![Login](https://github.com/vikas-nayak/Multilingual-Chat-App-Frontend/assets/102694776/e571b0ed-e624-477e-9206-51ddde15274c)

Quick Start:
------------

- ``` git clone ```
- ``` cd react-firebase-chatApp ```
- Add your firebase configuration to firebase.js file on /src
- ``` npm install ```
- ``` npm start ```


Additional Configuration:
-------------------------

1. Create Firestore Database
2. On firebase console navigate to Firestore Database -> Rules -> Edit Rules 
   replace the entire code to this:




```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```
