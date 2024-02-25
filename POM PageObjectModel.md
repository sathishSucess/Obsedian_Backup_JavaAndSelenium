To avoid the stale element Reference Exception
	StaleElementreference: if a WebElement reference become old ,when it is not attached  to the Dom page then the element reference become old  and it is called as Stale ElementReference
	
Step1: Create a class for Every page in the          Website
Step2: Apply POJO class Concepts
           Declare private Variables
           Use getters method only
Step3: use annotations
          @FindBy--- one locators for one WebElement
          @FindBys-- Multiple locators for one WebElement (And operators)
          @FindAll---Multiple locators for one WebElement (Or operators)
### eg: Annotation
![[Screenshot 2023-04-24 001552.png]]
Step4 :Page Object Model Class Should Extends the Base Class

Step5:   Declare a constructor in page Object model Class.
1. Inside the Constructor
2. PageFactory.initElements(driver,this)----> is to intilize element (not allow locators to become stale element)or(recreating)
*Note: it is intilize througth ['driver]' and intilize in same class so ['this ']keyword used.

pageFactory ---Class
initElements-- Static method



## Locators Of Each Webpage Eg:

![[Screenshot 2023-04-24 001905.png]]
![[Screenshot 2023-04-24 002133.png]]
## Base Class eg:

![[Screenshot 2023-04-24 002142.png]]
## Object Creation eg:
![[Screenshot 2023-04-24 002255.png]]
#### Note:
Even Though Memory wastage is high ,Every WebPage Object is Created without using 'extends' keyword


#### Ram sir task

Full automation Adactin booking Hotel using {page object model POM}