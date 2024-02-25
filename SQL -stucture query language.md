Topics Covered in Sql is **index 
1. Instalation
2. Basic Query
3. Order by
4. relational operator
5. Group by function    (most question  asked)
6. Analytical  function    (most question asked)
7. Create tabel
8. Joint 
9. Types of Joint
10. JDBC (Java Data base Connection)


![[Pasted image 20230403160841.png]]


### Basic Query   (to take data from table) and Order By(Ascending and descending)
![[Screenshot 2023-04-03 171213.png]]


****basic query
![[Screenshot 2023-04-03 170746.png]]


***Order By(Ascending and desending)  
![[Screenshot 2023-04-03 172235.png]]

### Relation Operator

![[Screenshot 2023-04-03 172730.png]]

#### (Less and greater ,AND,OR ,between,unique,null)

![[Screenshot 2023-04-03 180031.png]]


### Practiced in dashBoard

- it dosent see case sensentive means(captial letter or small letter)
- to excute particular query, we have to select query highlighted in blue in sql commands promt and select **run button.

![[Screenshot 2023-04-03 203415.png]]
===>54:30  till vedio seen




![[Pasted image 20230403212554.png]]


## as  
is rename query!
if u give as empty also ,it will rename.
![[Screenshot 2023-04-03 205822.png]]


## '  '  litral string
String value is single quotes
eg: 'deva'


## | |  concat

![[Screenshot 2023-04-03 210827.png]]


## like (letter start with 's' or last ' i ' and _UnderScore postion second letter _)
![[Screenshot 2023-04-03 212840.png]]


## dual

- is user create tabel
- to perform arthematic operation.

![[Pasted image 20230403213353.png]]

## in
in is a cluaes
- it used to compare more than  one data .

 **query
![[Screenshot 2023-04-03 214300.png]]

**Query in Console 
![[Screenshot 2023-04-03 214224.png]]



# Most important topic interview point view Ram sir told..
## Group by Function & Analytical function

![[Screenshot 2023-04-03 222316.png]]

### Group by coloum
![[Screenshot 2023-04-03 222900.png]]

#### interview Question is that ,how u take value from group by coloum and non group by coloum?

**query

![[Screenshot 2023-04-03 223717.png]]

![[Screenshot 2023-04-03 223348.png]]


### To give condition , 'having' -->is (claues )
![[Screenshot 2023-04-03 224544 1.png]]





# Analytical  function

![[Screenshot 2023-04-03 225857.png]]

## rank()

![[Screenshot 2023-04-03 230611.png]]

## dense rank
- it doest not skips
![[Screenshot 2023-04-03 230822.png]]



#### Question :Select the 5th maxi salary?
most important question always askes !    ram sir told  .....
![[Screenshot 2023-04-03 231713.png]]
![[Screenshot 2023-04-03 232539.png]]




# 2nd vedio
## Create Tabel

![[Screenshot 2023-04-03 234722.png]]


##### Different between char and vchar

![[Screenshot 2023-04-03 234248.png]]

vedio stoped 57:32 ...continue


### Constraints
Enforce rule on tabel
- primarykey
- unique
- Not null
- check
- Foreign key

### Primary key
- [Entity] integrity -->{it represet Tabel}
- it ignore null value and duplicate values
- only one primary key accept in tabel
- it automatically generate unique index
- it is given for only one column
### Unique
- [Entity] intergrity -->{it represet Tabel}
- it ignore Duplicate values and accept one null values
 - it automatically generate unique box

### Not null:
- it is a domain integrity [represent coloum]
- it ignore null values

### Check {Condition given tabel simliar to 'Where' and 'having' condition}
- it is a domain integrity
- it should satisfy the condition

### Foregin Key
- it is a referntial intergrity-->{refer one tabel to another tabel coloum/entire tabel}
- it refers the primary key or unique constraints coloumn of an another tabel
- it accept null values and Duplicates

### Foreign Key

![[Screenshot 2023-04-06 084613.png]]

# To Create tabel

Step1: mention the tabel name
Step2: Mention the coloum name
Step3: Mention Data type
Step4: Mention the constraints

Eg:
create tabel name
coloumnName data type constraints
or 
constraint costraintname constrainttype(column name)
![[Screenshot 2023-04-06 085952.png]]

### Tabel CREATED in console

![[Pasted image 20230406091840.png]]





# Joint

![[Screenshot 2023-04-06 092937.png]]

#### Frist tabel already created Above
###### Tabel-2 created 
![[Screenshot 2023-04-06 094138.png]]


## Task:
![[Screenshot 2023-04-06 094453.png]]
![[Pasted image 20230406101446.png]]

### Insert vlaue in tabel
![[Screenshot 2023-04-06 100644.png]]

### insert value 2nd tabel
![[Screenshot 2023-04-06 100903.png]] 

### Query For Joint Two Tabel

![[Screenshot 2023-04-06 113907.png]]



![[Screenshot 2023-04-06 103251.png]]

## 5 Types of joint
![[Screenshot 2023-04-06 105146 1.png]]



# 3rd Vedio 
## joint Types Query and JDBC Connection
	
![[Screenshot 2023-04-06 161310.png]]

#### Most important topic for interview Question----> Ram Sir Told
- joint
- analytical
- group by function


### Last Topic SQ is JDBC Connection.

###### JAVA DATA BASE CONNECTION(JDBC Connection)

Step1: Load the driver
Step2: Connect to the database
Step3: Write a Sql Query
Step4:Prepare the Statement
Step5:execute a query
Step6: Iterate the Results
Step7:Close The db connection

##### JAR File
ojdbc14.jar
oracle jdbc 14.jar

![[Screenshot 2023-04-06 170902.png]]

### JDBC code

		public class JdbcCode{
		public static void main (String[]args){
				// Load driver
				Class.forName("jdbc.oracle.driver.OracleDriver");
		//connect database
	Connection connection=DriverManager.getConnection("
		jdbc:oracle:thin:@localhost:1521:xe","hr","Sathish$123");
		// enter String
		String query="select * from employees";
		//prepare statement
		PreparedStatement prepareStatement=connection.prepareStatement(query);
		//executeQuery
		ResultSet executeQuery=prepareStatement.executeQuery();
		while(executeQuery.next()){
		String string=executeQuery.getString("last_name");
		System.out.println(string);
		}


		}
		
		
		}







