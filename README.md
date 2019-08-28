

import java.util.Scanner;

class Main{
    
    private double limit;
    private int number;
    private double balance;
    double amount;
    static final double Max_limit=20000;
    public Main(int number)
    {
        this.number=number;
    }
    protected void setlimit(int limit)
    {
        if(limit<=Max_limit)
        {
        this.limit=limit;
        }
        else 
        {
            System.out.println("limit error");
        }
        
        
    }
    protected boolean purchase()
    {
        	Scanner cs=new Scanner(System.in);
        System.out.println("enter the balance ");
        balance=cs.nextInt();
         System.out.println(balance);
         Scanner sc=new Scanner(System.in);
        System.out.println("enter the amount to purchase ");
        amount=sc.nextInt();
       
        if(balance-amount<=0)
        {
            System.out.println("balance is less");
             return false;
        }
       
        balance=balance-amount;
            System.out.println("transaction successful"+balance);
             return true;
        
       
    }
    public boolean creditsettle(){
        Scanner cs1=new Scanner(System.in);
        System.out.println("enter the amount to deposit ");
        amount=cs1.nextInt();
         
        	
        if(amount<0)
        {
            System.out.println("error");
            return false;
        }
        balance =balance+amount;
        System.out.println(balance);
        return true;
        
        
        
        
        
        
    }
    

	public static void main (String[] args) {
		Main i=new Main(98765454);
		i.setlimit(20000);
		i.purchase();
	
		
	
		i.creditsettle();
		
	}
}
