# JavaTest

**code**
public class arrays {
	
	/**
	 * @param args
	 */
	public static void main(String[] args) {
		// TODO Auto-generated method stub
         int[]  a = {1,2,3,4,5};
         int[] l = {1001,1002,1003,1004,1005};
         System.arraycopy(a, 2, l, 2, 3);
         for(int i=0; i<l.length; i++)
        	 System.out.println(i + ": "+ l[i]);
         }
}

**result**
0: 1001
1: 1002
2: 3
3: 4
4: 5

----------------------------------------
import java.util.Scanner;


public class test {

	/**
	 * @param args
	 */
	
	public static void main(String[] args) {
		
		Scanner in = new Scanner(System.in);
		int NMAX = in.nextInt();
		int i, j, k;
		int[][] odds = new int[NMAX][];
		for(i=0; i<NMAX; i++){
			odds[i] = new int[i+1];
		}
		
		for(i=0; i<odds.length; i++){
		for(j=0; j<odds[i].length; j++){
				
				int lottterOdds= 1;
				for(k=1; k<=j; k++)
	                        lottterOdds = lottterOdds*(i-k+1)/k;             
	             odds[i][j] = lottterOdds;			
			}
		}
	    	a
		    for(int[] row : odds){
	    		for(int odd:row)
	    		     System.out.printf("%4d", odd);
	    		System.out.println();
	    	}
	}
}


mport java.text.DateFormatSymbols;
import java.util.*;

public class test {

	/**
	 * @param args
	 */
	public static void main(String[] args) {
		// TODO Auto-generated method stub
	//	Locale.setDefault(Locale.ITALY);
		
          GregorianCalendar d = new GregorianCalendar();
           
          int  today = d.get(Calendar.DAY_OF_MONTH);
          int  month = d.get(Calendar.MONTH);
          
          d.set(Calendar.DAY_OF_MONTH, 1);
          
          int weekday = d.get(Calendar.DAY_OF_WEEK);
          
          int firstDayOfWeek = d.getFirstDayOfWeek();
          int indent = 0;
          while(weekday != firstDayOfWeek)
          {
        	  indent++;
        	  d.add(Calendar.DAY_OF_MONTH, -1);
        	  weekday = d.get(Calendar.DAY_OF_WEEK);
          }
          
          String[]  weekdayNames = new DateFormatSymbols().getShortWeekdays();
          do 
          {
        	  System.out.printf("%4s", weekdayNames[weekday]);
        	  d.add(Calendar.DAY_OF_MONTH, 1);
        	  weekday = d.get(Calendar.DAY_OF_WEEK);
          }
          while(weekday != firstDayOfWeek);  
          System.out.println();
          
          for(int i =1; i<=indent; i++)
        	  System.out.print(" ");
          
          d.set(Calendar.DAY_OF_MONTH, 1);
          do {
        	  int day = d.get(Calendar.DAY_OF_MONTH);
        	  System.out.printf("%3d", day);
			  
        	  if(day == today) System.out.print("*");
        	  else System.out.print(" ");
        	  
        	  d.add( Calendar.DAY_OF_MONTH,1);
        	  weekday = d.get(Calendar.DAY_OF_WEEK);
        	  	
        	  if(weekday == firstDayOfWeek) System.out.println();
		} while (d.get(Calendar.MONTH) == month);
          
         if(weekday != firstDayOfWeek) System.out.println();
	}
}
_______________________________________________________________
GOUZHAO LEI

import java.util.*;
import java.util.jar.Attributes.Name;

import org.omg.CORBA.PRIVATE_MEMBER;
import org.omg.CORBA.PUBLIC_MEMBER;

public class EmployeeTest {

	/**
	 * @param args
	 */
	public static void main(String[] args) {
		// TODO Auto-generated method stub
      Employee[] staff = new Employee[3];
      
      staff[0] = new Employee("zyh1", 10001, 1992, 12, 20);
      staff[1] = new Employee("zyh2", 10002, 1997, 5, 15);
      staff[2] = new Employee("zyh3", 10003, 2005, 7, 4);
      
      for(Employee e: staff){
    	  e.raiseSalary(5);
      }
      
      for(Employee e: staff){
    	  System.out.println("name=" + e.getName() + ",salary=" + e.getSalary() + ", hireDay=" + e.getHireDay() );
      }
    }
}

class Employee
{
    public Employee(String n,  double s,  int year,  int month, int day )
    {
         name = n;
         salary = s;
         GregorianCalendar calendar = new GregorianCalendar(year, month-1, day);
         hireDay = calendar.getTime();
    }
    
        public String getName(){
        	return name;
        }
         public double getSalary(){
        	 return salary;
         }
         public Date getHireDay(){
        	   return hireDay;
         }
         
         public void raiseSalary(double byPercent){	 
        	    double raise = salary * byPercent / 100 ;
        	    salary += raise;
         }
       
    private String name;
    private double salary;
    private Date hireDay;
}
_____________________________________________________________
