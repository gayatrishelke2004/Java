1....
public class JavaExample
{
  public static void main(String args[])
  {
    int num;
   System.out.print("Enter an Integer number: ");
//The input provided by user is stored in num
    Scanner input = new Scanner(System.in);
    num = input.nextInt();

    // If number is divisible by 2 then it's an even number
    //else it is an odd number
    if ( num % 2 == 0 )
      System.out.println(num+" is an even number.");
    else
      System.out.println(num+" is an odd number.");

  }
}



2....

import java.util.Scanner;
public class JavaExample 
{
public static void main(String[] args) 
{
 int num, num1 = 0, num2 = 1;
         	System.out.print("Enter an Integer number: ");
                //The input provided by user is stored in num
                Scanner input = new Scanner(System.in);
	num = input.nextInt();
System.out.print("Fibonacci Series of "+num+" numbers:");
 for (int i = 1; i <= num; ++i)
        {
            System.out.print(num1+" ");
 /* On each iteration, we are assigning second number
             * to the first number and assigning the sum of last two
             * numbers to the second number
             */
            int sumOfPrevTwo = num1 + num2;
            num1 = num2;
            num2 = sumOfPrevTwo;
        }
    }
}



3...
import java.util.Scanner;
class Main {
  public static void main(String[] args) {
     char operator;
    Double number1, number2, result;
    // create an object of Scanner class
    Scanner input = new Scanner(System.in);
  // ask users to enter operator
    System.out.println("Choose an operator: +, -, *, or /");
    operator = input.next().charAt(0);
   // ask users to enter numbers
    System.out.println("Enter first number");
    number1 = input.nextDouble();
    System.out.println("Enter second number");
    number2 = input.nextDouble();
    switch (operator) {
    // performs addition between numbers
      case '+':
        result = number1 + number2;
        System.out.println(number1 + " + " + number2 + " = " + result);
        break;

      // performs subtraction between numbers
      case '-':
        result = number1 - number2;
        System.out.println(number1 + " - " + number2 + " = " + result);
        break;
  // performs multiplication between numbers
      case '*':
        result = number1 * number2;
        System.out.println(number1 + " * " + number2 + " = " + result);
        break;
 // performs division between numbers
      case '/':
        result = number1 / number2;
        System.out.println(number1 + " / " + number2 + " = " + result);
        break;
  default:
        System.out.println("Invalid operator!");
        break;
    }
  input.close();
  }
}


4...
import java.applet.Applet;
import java.awt.Graphics;
public class Hello extends Applet
{
public void paint(Graphics g)
{
g.drawString("Hello world",50,30);
}
}

5..
class Calculation
 {
   int z;
      public void addition(int x, int y)
 {
      z = x + y;
      System.out.println("The sum of the given numbers:"+z);
   }
      public void Subtraction(int x, int y)
 {
      z = x - y;
      System.out.println("The difference between the given numbers:"+z);
   }
}
public class My_Calculation extends Calculation {
   public void multiplication(int x, int y)
 {
      z = x * y;
      System.out.println("The product of the given numbers:"+z);
   }
   public static void main(String args[]) 
{
      int a = 20, b = 10;
      My_Calculation demo = new My_Calculation();
      demo.addition(a, b);
      demo.Subtraction(a, b);
      demo.multiplication(a, b);
   }
}



6...
import javax.swing.*;
import java.awt.*;
import javax.swing.event.*;
import java.awt.event.*;
class MouseEventPerformer extends JFrame implements MouseListener
{
    JLabel l1;
    public MouseEventPerformer()
    {
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setSize(300,300);
        setLayout(new FlowLayout(FlowLayout.CENTER));
        l1 = new JLabel();
        Font f = new Font("Verdana", Font.BOLD, 20);
        l1.setFont(f);
        l1.setForeground(Color.BLUE);
        add(l1);
        addMouseListener(this);
        setVisible(true);
    }
    public void mouseExited(MouseEvent m)
    {
        l1.setText("Mouse Exited");
    }
    public void mouseEntered(MouseEvent m)
    {
        l1.setText("Mouse Entered");
    }
    public void mouseReleased(MouseEvent m)
    {
        l1.setText("Mouse Released");
    }
    public void mousePressed(MouseEvent m)
    {
        l1.setText("Mouse Pressed");
    }
    public void mouseClicked(MouseEvent m)
    {
        l1.setText("Mouse Clicked");
    }
    public static void main(String[] args) {
        MouseEventPerformer mep = new MouseEventPerformer();
    }
}



7...
class MultithreadingDemo extends Thread {
    public void run()
    {
        try {
            // Displaying the thread that is running
            System.out.println(
                "Thread " + Thread.currentThread().getId()
                + " is running");
        }
        catch (Exception e) {
            // Throwing an exception
            System.out.println("Exception is caught");
        }
    }
}
 
// Main Class
public class Multithread {
    public static void main(String[] args)
    {
        int n = 8; // Number of threads
        for (int i = 0; i < n; i++) {
            MultithreadingDemo object
                = new MultithreadingDemo();
            object.start();
        }
    }
}


8..
import java.util.*;

class StringTokenizerDemo {
	public static void main(String args[]) {
		int n;
		int sum = 0;
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter integers with one space gap:");
		String s = sc.nextLine();
		StringTokenizer st = new StringTokenizer(s, " ");
		while (st.hasMoreTokens()) {
			String temp = st.nextToken();
			n = Integer.parseInt(temp);
			System.out.println(n);
			sum = sum + n;
		}
		System.out.println("sum of the integers is: " + sum);
		sc.close();
	}
}
