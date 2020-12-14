
package com;

public class day2
{
	public static void main(String []args)
	{
		day2 obj=new day2();
		obj.insert(5);
		obj.insert(6);
		obj.insert(7);
		obj.insert(8);
		obj.insert(9);
		obj.delete();
		obj.delete();
		obj.delete();
		obj.insert(1);
		obj.insert(2);
		obj.insert(3);
		obj.insert(4);
		obj.display();
	}
	 int size=6;
	 int[] arr=new int[size];
	 int rear=-1;
	 int front=-1;
	

	void insert(int ele)
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
	 void delete()
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
	 void display()
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
