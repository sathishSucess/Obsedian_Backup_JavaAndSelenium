*Synchronization: Matching the speed of the Browser with the speed of the selenium 
**syncronization can be achieved using waits

### Two Different types of waits

##### 1.Static wait
  Time Mentioned completed -process 
     Thread.sleep();
##### 2. Dynamic wait
before the time completion - process
a) Implicit wait
b)Explicit wait
c)Fluent Wait

## Implicit wait
it resolves the Synchronization of locating the Elements once intilized
###### Syntax: 
     driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));

## Explicit wait

it Resolves the Synchronization of all the method including location of element 
Every method initialization
##### Syntax:
    WeDriverWait wait=new WebDriverWait(driver,10);
	 WebElement         until=wait.until(ExpectedConditions.visibilityOfElementLocated(By.name("username")));
	 until.sendKeys("Sll");

## Fluent Wait
- Both implicit wait and explicit wait has the **Default polling period of 500milli second.
- User defined frequency or polling period
##### Syntax:
    Wait<WebDriver> wait=new FluentWait<WebDriver>)(driver).withTimeOut(Duration.ofSecond(50)).pollingEvery(Duration.ofSecond(10)).ignoring(Exception.class);  

![[Screenshot 2023-03-17 212445 1.png]]


