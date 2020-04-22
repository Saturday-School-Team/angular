# angular
Angular 8 , Material Design using fire base database

--adding angular materail write the command : ng add @angular/material

--adding angular firebase

--> go to google firebase console

--> Add a new project with your desired name

--> after successfull generiting the project go to database menu

--> go real time database option and create a database and chose the test mode from the wizard and then press enable

-- install the bellow packages with the command

npm i --s firebase angularfire2
--import 2 packages in the app.module.ts file

import { AngularFireModule } from 'angularfire2'

import { AngularFireDatabaseModule } from 'angularfire2/database'

import the avobe two modules in side the import array

--back to the firebase site and click on project overview and copy the config file

-- paste the copied firebase config file in side the environment.ts file

-import the environment.ts file in side the app.module.ts file

import {environment} from '../environments/environment'

--for initialize the firebase config need to add the below command

AngularFireModule.initializeApp(environment.firebaseConfig)

---for storing and retrive data using firbase - import two classes in the service class

import {AngularFireDatabase, AngularFireList } from 'angularfire2/database'

inject the AngularFireDatabase in the constructor like - constructor(private firebase: AngularFireDatabase){}

for getting list need to initialize the AngularFireList like - traineeList: AngularFireList;
