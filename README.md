1.	Encapsulation is the bundling of data and methods that operate on the data into a single unit, called a class. It hides the internal state of an object from the outside world and only exposes the necessary functionality through well-defined interfaces. 
Create an Employee class having data members' Name, Eid, and Basic_Salary, to calculate the HRA is 20% of Basic Salary and DA is 25% of Basic salary and MA is 300 rupee. implement the following queries:
  a) Display the name and gross salary of an employee whose name starts With 'n'
  b).Display the Eid and gross salary whose Eid is equal to 107.
  c)  Count the total number of employees whose salary more than 20000/-


import java.util.Scanner;
public class Github1 {
		Scanner sc = new Scanner(System.in);
		int Eid , BS;
		String name;
		int MA = 300;
		double GS,HRA;
		static int count=0;
		void get_data(){
			System.out.println("Enter Employee Id : ");
			Eid = sc.nextInt();
			System.out.println("Enter Name : ");
			name = sc.next();
			System.out.println("Basic Salary : ");
			BS = sc.nextInt();
		}
		void cal(){
			HRA = (BS * 20)/100;
			GS = BS + HRA + MA;
		}
		void Display(){
			if(name.charAt(0) == 'N' )
			{
				System.out.println("Name of Employee whose name start with N : " + name);
			}
			if(Eid == 107)
			{
				System.out.println("Gross Salary of Employee 107 : " + GS);
			}
			if(GS>20000)
			{
				count = count +1;
			}
		}
		
		
		public static void main(String ar[]){
			System.out.println("Anugrah Das 2210997040");
			TwoC ob1 = new TwoC();
			TwoC ob2 = new TwoC();
			TwoC ob3 = new TwoC();
			ob1.get_data();
			ob2.get_data();
			ob3.get_data();
			ob1.cal();
			ob2.cal();
			ob3.cal();
			ob1.Display();
			ob2.Display();
			ob3.Display();
			System.out.println("Employees whose GS is more than 20000 : " + count);
		}
}
