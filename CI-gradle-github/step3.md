# Setting up a project with Gradle

## Crreating the project from the scratch
In this section we will go thorugh how to setup a Java project with gradle. 
Run the following command, 

`gradle init`{{execute}}

1. Select option 2, since we are going to be building an application with Java. 

2. In the options section enter '3' for Java. 

3. Enter Default

4. Enter 1 for groovy

5. Enter Default

6. In this tutorial we will be using JUnit Jupiter for Testing, Enter 4

7. Enter Default

8. Enter tutorial - it is important that you enter precisly 'tutorial' for this tutorial


Note that these are the project setting we entered for this tutorial and can can be customized depending on the project that you want to use. 

## Verifyin the project creation

You should now new folders being created. We will go through the some important ones.

1. app/ 
The App folder contains the java application and the testNG for the project.

2. build.gradle
Going into the app/ folder we see that there is a file called build.gradle. This is a groovy file that contains important information about gradle. 
If we examine this file we will find the dependencies that this project has and how these dependencies are resolved (mavenCentral). We can also see information about the test plattform. 

3. Gradlew.bat and gradlew
These are wrappers for Gradle for Windows or Linux/OS


## Running the tests and application
Now in order to verify that everything is working, examine the javafile under app/src/main/java/"Package name selected"/App.java
After that you should now see that this file will print a greeting if run, lets check it out by running it.

`gradle run`{{execute}}

Examine the test file which is located at app/src/test/java/test, 
Lets run the tests, 

`gradle test`{{execute}}

