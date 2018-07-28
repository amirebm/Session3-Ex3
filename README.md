# Session3-Ex3


// ب ن ک دو عدد از ورودی گرفته و ب م م آن را حساب کند
package com.personal.ex3;

import java.util.Scanner;

import com.sun.xml.internal.messaging.saaj.packaging.mime.internet.BMMimeMultipart;

public class ex3 {

public static void main(String[] args) {
		
		Scanner sc= new Scanner(System.in);
		System.out.println("Enter two Number");
		int num1= sc.nextInt();
		int num2=sc.nextInt();
		System.out.println(bmmFinder(num1, num2) + " is a BMM  "+ num1 + " and "+ num2 );	
	
}
	static int bmmFinder(int num1,int num2) {
	
		int min=0;
		int max=0;
		int remain=1;
		if (num1<num2) {
			min=num1;
			max=num2;}
		else {
			min=num2;
			max=num1;
		}
		do {
			
			remain=max % min;
			max=remain;
			min=max;
			
		} while(remain==0);	
		return remain;
	}

}
