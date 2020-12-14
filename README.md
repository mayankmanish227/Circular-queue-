# Circular-queue-
package com;

public class day2
{
	public static void main(String []args)
	{
		day2 obj=new day2();
		insert(5);
		insert(6);
		insert(7);
		insert(8);
		insert(9);
		delete();
		delete();
		delete();
		insert(1);
		insert(2);
		insert(3);
		insert(4);
		display();
	}
	static int size=6;
	static int[] arr=new int[size];
	static int rear=-1;
	static int front=-1;
	

	static void insert(int ele)
	{
		if((front==0 && rear==size-1) || (front==rear+1))
		{
			System.out.println("queue is full");
		}
		else if(front==-1 && rear==-1)
		{
			front=rear=0;
			arr[rear]=ele;	
		}
		else if(rear==size-1)
		{
			rear=0;
			arr[rear]=ele;
		}
		else
		{
			rear++;
			arr[rear]=ele;
		}
	}
	static void delete()
	{
		if(front==-1 && rear==-1)
		{
			System.out.println("queue is empty");
		}
		else if(front==rear)
		{
			
			front=rear=-1;
		}
		else if(front==size-1)
		{
			front=0;
		}
		else
		{
			front++;
		}
	}
	static void display()
	{
		if(front==-1 && rear==-1)
		{
			System.out.println("empty");
		}
		else if(rear>front && rear<=size)
		{
			for(int i=front;i<=rear;i++)
			{
				System.out.println(arr[i]);
			}
			
		}
		else if(front==0 )
		{
			for(int i=front;i<=rear;i++)
			{
				System.out.println(arr[i]);
			}
			
			
		}
		else
		{
			for(int i=front;i<size;i++)
			{
				System.out.println(arr[i]);
			}
			for(int i=0;i<=rear;i++)
			{
				System.out.println(arr[i]);
			}
			
		}
		
	}
}
