package com.curd;
import java.sql.*;
import java.util.Scanner;

public class ImplCurd {
	private Scanner sc;
	int id;
	String name;
	void insert()throws SQLException, ClassNotFoundException
	{
		sc = new Scanner(System.in);
		System.out.print("Enter Id=");
		id=sc.nextInt();
		System.out.println("Enter Name=");
		name=sc.next();
		Class.forName("com.mysql.jdbc.Driver");  
		  
		Connection con=DriverManager.getConnection("jdbc:mysql://localhost:3306/Pra","root","P@ssw0rd@123");   
		  
		Statement stmt= con.createStatement();

		stmt.executeUpdate("INSERT INTO Student " + "VALUES ('"+id+"','"+name+"')");
		System.out.println("Sucessfully Inserted..........");
	}
	
	void update()throws SQLException, ClassNotFoundException
	{
		sc = new Scanner(System.in);
		System.out.print("Enter Id to Update=");
		id=sc.nextInt();
		System.out.println("Enter Updated Name=");
		name=sc.next();
		Class.forName("com.mysql.jdbc.Driver");  
		  
		Connection con=DriverManager.getConnection("jdbc:mysql://localhost:3306/Pra","root","P@ssw0rd@123");   
		  
		Statement stmt= con.createStatement();
		String query = "update Student set stName='"+name+"' where stId='"+id+"'";
        int count = stmt.executeUpdate(query);
		System.out.println(count+" Row Sucessfully Updated..........");
	}
	
	void delete()throws SQLException, ClassNotFoundException
	{
		sc = new Scanner(System.in);
		System.out.print("Enter Id to Delete=");
		id=sc.nextInt();
		Class.forName("com.mysql.jdbc.Driver");  
		  
		Connection con=DriverManager.getConnection("jdbc:mysql://localhost:3306/Pra","root","P@ssw0rd@123");   
		  
		Statement stmt= con.createStatement();
		String query = "delete from Student where stId='"+id+"'";
        int count = stmt.executeUpdate(query);
		System.out.println(count+" Row Deleted Updated..........");
	}
	
	void view() throws SQLException, ClassNotFoundException
	{
		try{  
			Class.forName("com.mysql.jdbc.Driver");  
			  
			Connection con=DriverManager.getConnection("jdbc:mysql://localhost:3306/Pra","root","P@ssw0rd@123");   
			  
			Statement stmt= con.createStatement();  
			  
			ResultSet rs=stmt.executeQuery("select * from Student"); 
			  
			while(rs.next())  
			System.out.println(rs.getInt(1)+"  "+rs.getString(2));  
			  
			con.close();  
			  
			}catch(Exception e){ System.out.println(e);}  
	}
	
	}
