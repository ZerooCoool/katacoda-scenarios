# What is Gradle?
Gradle is a flexible cross-language open-source build automation tool. It is used in the development process to automate compilation, testing, deployment and publishing of your software. It is fast and customizable with a rich ecosystem of plugins, it also gives you the ability to use cached builds for optimization. Using gradle to automize the software development process will help increase the quality of the code and make it more efficient by automating most of the process.

# Why Gradle and its Alternatives
As already explained above, Gradle is a build automation tool. It is a tool we can use to automate and increase efficency in our DevOps. There are other build automation tools that one can use, for example CMake, GNU Make, and Maven which are all free and open source. Depending on the project different build automation tools might be a better fit. The benefits of using Gradle has already been described in the introduction, but to clarify Gradle is very focused on maintainability, performance, and flexibility. It supports many different projects and languages such as Java, C++, Android projects, Python, Groovy projects, etc. It is known for its high-speed performance since it uses build cache and is faster than some alternatives such as Maven which does not support this functionality. Other build automation tools might be focused on one project phase while Gradles goal is to add functionality to a whole project. On top of this Gradle is highly customizable making it a good fit for certain projects if you are feeling ambitious.

# Installing Gradle
Depending on your current system, there are different ways to download Gradle. The only prerequisity needed is Java SDK 8 or higher. To check if Java is installed you can enter:
</br> `java -version`{{execute}}

If you are on a system which has Brew installed you can easily install Gradle by doing:
</br> `brew install Gradle`

For other ways to install Gradle including manual installation follow the steps on [Installing Gradle](https://gradle.org/install/).

To check if Gradle has been installed correctly you can run:
</br> `gradle --version`{{execute}}

# Basic Gradle Commands

Some basic gradle commands are `init`, `run`, `build` and `test`.

</br> `init` will create a new gradle project.
</br> `build` will create a build of the project.
</br> `test` will run the test task for all subprojects within the directory.
</br> `run` will assemble the application and execute some script or binary.
