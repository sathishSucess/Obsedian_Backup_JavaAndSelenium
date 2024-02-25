	public class Employee{
	private int id;
	private String name;

	public int getId(){
	return.id;
	}
	public void setId(int id){
	this.id=id;
	}
	public String getName(){
	return.name;
	}
	public void setName(){
	this.name=name;
	}



    }
     public class Details{

	public static void main(String[]args){
	List<Employee> li=new ArrayList<>();
    Employee e1=new Employee();
    e1.setId(20);
    e1.setName("Geni");
	Employee e2=new Employee();
		e2.setId(30);
		e2.setName("Fenda");
	
		li.add(e1);
		li.add(e2);
		for(Employee l:li){
		System.out.println(l.getId());
		System.out.println(l.getName());
		}

	  }
    }