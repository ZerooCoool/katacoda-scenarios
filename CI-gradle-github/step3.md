
## Setting up the katakoda enviroment
For this part of the tutorial we will set up the enviroment by the following commands,

Run the following commands to create a new folder for the enviroment.
`mkdir newProject`{{execute}}

Move to that enviroment.
`cd newProject`{{execute}}


## Creating the project from the scratch
In this section we will go thorugh how to setup a Java project with gradle.

Run the following command,

`gradle init`{{execute}}

1. Select option 2, since we are going to be building an application with Java.

2. In the options section enter '3' for Java.

3. Enter 1 for groovy

5. In this tutorial we will be using JUnit Jupiter for Testing, Enter 4

6. Enter Default

7. Enter Default


Note that these are the project setting we entered for this tutorial and can can be customized depending on the project that you want to use.

## Verifyin the project creation

You should now see that new folders have been created. We will go through some of the important ones.

1. src/ - Contains the java application and the testNG for the project.

2. `newProject/build.gradle`{{open}} - This is a groovy file that contains important information about gradle.
If we examine this file we will find the dependencies that this project has and how these dependencies are resolved (mavenCentral). We can also see information about the test plattform.

3. Gradlew.bat and gradlew - These are wrappers for Gradle for Windows or Linux/OS


## Running the tests and application
Now in order to verify that everything is working, examine the javafile under `newProject/src/main/java/newProject/App.java`{{open}}
After that you should now see that this file will print a greeting if run, lets check it out by running it.

`gradle run`{{execute}}

Examine the test file which is located at `newProject/src/test/java/newProject/AppTest.java`{{open}},
Lets run the tests,

`gradle test`{{execute}}
