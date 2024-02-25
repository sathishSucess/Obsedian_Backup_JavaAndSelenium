
 
# Frist vidio intro 
## Why we go for FrameWork
 
 1. In Selenium we will maintain the code and the data in the same class
 2. Code and the data to be maintained seperately
 3. To increase the code reusability
 4. If the number of jar files are more than it is difficult to manage
 5.  Build -Collection of programmes onces excuted that will serve certsin purpose
 6. Build Management Tool-- Maven ,Ant ,Gradel
 7. Managing -- Serving the puropose of Framework
 8. Maven- Most probably used build management tool
 
### Diffrence Between java Project /Maven Project

**java Project
1. Pre defined files are called as jar
2. Folder Structure : JRE System Libery
 
 **Maven
 
 1. Pre Defined files are called as dependancies
 2. Folder Structure
      src/main/java ---- Developers code
        src/main/resourses ---- Developers data
        src/test/java ---- tester code
        src/test/resourses ---- Testers data 
       JRE System Library--- PreDefined library files of java
       src  --- Source code
       target--- To Store Reports after Execution
       pom.xml---- To add Dependancies
## How to Configure maven and Java

![[Screenshot 2023-04-23 211033.png]]
![[Screenshot 2023-04-23 211159.png]]





## Create a maven project
 
GroupId-- package name
ArtifactId-- Project name

Click -pom.xml --Add dependancies

To Use Selenium projects
Add two dependancies
1. WebDriverManager dependency-- to setup the Browser
2. Selenium java dependency-- To use the pre defined library files of selenium
![[Screenshot 2023-04-21 085410.png]]


**Under src/test/java   -- we maitain the code
Under src/test/Resourses -- we maintain Data. like Excel Data
eg:
![[Screenshot 2023-04-21 091357.png]]



#### Data Driven FrameWork
Online--> Database-- OracleDb,MangoDb,GDrive
Offline --> Excel

#### How read Data From Excel from Single row and coloum

Step1- Add apachi poi ooxml dependency
step 2- File -- predefined Class(java.io) , create Object
step 3-FileInputStream --(java.io)--object--File Not Found Exception
Step4- Workbook -- interface (apachi poi ooxml)--Object
Workbook w=new XSSFWorkbook(); -----Io Exception
Workbook -- collection of sheets
Row-- collection of cells
{Workbook,Sheet,Row}--->Interface
Step 5- Get the Sheet from the Workbook
Step 6-- Get the Row from Sheet
Step 7-- Get the Cell from Row
Step 8-- Get the String data from cell
![[Screenshot 2023-04-21 085354.png]]


## 2 nd Vedio

### How to read Multiple data from Excel,Numerical ,Date

Get The Sheet from the WorkBook
Sheet 1: Get the no of Rows Filled with Data 
           getPhysicalnumberOfRows();
Step 2: Get the no of cells filled with data 
           getPhysicalNumberOfCells()
Step 3: Find the Type Of Data
			getCellType();-----> 1 , 0
			1-- String Value
			2 -- Numeric value
		DateUtil.isCellDateFormated(cell)--> true (Date)
![[Screenshot 2023-04-22 095036.png]]
![[Screenshot 2023-04-22 095145.png]]

## 3rd Vedio
## How To Write Data in Excel

Step 1:  File  --->Object
Step 2: FileOutputStream---> Object
Step 3: Workbook  --Object
Step 4: Create sheet
Step 5: Create Row
Step 6: Create cell
Step 7: Set the Value for Cell
Step 8: Write The Excel
![[Screenshot 2023-04-22 101722.png]]
![[Screenshot 2023-04-22 101845.png]]

# Task Given by RamSir

Take Webtabel !
- print the data in the Excel - tabel formate
- inverted tabel formate
- Copy the tabel one sheet and print/write in another sheet










## Task OF Ramsir from diff Site

**Write WebTable values into Excel Sheet in Selenium with Apache POI API

![[Screenshot 2023-04-22 181540.png]]

# Output:
![[Screenshot 2023-04-22 181716.png]]

## Writing the Code Excel write for copeing values to Excel
![[Screenshot 2023-04-22 182355.png]]


## Inside For loop![[Screenshot 2023-04-22 182619.png]]

![[Screenshot 2023-04-22 182745.png]]

## Output In Eclipse Console:

![[Screenshot 2023-04-22 182855.png]]

## Output in Excel Sheet:

![[Screenshot 2023-04-22 182951.png]]










