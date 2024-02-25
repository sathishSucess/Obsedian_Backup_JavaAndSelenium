*Test Next generation or
Test New generation

## Advantage of Test Ng over  Junit Frame work
1. Html report can be generated
2. prioritize
3. Invocation count
4. skip the test case 
5. pass parameter
6. grouping in testing
7. Parallel Execution
8. rerun

#### How to Integate testng in maven project
Step 1 create maven Project
Step 2 add dependeceies
           WebDrivermanager
           Selenium -java
           Apachi poi ooxml
           testng

Step 3 install plugin

#### Annotation used in Testng
@Before Suite
@Before test
@Before Class
@Before Method
@Test
@AfterMethod
@AfterClass
@AfterTest
@AfterSuite

Suite- Collection of test
Test- Collection class
Class-Collection method

![[Screenshot 2023-03-07 053738.png]]
***Always run annotation use to run a method which is depend on second method where assertion fails. 



### TestNg 2nd=>vedio
1. Assertion
a)hard Assert
	1. Assert.assertTrue
	2. Assert.assertFalse
	3. Assert.assertEquals
b)Soft Assert
*same metod are present like hard assert.
2. Parallel Excution
3. data provider
4. testng rerun

#### HARD ASSERT
![[Screenshot 2023-03-07 053738.png]]

****HARD Assert ,when assertion get failed ,the next line of code does't perform to run by HARDAssert.


#### Soft Assert

Soft Assert is a class 
Soft Assert s=new Soft Assert();

![[Screenshot 2023-03-07 062825.png]]

****Soft Assert ,when assertion get failed ,the next line of code perform to run by SoftAssert.
to get error msg in console assertAll() method.


## Data Provider

*To provide bulk amount of data to the test case and execute the testcase multiple times Every Set of data

![[Screenshot 2023-03-07 090308.png]]


## TestNg Rerun
*whenever a test case is failed in testng,then we can execute the failed test case alone muiltiple times
 
Step 1: create a class and implement IAnnotationTransformer (Interface)
            This interface will monitor the execution going on in another class ,if any method
            failed then it will trigger the class which implemented IRetry Analyzer

Step 2: This interface will add an method  called as transform
Step 3: Inside the Method use the following logic getRetryAnalyzer
		setRetryAnalyzer
Step 4: Create one more class
Step 5: This class should implement the IRetryAnalyzer(Interface)
Step 6:This interface will add a method called as retry()
Step 7: This method will determine how many does a failed method will execute
Step8: In testng.xml file add a tag name Called as
###### Listener Image:
![[listeners.png]]

## Create testng rerun example:
![[Screenshot 2023-03-07 120143.png]]
![[Screenshot 2023-03-07 120134.png]]
![[Screenshot 2023-03-07 115932.png]]
![[Screenshot 2023-03-07 121121.png]]

![[Screenshot 2023-03-07 121206.png]]


![[Screenshot 2023-03-07 121215.png]]
***When Assertion Set as false  result is shown below image

![[Screenshot 2023-03-07 121229.png]]




## Parallel Excution

*parallel excuting the method in a class is parallel execution. 
or 
Excuting the more than methods parallely is called as parallel execution.

when a method runned line by line by is synochronised way excecution.

=>Suite-Collection of Test
=>Test-Collection of class
=>Class - Collection of methods
##### Example;
***Step1:
![[Screenshot 2023-03-07 192412.png]]


***Step2:
![[Screenshot 2023-03-07 192348.png]]





## Parallel execution with cross browser testing

two chrome browser
two firefox browser  ,tread count ='4'
![[Screenshot 2023-03-07 083141.png]]

![[Screenshot 2023-03-07 083204.png]]
##### TestNg.xml {Practice told by ramsir}

<suite name="Suite1" parallel="method" thread-count=2">
<test name ="Test1">
<classes>
<class name="packagename.classname"></class>
<class name="packagename.classname"/>
</classes>

</test>
</suite>    




