This lab guides you step-by-step through creating a Firebase project, registering a Web app, creating Firestore rules/indexes, obtaining the `firebaseConfig` object, and running the provided Expo app which writes to Firestore.
The app departs from the approach of using Expo Snacks used in previous labs. This project will be completed using vscode and executing commands on the command line.

> **Prerequisite:** The starter repo already contains these files:
> - `App.js`
> - `firestoreConfig.js` (placeholder)
> - `.firebaserc`
> - `firebase.json`
> - `firestore.rules`
> - `firestore.indexes.json`
> - `package.json`, `app.json` (Expo files)

## Step 1 - register on Firebase
Before proceeding visit firebase.google.com and login using your gmail/google account. If you don't already have one you'll have to create one. Once you have registered on firebase you can proceed with connecting it to your React Native App

## Step 2 — Install prerequisites
Install Expo CLI (optional but recommended) and the Firebase CLI.

```
npm install -g expo-cli
```
install the Firebase CLI
```
npm install -g firebase-tools
```

## Step 3 -- Login to Firebase type the following on the CLI of your repo

```
firebase login
```
A web broswer will open so that you can enter your google credentials and login to firebase. Confrm login by typing
``` 
firebase login list
```
## Step 4 — Create a new Firebase project
Create a project using a globally unique project ID (lowercase, letters/numbers/hyphens only). Replace ***project-id*** and ***"Display Name"*** with your chose project id and name (drop the angled brackets)
``` 
firebase projects:create <project-id> --display-name "<Display Name>"
```
Set the created project as the default for this folder:
``` 
firebase use <project-id>
```
## Step 5
Create a Web app entry inside the Firebase project (this produces an App ID):
``` 
firebase apps:create web "<App Name>" --project <project-id>
```
THe following command lists all your projects, you should see only the project you've just create in the list
``` 
firebase projects:list
```

## Step 6
Use the App ID (format 1:...:web:...) to print the SDK configuration. ***Do not use the project ID here.***
``` 
firebase apps:sdkconfig web <app-id>
```
Copy the printed firebaseConfig object and paste it into firestoreConfig.js where the placeholder comment is:

## Step 7
Run your react native project from the command line by typing
```
npx expo start
```
Choose ***w*** from the list of menu alternatives to run your project in local web mode

add a username and email and click on the button to save your data to firebase

Go to http://console.firebase.google.com

Under projects and workspaces, click on your project id. Under project shortcuts select Firestore Database. Look in the users collection and see if any data has been added. If everything worked correctly your app is saving data to your firestore database in the cloud.

