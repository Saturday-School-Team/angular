# angular

Tools and Technology:  Angular8, Material design, google firebase database.

--> How to add angular material in the project: go to your project then write the command "ng add @angular/material" in the integrated terminal in VS code.

--How to configure angular firebase database :

--> using your browser go to "https://firebase.google.com/" then click on "Go to console" buttone in the right corner of the page. 

--> Click on "+ Add Project"

--> Write your project name in the textbox. then click on "Continue" button

--> Dissabled the toggole from "Enable Google Analytics for this project". then press on "create project" button. after success press on "continue" button

--> From the left panel click on "database menu" go to "Realtime Database" located in the bottom of the page.

--> Click on "create database" mark the Radio Button as "Start in test mode" then click on "enable" button


--> Install the below packages with the command inside your project with the integrated terminal in VS code.

   "npm i --s firebase angularfire2"

--> import 2 packages in the app.module.ts file

import { AngularFireModule } from 'angularfire2'

import { AngularFireDatabaseModule } from 'angularfire2/database'

--> import the avobe two modules in side the import array

--back to the firebase panel in the browser and click on "project overview" and the  and copy the config file from 
 
 "Get started by adding Firebase to your app" under this line you will find a icon like </>

--> paste the copied firebase config file inside the environment.ts file

--> import the environment.ts file in side the app.module.ts file

  import {environment} from '../environments/environment'

--> for initialize the firebase config need to add the below command in the import arry of add.module.ts file

  AngularFireModule.initializeApp(environment.firebaseConfig) 

---for storing and retrive data using firbase - import two classes in the service class

import {AngularFireDatabase, AngularFireList } from 'angularfire2/database'

inject the AngularFireDatabase in the constructor like - constructor(private firebase: AngularFireDatabase){}

