# Creating CI pipeline with Github Actions
In order to create the experience of atomated testing we are going to set up a CI pipeline on github.

## Setting up the github Actions
Setting up GitHub Actions is very simple. It uses a .yml file that describes the process for the github actions.

The .yml file can be found under .github/workflows/gradle.yml,

We will initilize the file by adding on what github commands we will perform the process. In this case we want to perform a process (described later) on Pull Request to main and direct push to main.

Lets add that,
COMMAND: ADD ON: PUSH ETC

Now, lets create a job or a process to be executed if abovementioned tasks are performed. This is done under the Jobs section.
We want to perform A build and test on github push and pull-request to main.
Lets add it,
COMMAND: ADD Jobs

Done! You have now successfully created a Github Action.
