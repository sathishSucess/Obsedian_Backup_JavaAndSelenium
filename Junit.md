
##### Junit  frameWork
unit testing (Testing a single module alone)
- Using Junit FrameWork ,we can verify the test case

##### How to intergate junit Framework with Maven Project
Step1: Create a  maven project
Step2: Add Dependancies
			1. WebDrivermanager
			2. Selenium-java
			3. apachi poi ooxml
			4. Junit
Step3: Create a class
Step4: write your automation script inside the annoatations
Note:**All the Annoatations should be used on top of the methods

@BeforeClass -- the method will execute before the execution of all the other method  in class 
@Before-- The method will execute every time before the execution of each [@Test method]
@Test--  Mandatory annotation(multiple times)
@After-- the method will execute every time after the execution of each [@Test method ],and it used find time different complete entire testcase in@Test method
@AfterClass-- the method will execute after the execution of all the other methods in class 

Note:**All methods than one @Test methods (ascending order of method name )

![[Screenshot 2023-04-25 101211.png]]



### @Ignore annotation

![[Screenshot 2023-04-25 092426.png]]
Note:**To Ignore any @Test methods use @Ignore annotation.
@Ignore Does not work other annotation


Note: 
**- @Before and @After used for verification process before and after of test case.
**- @AfterClass is close the browser.










# Verification in Junit

Checking with Expected result

Assert - pre defined class

assertTrue(boolean)-- static method  ---- (true--following lines will execute,false--will not execute)
assertFalse(boolean)-- static method----(false--will execute,true-will not execute)
assertEquals(expected,actual)--static method-------(excpected=actual--will execute)
### Base Class
![[Screenshot 2023-04-25 201926.png]]
### Pom{Locators are managed in  private}
![[Screenshot 2023-04-25 201739.png]]

![[Screenshot 2023-04-25 100126.png]]
### Task :Ramsir said to Practice 
junit :is used to test particular module test case[ login page] or[ particular webpage of application] 

- same program practice 
- and adactin hotel practice