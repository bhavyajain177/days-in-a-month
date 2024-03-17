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

import java.util.*;
import java.util.Scanner;

class Node {
    int data;
    Node next;

    public Node(int data) {
        this.data = data;
        this.next = null;
    }
}

class LinkedList {
    Node head;

    public LinkedList() {
        this.head = null;
    }

    public void insert(int data) {
        Node newNode = new Node(data);
        if (head == null) {
            head = newNode;
        } else {
            Node temp = head;
            while (temp.next != null) {
                temp = temp.next;
            }
            temp.next = newNode;
        }
    }
  	public void mergeSortedLinkedLists(LinkedList list2) {
        if (list2.head == null) {
            return;
        }

        if (this.head == null) {
            this.head = list2.head;
            return;
        }

        Node dummy = new Node(0);
        Node tail = dummy;
        Node temp1 = this.head;
        Node temp2 = list2.head;

        while (temp1 != null && temp2 != null) {
            if (temp1.data < temp2.data) {
                tail.next = temp1;
                temp1 = temp1.next;
            } else {
                tail.next = temp2;
                temp2 = temp2.next;
            }
            tail = tail.next;
        }

        if (temp1 != null) {
            tail.next = temp1;
        }
        if (temp2 != null) {
            tail.next = temp2;
        }

        this.head = dummy.next;
    }

    public void display() {
        Node temp = head;
        while (temp != null) {
            System.out.print(temp.data + "->");
            temp = temp.next;
        }
      	if(temp==null){
          System.out.print("NULL");
        }
        System.out.println();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        LinkedList list1 = new LinkedList();
        LinkedList list2 = new LinkedList();

        
        int n = scanner.nextInt();
        
        for (int i = 0; i < n; i++) {
            list1.insert(scanner.nextInt());
        }

        
        int m = scanner.nextInt();
        
        for (int i = 0; i < m; i++) {
            list2.insert(scanner.nextInt());
        }

        

        list1.mergeSortedLinkedLists(list2);

        
        list1.display();
    }
}


import java.util.*;

class Node{
    
    int data;
    Node next;
    
    Node(int d){
        data=d;
        next=null;
    }
}

class linkedlist{
    
    public Node head;
    
    public linkedlist(){
        head=null;
    }
    
    public void insert(int n){
        Node new_node=new Node(n);
        if(head==null){
            head=new_node;
            
            return;
        }
        
        Node temp=head;
        
        while(temp.next!=null){
            temp=temp.next;
        }
        temp.next=new_node;
        
    }
    
    public void display(){
        Node temp=head;
        while(temp!=null){
            System.out.println(temp.data);
            temp=temp.next;
            
        }
        
        
    }
    
}



public class Main{
    
    
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        
        linkedlist list1=new linkedlist();
        linkedlist list2=new linkedlist();
        
        int n=sc.nextInt();
        for(int i=0;i<n;i++){
            int a=sc.nextInt();
            list1.insert(a);
        }
        
        
        int m=sc.nextInt();
        for(int i=0;i<n;i++){
            int a=sc.nextInt();
            list2.insert(a);
        }
        
        list1.display();
        list2.display();
        
    }
}
