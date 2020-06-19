# hello-world
This is my first Calculator

import java.util.Scanner;

class Calculator
{
	Scanner myObj = new Scanner(System.in);

	public static void main(String[] args) {
	System.out.println("Welcome to My Calculator");
		new Calculator();
	}
	Integer penjumlahan(Integer a, Integer b) {
		return (a + b);
	}
	Integer pengurangan(Integer a, Integer b) {
		return (a - b);
	}
	Integer pengkalian(Integer a, Integer b) {
		return (a * b);
	}
	Integer pembagian(Integer a, Integer b) {
		return (a / b);
	}
	public Calculator(){
		System.out.print("Input A: ");
		Integer a = myObj.nextInt();
		System.out.println("[1] +");
		System.out.println("[2] -");
		System.out.println("[3] *");
		System.out.println("[4] /");
		System.out.print("Select Operator: ");
		Integer operator = myObj.nextInt();
		while(operator > 4 || operator <= 0){
			System.out.print("Operator Salah Masukan Lagi!\n");
			System.out.print("Select Operator: ");
			operator = myObj.nextInt();
		}
		System.out.print("Input B: ");
		Integer b = myObj.nextInt();
		System.out.print("Result: ");
		String result = myObj.nextLine();
		if (operator == 1) {
			System.out.println(penjumlahan(a,b));
		}
		else if (operator == 2) {
			System.out.println(pengurangan(a,b));
		}
		else if (operator == 3) {
			System.out.println(pengkalian(a,b));
		}
		else if (operator == 4) {
			System.out.println(pembagian(a,b));
		}
	}
}
