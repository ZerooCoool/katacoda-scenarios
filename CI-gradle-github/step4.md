# Adding Unit tests and Integration tests
Now that we have concluded the functionality of being able to run, build and test the code we are going to add a few more tests.

## Setting up the enviroment
In order to get best learning experience with Katacodas we need to reset the working enviroment for the oncomming assignments.

To do this go back to the root of the enviroment by run the following commands,

`cd `{{execute}}

Clone the github repo to set up the enviroment, by running this command.
`git clone git@github.com:Kubha99/katacoda-code.git`{{execute}}

Go to the directory,
`cd katacoda-code`{{execute}}

## Unit tests
It can already be seen that a unit test was created for the initial app.

Since there does not exist any functional logic in the application we will add a simple function called, simpleAddition in the main function.
Lets do that!

ADD THE SIMPLE ADDITION command
ADD simpleMultiplication command

Now lets add a unit test testing this functionality,

ADD simpleAdditionTest command
ADD simpleMultiplicationTest command

## Add Integration test
In this section we will perform a integration test where we will have two seperate classes with different functionality and test that their integration is working correctly. The main java application App.java will then integrate the functionalites in both of them.

These classes could be in different modules or components in a real life project, however to simplify it in our demo we will create two classes.

Lets create the Integration test.

ADD INTEGRATION TEST command

## Verify
Lets verify that everything is working and the tests are good.

`gradle test`{{execute}}
