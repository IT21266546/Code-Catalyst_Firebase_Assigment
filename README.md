# Code-Catalyst_Firebase_Assigment
## **Objective:**

Create an authentication system using Firebase, integrating various authentication providers, and managing user data using Firestore and Cloud Functions. This assignment aims to deepen your understanding of Firebase authentication, Firestore database management, and serverless functions.

# Firebase Initialization
PS C:\Users\ACER\Desktop\Intern\Code-Catalyst_Firebase_Assigment\backend> firebase init

     ######## #### ########  ######## ########     ###     ######  ########
     ##        ##  ##     ## ##       ##     ##  ##   ##  ##       ##
     ######    ##  ########  ######   ########  #########  ######  ######
     ##        ##  ##    ##  ##       ##     ## ##     ##       ## ##
     ##       #### ##     ## ######## ########  ##     ##  ######  ########

You're about to initialize a Firebase project in this directory:

  C:\Users\ACER\Desktop\Intern\Code-Catalyst_Firebase_Assigment\backend

? Are you ready to proceed? Yes
? Which Firebase features do you want to set up for this directory? Press Space to   
select features, then Enter to confirm your choices. Firestore: Configure security   
rules and indexes files for Firestore, Functions: Configure a Cloud Functions        
directory and its files, Storage: Configure a security rules file for Cloud Storage, 
Emulators: Set up local emulators for Firebase products

=== Project Setup

First, let's associate this project directory with a Firebase project.
You can create multiple project aliases by running firebase use --add,
but for now we'll just set up a default project.

? Please select an option: Use an existing project
? Select a default Firebase project for this directory: fir-assigment-7f517
(firebase-assigment)
i  Using project fir-assigment-7f517 (firebase-assigment)

=== Firestore Setup

Firestore Security Rules allow you to define how and when to allow
requests. You can keep these rules in your project directory
and publish them with firebase deploy.

? What file should be used for Firestore Rules? firestore.rules

Firestore indexes allow you to perform complex queries while
maintaining performance that scales with the size of the result
set. You can keep index definitions in your project directory
and publish them with firebase deploy.

? What file should be used for Firestore indexes? firestore.indexes.json

=== Functions Setup
Let's create a new codebase for your functions.
A directory corresponding to the codebase will be created in your project
with sample code pre-configured.

See https://firebase.google.com/docs/functions/organize-functions for
more information on organizing your functions using codebases.

Functions can be deployed with firebase deploy.

? What language would you like to use to write Cloud Functions? TypeScript
? Do you want to use ESLint to catch probable bugs and enforce style? Yes
+  Wrote functions/package.json
+  Wrote functions/.eslintrc.js
+  Wrote functions/tsconfig.json
 Storage Emulator
? Which port do you want to use for the auth emulator? 9099
? Which port do you want to use for the functions emulator? 5001
? Which port do you want to use for the firestore emulator? 8080
? Which port do you want to use for the storage emulator? 9199
? Would you like to enable the Emulator UI? Yes
? Which port do you want to use for the Emulator UI (leave empty to use any available port)?   
? Would you like to download the emulators now? Yes

i  Writing configuration info to firebase.json...
i  Writing project information to .firebaserc...
i  Writing gitignore file to .gitignore...

+  Firebase initialization complete!
+  
change package.json

"serve": "npm run build && firebase emulators:start --only functions" ;
to

"serve": "npm run build && firebase emulators:start --only functions,firestore,auth,storage",