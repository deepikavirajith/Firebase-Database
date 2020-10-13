# Firebase-Database
Notes application in Android Studio with Firebase-Database.
Here i used firebase database from google, it is a free database used to store our data and i used Android studio to create the application.
I have implement RESTful API webservice that will be responsible for managing and storing in database with simple notes.
Firebase database provides realtime database, authentication, cloud storage etc., to create a firebase database go to www.firebase.google.com and click on a start button which is provided and there you can see a button containing CreateNewProject click on the button to start the project and gitve your app name, you can provide an name of your choice.
Go to your project and click on android application and here you need to provide your package name, your package name will be in your AmdroidManifests.xml file copy the package name and paste in the firebase website and click on add app button.
You will get a file name google-service.json download the file, copy the file and paste in app folder which is present in Android Studio project folder(If you create a new project in Android Studio there you can find a project folder).
Now you need to add a classpath provided by the firebase database to your Android app build.gradle(Project:your app name) as shown below,
 dependencies {
        classpath "com.android.tools.build:gradle:4.0.2"
       // Here you need to add the provided classpath
    }
    Now you need a add a apply plugin in the build.gradle(module:app)folder below the dependencies as shown below.
    dependencies {
    implementation fileTree(dir: "libs", include: ["*.jar"])
    implementation 'androidx.appcompat:appcompat:1.1.0'
    implementation 'androidx.constraintlayout:constraintlayout:1.1.3'
   implementation 'com.google.firebase:firebase-database:17.0.0'
    testImplementation 'junit:junit:4.12'
    androidTestImplementation 'androidx.test.ext:junit:1.1.1'
    androidTestImplementation 'androidx.test.espresso:espresso-core:3.2.0'
    implementation 'com.google.firebase:firebase-auth:19.4.0'

}
apply plugin: 'com.google.gms.google-services'
After adding sync the project, as we will work on authentication GO TO Docs provided on the left corner side and set-up a sign-in method of your choice and we need to add an authentication dependence in your build.gradle(module:app) folder as shown above to add authentication got to For Andoid folder in firebase database website and click on Get Started Guide and copy the link an paste (com.google.firebase:firebase-auth:19.4.0) in your android build.gradle(module:app) as shown above and sync the project.
Now go to Android Studio and got ot tools and click on firebase database and click on realtime-database and click on save ad retrive data, here you need to create a data base on open the existing database.
Now you need to work an Android Studio to perform CRUD operations for the application, download the coding part from the above listed file.
Webservice will accept HTTP calls for creating, reading, updating and deleting notes.
