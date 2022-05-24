# Creating CI pipeline with Github Actions
In order to create the experience of automated testing we are going to set up a CI pipeline on github.

## Setting up the github Actions
Setting up GitHub Actions is very simple. It uses a .yml file that describes the process for the github actions.

The .yml file can be found under .github/workflows/gradle.yml,

go to the file `katacoda-code/.github/workflows/gradle.yml`{{open}}

We will initilize the file by adding `on` tag which specifies what github events should trigger a process/workflow. In this case we want to perform a proccess (described later) on Pull Requests to main and for direct pushes to main.
`runs-on` specifies which virtual machine to run on. Steps sets up the steps in a workflow, here we setup java JDK-18 and execute `gradle build` and `gradle test`.



Lets add that,
<pre class="file" data-filename="./katacoda-code/.github/workflows/gradle.yml" data-target="insert"  data-marker="# Add On Tag">
on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]
</pre>

To automatically trigger workflows we use the keyword 'on'. In this case it trigger a workflow (will be specified later) on the push and pull request to the main branch.

Now, lets specify the workflow to be triggered. This is done under the Jobs section.
We want to perform A build and test on github push and pull-request to main.
Lets add it,

<pre class="file" data-filename="./katacoda-code/.github/workflows/gradle.yml" data-target="insert"  data-marker="# Add Jobs">
jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: Set up JDK 18
      uses: actions/setup-java@v2
      with:
        java-version: '18'
        distribution: 'temurin'
    - name: Execute Build
      run: gradle build
    - name: Execute Tests
      run: gradle test
</pre>

In this we define a different jobs to be done, in this case build. For this jobs we define the steps and in the order that they need to be executed. We start by checking out the repository so that the workflow can access it. Then we set up JDK version 18 by using the setup command as well as specifying java-version and distribution. 

Now comes the more interesting part. Here we do two important steps. Namely the Execute of Build and Tests. Since we are using gradle and we know we have a script specified for it. We simply want it to run the gradle build and gradle test commands in the terminal.

Done! You have now successfully created a Github Actions.
