##### 1--Vedio
80% cucumber 20%TestNg in companies
is a Frame Work
1.  **TDD Frame work (Test Driven Development )
- From Requirement ---> Test Case -----> Automation Script 
 - Only Techinical Person Can Under Stand
 - Tools : TestNg,Junit
 
1. **BDD Framework(Behaviour Driven )
- From the Requirement --File(Step By Step Application workFlow )---TestCase ----AutomationScript
- Non Technical person Can Also underStand
- Tools: Cucumber ,Jbheave,SpecFlow

### Flow of project
![[Screenshot 2023-03-09 134259 1.png]]

Cucumber 
It also called As Hybrid Framework
its Work with Any TDD Frame That is called HybridFrame Work
Cucumber + Junit
Cucmber +TestNg

How to Configure Cucumber Project In maven
Step 1: Create maven project
Step2:
Add Dependancies
WebDriver Manger
Selenium -Java
Apachi Poi.ooxml
cucumber -Junit 4.2.0
Cucumber -java 4.2.0
Step 3: Install Cucumber plugins
Step4: Create File under Src/test/resourse with the extension ' .feature'    Feture File

Step by Step Application workFlow in Simple english Language
	
	        Feature: Test Scenrio
	        Scenario: Test Case
	        Given  pre condition
	        When   action performed 
	        And    addtional action
			Then    TO Performe Validation Operation
###### Gherkin Keyword: Feature ,Scenario,Given,When, And  ,Then

Step 5: Create a class under the src/test/java
		Name this class as TesttRunnerClass
		In this class use two annotation
		i)@RunWith (Cucumber.class)
		ii)@CucumberOptions
			1)feature -path of the feature file within double quotes
			2)dryRun- true/flase
				dryRun= true(All the steps in Feature file match with the method in the Step Definition class) snipts genereated if methods missing.
			dryRun:false-->Excution take place. 
			
3)Glue-package name of  the step definition class.   ---> feature file used to compare with StepDefinition class.
		![[Screenshot 2023-04-20 203130.png]]
Step6: generate the Snippets
Step7: Create one more class under src/test/java and write the automation script
Step8: Execute

### File As to Created:

![[Screenshot 2023-04-20 205435.png]] 

### Feature File:

![[Screenshot 2023-04-20 210204.png]]




# 2nd Vedio --> 

### Cucumber Topic As to Cover Follows

1. Scenario Outline
2. JVM Report
3. Cucumber Option
4. Cucumber Architecture

## Scenario Outline

- To pass bulk no of data from the feature file into the scenario.
- For Every set of data,each and every line in scenerio will execute multiple times
- Whenever we are using Scenario outline then [Example] Keyword is Mandatory

![[Pasted image 20230420212135.png]]

Question1: When ever u r using  Scenario Outline wheather 'Example' Keyword Is mandotory
ans: Yes
Question2: Wheather we give 'Example 'keyword in Scenario
ans: no.

## Cucumber Option


1. features
		Specify the path of the feature file
2. dry run
	   true,noExecution ,steps in feature files= step in stepDefinition- no snippets
	   dryRun- false ,execution
3. glue - package name of the step definition class
		 to bind the step in the feature file with the method in the step definition class 
4. monoChrome -true (Console will be in better readable formate),default value --false.
5. plugin- to generate the report
			1. html report  ---"html: path of the folder to store report"
			2. json report ---"json: path of the folder to store report\\filename.json"
			3. xml report ---"xml: path of the folder to store report\\filename.xml"
## Eg:
![[Screenshot 2023-04-25 061723.png]]

*Question:
Tell about Cucumber options?







## JVM Report
  
  To convert the json machine formate into human underStandable format
	  Step 1: Add a dependency called as [cucumber reporting dependency ]
  step2: Create a class under step definition package
  step3: Create static method and pass the json files as the argument 
  step4: Inside the class create object for File(java.io)
  step5:Create object for pre defined class called as configuration 
  Step6: in this class,addClassification(to change the report with user defined fields )
  Step7:Create an object for List and add json file in the List
  Step8: create an object for pre defined class called as Report Builder
            - The purpose is to bind the json fileds and user defined field from configuration
  
  Step9: In the Test runner class use an annotation called As @AfterClass
  because this annotation used beacause of cucumber -junit  combination

**Note:@AfterClass    '' rules" 
the method should be in public static 
  

#### Generate Report Class

![[Screenshot 2023-04-25 062017.png]]

### @AfterClass to produce custom JVM report
![[Screenshot 2023-04-25 063537.png]]


### Report generated in  'target ' Folder

![[Screenshot 2023-04-25 064211.png]]

![[Screenshot 2023-04-25 064415.png]]





## Cucumber Architecture

*what  are all steps we followed in creating cucumber project is ***Cucumber Architecture

![[Screenshot 2023-04-25 071608 1.png]]