# What is Gradle?
Gradle is a flexible cross-language open-source build automation tool. It is used in the development process to automate compilation, testing, deployment and publishing of your software. It is fast and customizable with a rich ecosystem of plugins, it also gives you the ability to use cached builds for optimization. Using gradle to automize the software development process will help increase the quality of the code and make it more efficient by automating most of the process.

# Installing Gradle
Depending on your current system, there are different ways to download Gradle. The only prerequisity needed is Java SDK 8 or higher. To check if Java is installed you can enter:
</br> `$ java -version`{{execute}}

If you are on a system which has Brew installed you can easily install Gradle by doing:
</br> `$ brew install Gradle`{{execute}}

For other ways to install Gradle including manual installation follow the steps on [Installing Gradle](https://gradle.org/install/).

To check if Gradle has been installed correctly you can run:
</br> `$ gradle --version`{{execute}}

# Basic Gradle Commands

Some basic gradle commands are `init`, `run` and `test`.

</br> `init` will create a new gradle project.
</br> `test` will run the test task for all subprojects within the directory.
</br> `run` will assemble the application and execute some script or binary.
