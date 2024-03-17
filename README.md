# days-in-a-month
import java.util.*;

class Main{
    public static void main(String[] args){
        
        int month;
        
        Scanner sc=new Scanner(System.in);
        
        month= sc.nextInt();
        
        switch(month){
            default:
                System.out.println("invalid input");
                break;
            
            case 2:
                System.out.println("28/29");
                break;
                
            case 1:case 3:case 5:case 7:case 8:case 10:case 12:
                System.out.println("31");
                break;
            
            case 4:case 6:case 9:case 11:
                
                System.out.println("30");
                break;
        }
        
        
    }
}

#factorial recursive 
import java.util.*;

class Main{
    
    public static void factorial(int num,int product){
        product=product*num;
        num--;
        if(num>1){
            factorial(num,product);
            
        }
        
        else{
            System.out.println(product);
        }
        
        
    }
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        
        int n=sc.nextInt();
        int prod=1;
        factorial(n,prod);
    }
}

