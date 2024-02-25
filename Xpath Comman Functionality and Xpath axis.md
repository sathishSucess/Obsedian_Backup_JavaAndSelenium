

![[Screenshot 2023-03-14 190847.png]]

![[Screenshot 2023-03-14 191325.png]]
![[Screenshot 2023-03-14 201035.png]]
![[Screenshot 2023-03-14 201055.png]]
![[Screenshot 2023-03-14 201103.png]]
![[Screenshot 2023-03-14 201136.png]]
![[Screenshot 2023-03-14 201605.png]]
![[Screenshot 2023-03-14 201639.png]]
![[Screenshot 2023-03-14 201729.png]]
![[Screenshot 2023-03-14 201851.png]]
![[Screenshot 2023-03-14 202012.png]]
![[Screenshot 2023-03-14 204152.png]]





 

# 2.Xpath axes:

*Finding of unknown WebElement by using known WebElement is called Xpath axes.

By using relationship ,we are going to find the unknow WebElement the Relation Are;
- ancestor
- parent
- child
- following-sibling
- preceding-sibling

#### Syntax of Xpath

//xpath of known element//relation::xpath of unknown WebElement
****for facebook password too username  the flow is sample example explained in syntax

//input[@id='pass']//ancestor::div[@class='_6lix']//preceding-sibling::div//child::input[@id='email']

#### Common functionality: 
**{Question: What ever, country i choose ,check the check Box }

String country="Albania";
String xpath="//strong[text()='"+country+"']/parent::td/preceding-sibling::td";
driver.findElement(By.xpath(xpath));



### Tabel example:

![[Screenshot 2023-03-15 085438.png]]
![[Screenshot 2023-03-15 085505.png]]
 
 
 
 
#### Question : print Second Row And Second Coloum using xpath axis
 ![[Screenshot 2023-03-15 085536.png]]


#### Question : check the chech box  before afghanistan

![[Screenshot 2023-03-15 090009.png]]

#### Question : Check the Check box  from kabul

![[Screenshot 2023-03-15 090050.png]]


#### Task : amzon site --> select a product and in that product page-->create xpath axis from [product name] to [Exchange offer].

![[Screenshot 2023-03-15 091538.png]]

#### Task: Question in Photo and Mention below

![[Screenshot 2023-03-15 091627.png]]
- Get the count of number of coloumns
- Get the count of number of Rows
- Get the Progress value of 'Learn to interact with Elements'
- Check the Vital Task for the least completed progress