package com.curd;

import java.sql.SQLException;
import java.util.Scanner;

public class CurdMain {
	private static Scanner sc;

	public static void main(String ag[])
	{
	int choice;
	{
	do
	{	System.out.println("-------------Enter Choice--------");
		System.out.println("1. Insert");
		System.out.println("2. Update");
		System.out.println("3. Delete");
		System.out.println("4. View");
		sc = new Scanner(System.in);
		choice=sc.nextInt();
		ImplCurd im;
		switch(choice)
		{
		case 1:im=new ImplCurd();
		try {
			im.insert();
		} catch (ClassNotFoundException | SQLException e) {
			
			e.printStackTrace();
		}
		break;
		case 2:im=new ImplCurd();
		try {
			im.update();
		} catch (ClassNotFoundException | SQLException e) {
			
			e.printStackTrace();
		}
		break;
		case 3:im=new ImplCurd();
		try {
			im.delete();
		} catch (ClassNotFoundException | SQLException e) {
			
			e.printStackTrace();
		}
		break;
		case 4:
				im=new ImplCurd();
			try {
				im.view();
			} catch (ClassNotFoundException | SQLException e) {
				
				e.printStackTrace();
			}
		break;
		}
		
	}while(choice!=5);
	System.out.println("You are now out of Program............");
	}
	}
}
