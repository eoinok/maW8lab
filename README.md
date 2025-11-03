This lab guides you step-by-step through creating a Firebase project, registering a Web app, creating Firestore rules/indexes, obtaining the `firebaseConfig` object, and running the provided Expo app which writes to Firestore.

> **Prerequisite:** The starter repo already contains these files:
> - `App.js`
> - `firestoreConfig.js` (placeholder)
> - `.firebaserc`
> - `firebase.json`
> - `firestore.rules`
> - `firestore.indexes.json`
> - `package.json`, `app.json` (Expo files)


## Step 1 — Install prerequisites
Install Expo CLI (optional but recommended) and the Firebase CLI.

```npm install -g expo-cli```

install the Firebase CLI
```npm install -g firebase-tools```

## Step 2 -- Login to Firebase type the following on the CLI of your repo

``` firebase login ```

confrm login by typing
``` firebase login list ```

## Step 3 — Create a new Firebase project
Create a project using a globally unique project ID (lowercase, letters/numbers/hyphens only).
``` firebase projects:create <project-id> --display-name "<Display Name>" ```
Set the created project as the default for this folder:
``` firebase use <project-id> ```

## Step 4
Create a Web app entry inside the Firebase project (this produces an App ID):
``` firebase apps:create web "<App Name>" --project <project-id> ```
THe following command lists all your projects, you should see only the project you've just create in the list
``` firebase projects:list ```

## Step 5
Use the App ID (format 1:...:web:...) to print the SDK configuration. ***Do not use the project ID here.***
``` firebase apps:sdkconfig web <app-id> ```
Copy the printed firebaseConfig object and paste it into firestoreConfig.js where the placeholder comment is:

## 
