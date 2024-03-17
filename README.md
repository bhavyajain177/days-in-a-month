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

linked list

import java.util.*;
import java.io.*;
class Node 
{
    int data;
    Node next;
    Node(int data)
    {
        this.data=data;
        this.next=null;
    }
}
class GFG {
    static Node head=null;
    static void insert_at_begin(int data)
    {
        Node new_node=new Node(data);
        if(head==null)
        {
            head=new_node;
            return;
        }
        new_node.next=head;
        head=new_node;
    }
    static void printlist()
    {
        Node temp=head;
        while(temp!=null)
        {
            System.out.print(temp.data+" ");
            temp=temp.next;
        }
    }
    public static void main (String[] args) {
            Scanner s=new Scanner(System.in);
            int n=s.nextInt();
            for(int i=0; i<n; i++)
                insert_at_begin(s.nextInt());
            printlist();
    }
}

mycode
import java.util.*;
import java.io.*;


class Node{
    int data;
    Node next;
    
    Node(int d){
        data=d;
        next= null;
    }
}
class Main{
    static Node head=null;
    static void insertbegin(int n){
        Node new_node=new Node(n);
        if (head==null){
            head=new_node;
            return;
        }
        new_node.next=head;
        head=new_node;
        
    }
    
    static void printls(){
        Node temp=head;
        while(temp!=null){
            System.out.print(temp.data+" ");
            temp=temp.next;
        }
    }
    public static void main (String[] args) {
            Scanner s=new Scanner(System.in);
            int n=s.nextInt();
            for(int i=0; i<n; i++)
                insertbegin(s.nextInt());
            printls();
    }
}

import java.util.*;
import java.io.*;


class Node{
    int data;
    Node next;
    
    Node(int d){
        data=d;
        next= null;
    }
}
class Main{
    static Node head=null;
    static Node temp=null;
    static void insertlast(int n){
        Node new_node= new Node(n);
        
        if(head==null){
            head=new_node;
            temp=head;
            return; //purpose??
        }
        
        
        if (temp.next==null){
            temp.next=new_node;
            temp=new_node;
        }
    }
    static void insertbetween(Node prev,int n){
        Node new_node= new Node(n);
        if(prev==null){
            System.out.println("prev node cannt be null");
        }
        
        else{
            new_node.next=prev.next;
            prev.next=new_node;
        }
    }
    
    static void printls(){
        Node temp=head;
        while(temp!=null){
            System.out.print(temp.data+" ");
            temp=temp.next;
        }
    }
    public static void main (String[] args) {
            Scanner s=new Scanner(System.in);
            int n=s.nextInt();
            for(int i=0; i<n; i++){
                int a=s.nextInt();
                insertlast(a);
            }
            
            int j=s.nextInt();
            
            Node(j);
            int k=s.nextInt();
            insertbetween(mynode,k);
            printls();
    }
}
