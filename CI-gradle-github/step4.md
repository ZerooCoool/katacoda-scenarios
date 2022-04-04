# Adding Unit tests and Integration tests
Now that we have concluded the functionality of being able to run, build and test the code we are going to add a few more tests.

## Setting up the enviroment
In order to get best learning experience with Katacodas we need to reset the working enviroment for the oncomming assignments.

To do this go back to the root of the enviroment by run the following commands,

`cd `{{execute}}

Clone the github repo to set up the enviroment, by running this command.
`git clone https://github.com/Kubha99/katacoda-code.git`{{execute}}

Go to the directory,
`cd katacoda-code`{{execute}}

## Unit tests
It can already be seen that a unit test was created for the initial app.

Since there does not exist any functional logic in the application we will add a simple function called, simpleAddition in the main function.
Lets do that!

<pre class="file" data-filename="./katacoda-code/app/src/main/java/tutorial/MathOne.java" data-target="insert"  data-marker="// Create simple Java class here">
package tutorial;

public class MathOne{

  public int simpleAddition(int a, int b){
    return a+b;
  }
}
</pre>

<pre class="file" data-filename="./katacoda-code/app/src/main/java/tutorial/MathTwo.java" data-target="insert"  data-marker="// Create simple Java class">
package tutorial;

public class MathTwo{

  public int simpleMultiplication(int a, int b){
    return a*b;
  }
}
</pre>

Now lets add a unit test testing this functionality,
<pre class="file" data-filename="./katacoda-code/app/src/test/java/tutorial/AppTest.java" data-target="insert"  data-marker="// Add Unittest addition">
@Test
void simpleAdditionTest(){
  MathOne math1 = new MathOne();
  assertEquals(math1.simpleAddition(1,1), 2);
}
</pre>

<pre class="file" data-filename="./katacoda-code/app/src/test/java/tutorial/AppTest.java" data-target="insert"  data-marker="// Add unittest multiplication">
@Test
void simpleMultiplicationTest(){
  MathTwo math2 = new MathTwo();
  assertEquals(math2.simpleMultiplication(1,1), 1);
}
</pre>

## Verify
Lets verify that everything is working and the tests are good.

`gradle test`{{execute}}


## Add Integration test
In this section we will perform a integration test where we will have two seperate classes with different functionality and test that their integration is working correctly. The main java application App.java will then integrate the functionalites in both of them.

These classes could be in different modules or components in a real life project, however to simplify it in our demo we will create two classes.

Lets create the functionality of integration,
<pre class="file" data-filename="./katacoda-code/app/src/main/java/tutorial/App.java" data-target="insert"  data-marker="// Add Integration functionality">
public int squareSum(int a, int b){
  MathOne m1 = new MathOne();
  MathTwo m2 = new MathTwo();
  return m2.simpleMultiplication(m1.simpleAddition(a,b),m1.simpleAddition(a,b));
}
</pre>

Lets create the Integration test.

<pre class="file" data-filename="./katacoda-code/app/src/test/java/tutorial/AppTest.java" data-target="insert"  data-marker="// Add Integration Test">
@Test
void simpleIntegrationTest(){
  App app = new App();
  assertEquals(app.squareSum(2,3), 25);
}
</pre>

## Verify
Lets verify that everything is working and the tests are good.

`gradle test`{{execute}}

Note: sometimes Katakoda acts weirdly, remove the codes under section Add integration test and manually copy paste them into file and it should work fine!
