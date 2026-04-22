## INDEX

[PROGRAM-1 WRITE A PROGRAM FOR ADDITION, SUBTRACTION, MULTIPLICATION AND DIVISION USING CLASSES AND OBJECTS](#assi-1)

[PROGRAM-2 WRITE A PROGRAM FOR THE ADDITION OF 2 DISTANCE WHERE EACH DISTANCE IS GIVEN IN METER, CENTIMETER AND MILLIMETER](#assi-2)

[PROGRAM-3 WRITE A PROGRAM FOR THE ADDITION OF TWO TIMES WHERE EACH TIME IS GIVEN IN HOURS, MINUTES AND SECONDS USING CLASSES AND OBJECTS](#assi-3)

[PROGRAM-4 WRITE A PROGRAM FOR THE ADDITION OF TWO DISTANCES WHERE EACH DISTANCE IS GIVEN IN METER AND CENTIMETER](#assi-4)

[PROGRAM-5 WRITE A PROGRAM USING OBJECTS AND CLASSES TO DO REVERSE OF 1-D ARRAY](#assi-5)

[PROGRAM-6 WRITE A CLASS FOR IMPORTANT OPERATION OF MATRIX(3X3): TRANSPOSE, SUM, MULTUPLY, SUM OF ROWS, SUM OF COLUMNS AND SUM OF DIAGONALS](#assi-6)

[PROGRAM-7 COLLECT THE CODE OF C LANGUAGE OF ANY 5 OPERATION AND CONVERT THE LOGIC INTO JAVA OOPS FASHION](#assi-7)

[PROGRAM-8 DEMONSTRATE ALL THREE TYPES OF INHERITANCE WITH MINIMAL SIZE OF CODE](#assi-8)

[PROGRAM-9. Write a program using three classes to print 1-100 ,1-100,1-100 with and without thread and analyse the output and repeat the same program using runnable interface.](#assi-9)

[PROGRAM-10. Using the concept of multithreading the output of all three threads must be synchronised (use join method).](#assi-10)

[PROGRAM-11.  Addition of 2 numbers using swing.](#assi-11)

[PROGRAM-12.  Make a registration form with 10 elements and send the data into database (use jdbc connectivity)](#assi-12)

[PROGRAM-13.  Make one calculator in swing.](#assi-13)

[PROGRAM-14.  Matrix Addition using swing class.](#assi-14)

[PROGRAM-15.  Create one jframe apply 10 buttons on that after clicking on each button a new structure is created.(Circle, oval rectangle, etc ....)](#assi-15)

[PROGRAM-16.  Just using mouse Event create a frame like paint brush with selection of colour and width .](#assi-16)

[PROGRAM-17.  Create a package of any 5 classes of your choice and import it.](#assi-17)

[PROGRAM-18.  Create one package and sub package  import and test it .](#assi-18)

[PROGRAM-19.  Create one small array of size 5 apply array out of bounds exception using try catch give a proper message in catch and demonstrate the exception exactly in the same fashion demonstrate arithmetic exception .](#assi-19)

[PROGRAM-20.  To test the range of age of one student.write a program using user defined exception.](#assi-20)

[PROGRAM-21.  File Handling Programs (given in the PPT)](#assi-21)

[PROGRAM-22.  Inheritance Programs, using interface and abstract classes.](#assi-22)

## assi-1
```import java.util.Scanner;
class Calculator {
    int add(int a, int b)
    {
        return a + b;
    }
    int subtract(int a, int b)
    {
        return a - b;
    }
    int multiply(int a, int b)
    {
        return a * b;
    }
    double divide(int a, int b)
    {
        return (double) a / b;
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Calculator obj = new Calculator();
        int a, b;
        System.out.print("Enter first number: ");
        a = sc.nextInt();
        System.out.print("Enter second number: ");
        b = sc.nextInt();
        System.out.println("Addition = " + obj.add(a, b));
        System.out.println("Subtraction = " + obj.subtract(a, b));
        System.out.println("Multiplication = " + obj.multiply(a, b));
        System.out.println("Division = " + obj.divide(a, b));
    }
}
```
<img width="885" height="262" alt="image" src="https://github.com/user-attachments/assets/d276f316-a796-4e0c-a7c4-d84b2b32d9e3" />


## assi-2
```import java.util.Scanner;
class Distance {
    int m, cm, mm;
    void add(Distance d1, Distance d2) {
        mm = d1.mm + d2.mm;
        cm = d1.cm + d2.cm + mm / 10;
        mm = mm % 10;
        m = d1.m + d2.m + cm / 100;
        cm = cm % 100;
    }
    void display() {
        System.out.println("Total Distance = " + m + " m " + cm + " cm " + mm + " mm");
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Distance d1 = new Distance();
        Distance d2 = new Distance();
        Distance d3 = new Distance();
        System.out.print("Enter first distance (m,cm,mm): ");
        d1.m = sc.nextInt();
        d1.cm = sc.nextInt();
        d1.mm = sc.nextInt();
        System.out.print("Enter second distance (m,cm,mm): ");
        d2.m = sc.nextInt();
        d2.cm = sc.nextInt();
        d2.mm = sc.nextInt();
        d3.add(d1, d2);
        d3.display();
    }
}
```
<img width="738" height="147" alt="image" src="https://github.com/user-attachments/assets/c1e9c1a2-a02b-4521-93da-702353028657" />

## assi-3
```import java.util.Scanner;
class Time {
    int h, m, s;
    void add(Time t1, Time t2) {
        s = t1.s + t2.s;
        m = t1.m + t2.m + s / 60;
        s = s % 60;
        h = t1.h + t2.h + m / 60;
        m = m % 60;
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Time t1 = new Time();
        Time t2 = new Time();
        Time result = new Time();
        System.out.print("Enter first time (h m s): ");
        t1.h = sc.nextInt();
        t1.m = sc.nextInt();
        t1.s = sc.nextInt();
        System.out.print("Enter second time (h m s): ");
        t2.h = sc.nextInt();
        t2.m = sc.nextInt();
        t2.s = sc.nextInt();
        result.add(t1, t2);
        System.out.println("Total Time = " + result.h + " hr " + result.m + " min " + result.s          + " sec");
    }
}
```
<img width="718" height="146" alt="image" src="https://github.com/user-attachments/assets/50a400c2-eb13-48c2-87bb-9ae37e786584" />

## assi-4
```import java.util.Scanner;
class Distance {
    int m, cm;

    void add(Distance d1, Distance d2) {
        cm = d1.cm + d2.cm;
        m = d1.m + d2.m + cm / 100;
        cm = cm % 100;
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Distance d1 = new Distance();
        Distance d2 = new Distance();
        Distance result = new Distance();
        System.out.print("Enter first distance (m cm): ");
        d1.m = sc.nextInt();
        d1.cm = sc.nextInt();
        System.out.print("Enter second distance (m cm): ");
        d2.m = sc.nextInt();
        d2.cm = sc.nextInt();
        result.add(d1, d2);
        System.out.println("Total Distance = " + result.m + " m " + result.cm + " cm");
    }
}
```
<img width="728" height="147" alt="image" src="https://github.com/user-attachments/assets/ae2454a1-2bcb-49bc-898a-d93781b04848" />

## assi-5
```import java.util.Scanner;
class ArrayReverse {
    void reverse(int arr[], int n) {
        for(int i = n-1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayReverse obj = new ArrayReverse();
        System.out.print("Enter size of array: ");
        int n = sc.nextInt();
        int arr[] = new int[n];
        System.out.println("Enter array elements:");
        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println("Reversed array:");
        obj.reverse(arr, n);
    }
}
```
<img width="965" height="445" alt="image" src="https://github.com/user-attachments/assets/8cd00784-c7a4-49fd-92f8-7c90cb6f2eef" />

## assi-6
```import java.util.Scanner;
class Matrix {
    int a[][] = new int[3][3];
    // Input method
    void input() {
        Scanner sc = new Scanner(System.in);
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                a[i][j] = sc.nextInt();
            }
        }
    }
    // Output method
    void display() {
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                System.out.print(a[i][j] + " ");
            }
            System.out.println();
        }
    }
    // Transpose
    void transpose() {
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                System.out.print(a[j][i] + " ");
            }
            System.out.println();
        }
    }
    // Sum of matrices
    void sum(Matrix b) {
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                System.out.print((a[i][j] + b.a[i][j]) + " ");
            }
            System.out.println();
        }
    }
    // Multiplication
    void multiply(Matrix b) {
        int c[][] = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                for(int k=0;k<3;k++){
                    c[i][j] += a[i][k] * b.a[k][j];
                }
                System.out.print(c[i][j] + " ");
            }
            System.out.println();
        }
    }
    // Sum of rows
    void rowSum() {
        for(int i=0;i<3;i++){
            int sum = 0;
            for(int j=0;j<3;j++){
                sum += a[i][j];
            }
            System.out.println("Row " + (i+1) + " Sum = " + sum);
        }
    }
    // Sum of columns
    void columnSum() {
        for(int j=0;j<3;j++){
            int sum = 0;
            for(int i=0;i<3;i++){
                sum += a[i][j];
            }
            System.out.println("Column " + (j+1) + " Sum = " + sum);
        }
    }
    // Sum of diagonals
    void diagonalSum() {
        int d1=0, d2=0;
        for(int i=0;i<3;i++)
        {
            d1 += a[i][i];
            d2 += a[i][2-i];
        }
        System.out.println("Main Diagonal Sum = " + d1);
        System.out.println("Other Diagonal Sum = " + d2);
    }
}
public class Main {
    public static void main(String[] args) {
        Matrix m1 = new Matrix();
        Matrix m2 = new Matrix();
        System.out.println("Enter First Matrix (3x3):");
        m1.input();
        System.out.println("Enter Second Matrix (3x3):");
        m2.input();
        System.out.println("Matrix 1:");
        m1.display();
        System.out.println("Transpose:");
        m1.transpose();
        System.out.println("Sum of Matrices:");
        m1.sum(m2);
        System.out.println("Multiplication:");
        m1.multiply(m2);
        System.out.println("Row Sum:");
        m1.rowSum();
        System.out.println("Column Sum:");
        m1.columnSum();
        System.out.println("Diagonal Sum:");
        m1.diagonalSum();
    }
}
```
<img width="619" height="790" alt="image" src="https://github.com/user-attachments/assets/929fcd21-14e2-44e8-8e75-6828beaf5fb3" />

## assi-7
```import java.util.Scanner;
class Ops {
    void factorial(int n){
        int f=1;
        for(int i=1;i<=n;i++) f*=i;
        System.out.println("Factorial = "+f);
    }
    void fibonacci(int n){
        int a=0,b=1,c;
        System.out.print("Fibonacci: ");
        for(int i=1;i<=n;i++){
            System.out.print(a+" ");
            c=a+b; a=b; b=c;
        }
        System.out.println();
    }
    void palindrome(int n){
        int t=n,r,rev=0;
        while(n>0){
            r=n%10;
            rev=rev*10+r;
            n/=10;
        }
        if(t==rev) System.out.println("Palindrome");
        else System.out.println("Not Palindrome");
    }
    void armstrong(int n){
        int t=n,r,sum=0;
        while(n>0){
            r=n%10;
            sum+=r*r*r;
            n/=10;
        }
        if(sum==t) System.out.println("Armstrong");
        else System.out.println("Not Armstrong");
    }
    void pattern(int n){
        for(int i=1;i<=n;i++){
            for(int j=1;j<=i;j++)
                System.out.print("*");
            System.out.println();
        }
    }
}
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        Ops o1=new Ops();
        int n;
        System.out.print("Enter number for factorial: ");
        n=sc.nextInt();
        o1.factorial(n);
        System.out.print("Enter terms for fibonacci: ");
        n=sc.nextInt();
        o1.fibonacci(n);
        System.out.print("Enter number for palindrome check: ");
        n=sc.nextInt();
        o1.palindrome(n);
        System.out.print("Enter number for armstrong check: ");
        n=sc.nextInt();
        o1.armstrong(n);
        System.out.print("Enter rows for pattern: ");
        n=sc.nextInt();
        o1.pattern(n);
    }
}
```
<img width="754" height="394" alt="image" src="https://github.com/user-attachments/assets/218927bc-40f2-40f2-9e20-807547526632" />

## assi-8
```class A {
    void showA() {
        System.out.println("Class A");
    }
}
// Single Inheritance
class B extends A {
    void showB() {
        System.out.println("Class B (Single Inheritance)");
    }
}
// Multiple Inheritance
class C extends B {
    void showC() {
        System.out.println("Class C (Acts like Multiple/Multilevel)");
    }
}
// Hierarchical Inheritance
class D extends A {
    void showD() {
        System.out.println("Class D (Hierarchical Inheritance)");
    }
}
public class Main {
    public static void main(String[] args) {
        // Single
        B obj1 = new B();
        obj1.showA();
        obj1.showB();
        // Multilevel
        C obj2 = new C();
        obj2.showA();
        obj2.showB();
        obj2.showC();
        // Hierarchical
        D obj3 = new D();
        obj3.showA();
        obj3.showD();
    }
}
```
<img width="790" height="260" alt="image" src="https://github.com/user-attachments/assets/b9c02b38-a32f-495e-98ee-e6f7650bbdf6" />

## assi-9

class WithoutThread {
    void printNumbers(String name) {
        for (int i = 1; i <= 100; i++) {
            System.out.println(name + ": " + i);
        }
    }
}

// Using Thread class
class MyThread extends Thread {
    String name;

    MyThread(String name) {
        this.name = name;
    }

    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println(name + ": " + i);
        }
    }
}

// Using Runnable interface
class MyRunnable implements Runnable {
    String name;

    MyRunnable(String name) {
        this.name = name;
    }

    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println(name + ": " + i);
        }
    }
}

public class Main {
    public static void main(String[] args) {

        // WITHOUT THREAD
        System.out.println("=== WITHOUT THREAD ===");
        WithoutThread obj = new WithoutThread();
        obj.printNumbers("A");
        obj.printNumbers("B");
        obj.printNumbers("C");

        // USING THREAD CLASS
        System.out.println("\n=== USING THREAD CLASS ===");
        MyThread t1 = new MyThread("T1");
        MyThread t2 = new MyThread("T2");
        MyThread t3 = new MyThread("T3");

        t1.start();
        t2.start();
        t3.start();

        try {
            t1.join();
            t2.join();
            t3.join();
        } catch (Exception e) {
            System.out.println(e);
        }

        // USING RUNNABLE INTERFACE
        System.out.println("\n=== USING RUNNABLE ===");
        Thread r1 = new Thread(new MyRunnable("R1"));
        Thread r2 = new Thread(new MyRunnable("R2"));
        Thread r3 = new Thread(new MyRunnable("R3"));

        r1.start();
        r2.start();
        r3.start();
    }
}
<img width="663" height="221" alt="image" src="https://github.com/user-attachments/assets/be70717a-4117-4cb2-8cca-5794dba09bd8" />
<img width="371" height="218" alt="image" src="https://github.com/user-attachments/assets/f00c3cba-bbc6-475e-8e79-807849d13746" />
<img width="438" height="197" alt="image" src="https://github.com/user-attachments/assets/6dc547ca-67b0-4616-bfc5-e75421b927d3" />

## assi-10
class MyThread extends Thread {
    String name;

    MyThread(String name) {
        this.name = name;
    }

    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println(name + ": " + i);
        }
    }
}

public class Main {
    public static void main(String[] args) {

        MyThread t1 = new MyThread("T1");
        MyThread t2 = new MyThread("T2");
        MyThread t3 = new MyThread("T3");

        try {
            t1.start();
            t1.join();   // wait for t1

            t2.start();
            t2.join();   // wait for t2

            t3.start();
            t3.join();   // wait for t3

        } catch (Exception e) {
            System.out.println(e);
        }

        System.out.println("Execution completed in order.");
    }
}

<img width="590" height="217" alt="image" src="https://github.com/user-attachments/assets/85aa9036-6300-4fce-b033-6402a12db537" />

## assi-11
import javax.swing.*;
import java.awt.event.*;

public class Main {
    public static void main(String[] args) {

        // Create frame
        JFrame f = new JFrame("Addition");
        f.setSize(300, 200);
        f.setLayout(null);

        // Labels
        JLabel l1 = new JLabel("Number 1:");
        l1.setBounds(20, 20, 100, 20);
        f.add(l1);

        JLabel l2 = new JLabel("Number 2:");
        l2.setBounds(20, 50, 100, 20);
        f.add(l2);

        JLabel result = new JLabel("Result:");
        result.setBounds(20, 120, 200, 20);
        f.add(result);

        // Text fields
        JTextField t1 = new JTextField();
        t1.setBounds(120, 20, 120, 20);
        f.add(t1);

        JTextField t2 = new JTextField();
        t2.setBounds(120, 50, 120, 20);
        f.add(t2);

        // Button
        JButton b = new JButton("Add");
        b.setBounds(80, 80, 100, 30);
        f.add(b);

        // Button action
        b.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                try {
                    int num1 = Integer.parseInt(t1.getText());
                    int num2 = Integer.parseInt(t2.getText());
                    int sum = num1 + num2;

                    result.setText("Result: " + sum);
                } catch (Exception ex) {
                    result.setText("Invalid Input!");
                }
            }
        });

        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        f.setVisible(true);
    }
}

<img width="364" height="248" alt="image" src="https://github.com/user-attachments/assets/535cf114-dd72-42e8-8613-fa582188a45b" />
## assi-12
# 📝 Java Registration Form (Swing + JDBC)
This project is a **Java Swing-based Registration Form** that stores user data in a **MySQL database using JDBC**.
## Features
- GUI form using Swing
- Multiple input fields (Name, Email, Password, Gender, Course, City, Contact)
- Data stored in MySQL database
- Uses PreparedStatement (prevents SQL injection)
## Technologies Used
- Java (Swing)
- JDBC
- MySQL
- VS Codes

## Database Setup
CREATE DATABASE studentdb;
USE studentdb;

CREATE TABLE registration (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    email VARCHAR(50),
    password VARCHAR(50),
    gender VARCHAR(10),
    course VARCHAR(50),
    city VARCHAR(50),
    contact VARCHAR(15)
);

import javax.swing.*;
import java.awt.event.*;
import java.sql.*;

public class Main {
    public static void main(String[] args) {

        JFrame f = new JFrame("Form");
        f.setSize(400,400);
        f.setLayout(null);

        JLabel l1 = new JLabel("Name:");
        l1.setBounds(20,20,100,20);
        JTextField t1 = new JTextField();
        t1.setBounds(120,20,150,20);

        JLabel l2 = new JLabel("Email:");
        l2.setBounds(20,50,100,20);
        JTextField t2 = new JTextField();
        t2.setBounds(120,50,150,20);

        JLabel l3 = new JLabel("Password:");
        l3.setBounds(20,80,100,20);
        JPasswordField t3 = new JPasswordField();
        t3.setBounds(120,80,150,20);

        JLabel l4 = new JLabel("Gender:");
        l4.setBounds(20,110,100,20);
        JRadioButton r1 = new JRadioButton("Male");
        r1.setBounds(120,110,70,20);
        JRadioButton r2 = new JRadioButton("Female");
        r2.setBounds(200,110,80,20);
        ButtonGroup bg = new ButtonGroup();
        bg.add(r1); bg.add(r2);

        JLabel l5 = new JLabel("Course:");
        l5.setBounds(20,140,100,20);
        String courses[] = {"B.Tech","BCA","MCA"};
        JComboBox cb = new JComboBox(courses);
        cb.setBounds(120,140,150,20);

        JLabel l6 = new JLabel("City:");
        l6.setBounds(20,170,100,20);
        JTextField t6 = new JTextField();
        t6.setBounds(120,170,150,20);

        JLabel l7 = new JLabel("Contact:");
        l7.setBounds(20,200,100,20);
        JTextField t7 = new JTextField();
        t7.setBounds(120,200,150,20);

        JButton b = new JButton("Submit");
        b.setBounds(140,250,100,30);

        f.add(l1); f.add(t1);
        f.add(l2); f.add(t2);
        f.add(l3); f.add(t3);
        f.add(l4); f.add(r1); f.add(r2);
        f.add(l5); f.add(cb);
        f.add(l6); f.add(t6);
        f.add(l7); f.add(t7);
        f.add(b);

        b.addActionListener(e -> {
            try {
                Class.forName("com.mysql.cj.jdbc.Driver");

                Connection con = DriverManager.getConnection(
                    "jdbc:mysql://localhost:3306/studentdb",
                    "root",
                    "YOUR_PASSWORD"
                );

                String gender = r1.isSelected() ? "Male" : "Female";

                String query = "INSERT INTO registration(name,email,password,gender,course,city,contact) VALUES(?,?,?,?,?,?,?)";

                PreparedStatement pst = con.prepareStatement(query);

                pst.setString(1, t1.getText());
                pst.setString(2, t2.getText());
                pst.setString(3, new String(t3.getPassword()));
                pst.setString(4, gender);
                pst.setString(5, cb.getSelectedItem().toString());
                pst.setString(6, t6.getText());
                pst.setString(7, t7.getText());

                pst.executeUpdate();

                JOptionPane.showMessageDialog(f, "Saved!");

                con.close();

            } catch(Exception ex) {
                ex.printStackTrace();
            }
        });

        f.setVisible(true);
    }
}

<img width="485" height="494" alt="image" src="https://github.com/user-attachments/assets/e3299e6b-de0b-4e9f-8611-466e9f87319f" />
<img width="1066" height="381" alt="image" src="https://github.com/user-attachments/assets/6b74f1de-9533-49a8-9042-834e15612313" />


## assi-13
import javax.swing.*;
import java.awt.event.*;

public class Main implements ActionListener {

    JFrame f;
    JTextField t;
    String num1 = "", num2 = "", operator = "";

    Main() {
        f = new JFrame("Calculator");
        f.setSize(300, 400);
        f.setLayout(null);

        t = new JTextField();
        t.setBounds(20, 20, 240, 40);
        f.add(t);

        String buttons[] = {
            "7","8","9","/",
            "4","5","6","*",
            "1","2","3","-",
            "0","C","=","+"
        };

        int x = 20, y = 80;

        for (int i = 0; i < buttons.length; i++) {
            JButton b = new JButton(buttons[i]);
            b.setBounds(x, y, 50, 40);
            b.addActionListener(this);
            f.add(b);

            x += 60;
            if ((i + 1) % 4 == 0) {
                x = 20;
                y += 50;
            }
        }

        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        f.setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        String cmd = e.getActionCommand();

        if (cmd.matches("[0-9]")) {
            t.setText(t.getText() + cmd);
        }
        else if (cmd.matches("[+\\-*/]")) {
            num1 = t.getText();
            operator = cmd;
            t.setText("");
        }
        else if (cmd.equals("=")) {
            num2 = t.getText();
            double n1 = Double.parseDouble(num1);
            double n2 = Double.parseDouble(num2);
            double result = 0;

            switch (operator) {
                case "+": result = n1 + n2; break;
                case "-": result = n1 - n2; break;
                case "*": result = n1 * n2; break;
                case "/": result = n1 / n2; break;
            }

            t.setText("" + result);
        }
        else if (cmd.equals("C")) {
            t.setText("");
            num1 = num2 = operator = "";
        }
    }

    public static void main(String[] args) {
        new Main();
    }
}

<img width="364" height="494" alt="image" src="https://github.com/user-attachments/assets/2489e4a9-18bd-47aa-a3ef-38661fa87858" />

## assi-14
import javax.swing.*;
import java.awt.event.*;

public class Main implements ActionListener {

    JFrame f;

    JTextField a11, a12, a21, a22;
    JTextField b11, b12, b21, b22;

    JLabel r11, r12, r21, r22;

    JButton add;

    Main() {
        f = new JFrame("Matrix Addition");
        f.setSize(400, 400);
        f.setLayout(null);

        // Matrix A
        a11 = new JTextField(); a11.setBounds(50, 50, 50, 30);
        a12 = new JTextField(); a12.setBounds(110, 50, 50, 30);
        a21 = new JTextField(); a21.setBounds(50, 90, 50, 30);
        a22 = new JTextField(); a22.setBounds(110, 90, 50, 30);

        // Matrix B
        b11 = new JTextField(); b11.setBounds(200, 50, 50, 30);
        b12 = new JTextField(); b12.setBounds(260, 50, 50, 30);
        b21 = new JTextField(); b21.setBounds(200, 90, 50, 30);
        b22 = new JTextField(); b22.setBounds(260, 90, 50, 30);

        // Result labels
        r11 = new JLabel(); r11.setBounds(125, 150, 50, 30);
        r12 = new JLabel(); r12.setBounds(185, 150, 50, 30);
        r21 = new JLabel(); r21.setBounds(125, 190, 50, 30);
        r22 = new JLabel(); r22.setBounds(185, 190, 50, 30);

        // Button
        add = new JButton("Add");
        add.setBounds(140, 250, 100, 30);
        add.addActionListener(this);

        // Add components
        f.add(a11); f.add(a12); f.add(a21); f.add(a22);
        f.add(b11); f.add(b12); f.add(b21); f.add(b22);

        f.add(r11); f.add(r12); f.add(r21); f.add(r22);

        f.add(add);

        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        f.setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        try {
            int A11 = Integer.parseInt(a11.getText());
            int A12 = Integer.parseInt(a12.getText());
            int A21 = Integer.parseInt(a21.getText());
            int A22 = Integer.parseInt(a22.getText());

            int B11 = Integer.parseInt(b11.getText());
            int B12 = Integer.parseInt(b12.getText());
            int B21 = Integer.parseInt(b21.getText());
            int B22 = Integer.parseInt(b22.getText());

            r11.setText("" + (A11 + B11));
            r12.setText("" + (A12 + B12));
            r21.setText("" + (A21 + B21));
            r22.setText("" + (A22 + B22));

        } catch (Exception ex) {
            JOptionPane.showMessageDialog(f, "Invalid Input");
        }
    }

    public static void main(String[] args) {
        new Main();
    }
}
<img width="488" height="492" alt="image" src="https://github.com/user-attachments/assets/63e3193b-923b-4020-9dd3-9ba466241aac" />
<img width="480" height="491" alt="image" src="https://github.com/user-attachments/assets/fabce661-1360-4856-85c4-f84911d905e1" />

## assi-15
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

class MyPanel extends JPanel {
    String shape = "";

    public void setShape(String s) {
        shape = s;
        repaint();
    }

    protected void paintComponent(Graphics g) {
        super.paintComponent(g);

        switch (shape) {
            case "Circle":
                g.drawOval(100, 100, 100, 100);
                break;

            case "Rectangle":
                g.drawRect(100, 100, 150, 100);
                break;

            case "Oval":
                g.drawOval(80, 100, 150, 100);
                break;

            case "Line":
                g.drawLine(50, 50, 200, 200);
                break;

            case "Square":
                g.drawRect(100, 100, 100, 100);
                break;

            case "RoundRect":
                g.drawRoundRect(100, 100, 150, 100, 30, 30);
                break;

            case "Arc":
                g.drawArc(100, 100, 100, 100, 0, 180);
                break;

            case "FillCircle":
                g.fillOval(100, 100, 100, 100);
                break;

            case "FillRect":
                g.fillRect(100, 100, 150, 100);
                break;

            case "Clear":
                // nothing drawn
                break;
        }
    }
}

public class Main {
    public static void main(String[] args) {

        JFrame f = new JFrame("Shapes");
        f.setSize(400, 400);
        f.setLayout(null);

        MyPanel panel = new MyPanel();
        panel.setBounds(0, 100, 400, 300);
        f.add(panel);

        String buttons[] = {
            "Circle","Rectangle","Oval","Line","Square",
            "RoundRect","Arc","FillCircle","FillRect","Clear"
        };

        int x = 10;

        for (String text : buttons) {
            JButton b = new JButton(text);
            b.setBounds(x, 10, 90, 30);
            f.add(b);

            b.addActionListener(e -> panel.setShape(text));

            x += 95;
            if (x > 300) {
                x = 10;
            }
        }

        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        f.setVisible(true);
    }
}
<img width="478" height="491" alt="image" src="https://github.com/user-attachments/assets/b3f07078-5c59-44b0-b0c6-b183b91f7035" />
<img width="488" height="498" alt="image" src="https://github.com/user-attachments/assets/00ba1ce6-7970-4b68-86e3-6932cb0320cd" />
<img width="482" height="487" alt="image" src="https://github.com/user-attachments/assets/01167f2a-9441-4ff3-8832-2f856a203199" />
<img width="485" height="492" alt="image" src="https://github.com/user-attachments/assets/1dec8cc2-2203-4e58-8ddb-23d7f8bd4b8c" />

## assi-16
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

class PaintPanel extends JPanel implements MouseMotionListener {

    int x = -1, y = -1;
    Color color = Color.BLACK;
    int size = 5;

    PaintPanel() {
        addMouseMotionListener(this);
    }

    public void setColor(Color c) {
        color = c;
    }

    public void setSize(int s) {
        size = s;
    }

    public void mouseDragged(MouseEvent e) {
        Graphics g = getGraphics();
        g.setColor(color);
        g.fillOval(e.getX(), e.getY(), size, size);
    }

    public void mouseMoved(MouseEvent e) {}
}

public class Main {
    public static void main(String[] args) {

        JFrame f = new JFrame("Paint App");
        f.setSize(500, 500);
        f.setLayout(null);

        PaintPanel panel = new PaintPanel();
        panel.setBounds(0, 100, 500, 400);
        panel.setBackground(Color.WHITE);
        f.add(panel);

        // Color buttons
        JButton red = new JButton("Red");
        red.setBounds(10, 10, 80, 30);
        red.addActionListener(e -> panel.setColor(Color.RED));
        f.add(red);

        JButton blue = new JButton("Blue");
        blue.setBounds(100, 10, 80, 30);
        blue.addActionListener(e -> panel.setColor(Color.BLUE));
        f.add(blue);

        JButton black = new JButton("Black");
        black.setBounds(190, 10, 80, 30);
        black.addActionListener(e -> panel.setColor(Color.BLACK));
        f.add(black);

        // Size buttons
        JButton small = new JButton("Small");
        small.setBounds(10, 50, 80, 30);
        small.addActionListener(e -> panel.setSize(5));
        f.add(small);

        JButton medium = new JButton("Medium");
        medium.setBounds(100, 50, 90, 30);
        medium.addActionListener(e -> panel.setSize(10));
        f.add(medium);

        JButton large = new JButton("Large");
        large.setBounds(200, 50, 80, 30);
        large.addActionListener(e -> panel.setSize(20));
        f.add(large);

        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        f.setVisible(true);
    }
}
<img width="603" height="621" alt="image" src="https://github.com/user-attachments/assets/64183116-9fa2-4578-b3a0-c3cdd2566cd8" />

## assi-17
//addition 
package mypack;

public class Add {
    public int sum(int a, int b) {
        return a + b;
    }
}

//subtraction
package mypack;

public class Subtract {
    public int sub(int a, int b) {
        return a - b;
    }
}

//multiplication
package mypack;

public class Multiply {
    public int mul(int a, int b) {
        return a * b;
    }
}

//division
package mypack;

public class Divide {
    public int div(int a, int b) {
        return a / b;
    }
}


//modulus
package mypack;

public class Modulus {
    public int mod(int a, int b) {
        return a % b;
    }
}

//main class
import mypack.*;

public class Main {
    public static void main(String[] args) {

        Add a = new Add();
        Subtract s = new Subtract();
        Multiply m = new Multiply();
        Divide d = new Divide();
        Modulus mo = new Modulus();

        System.out.println("Addition: " + a.add(10, 5));
        System.out.println("Subtraction: " + s.sub(10, 5));
        System.out.println("Multiplication: " + m.mul(10, 5));
        System.out.println("Division: " + d.div(10, 5));
        System.out.println("Modulus: " + mo.mod(10, 5));
    }
}

<img width="891" height="190" alt="image" src="https://github.com/user-attachments/assets/1cb56f96-8b59-410c-8122-538fdd176636" />

## assi-18

//package creating 
package mypack;

public class Add {
    public int sum(int a, int b) {
        return a + b;
    }
}


//subpackage creating 
package mypack.subpack;

public class Multiply {
    public int mul(int a, int b) {
        return a * b;
    }
}


// main class
import mypack.Add;
import mypack.subpack.Multiply;

public class Main {
    public static void main(String[] args) {

        Add a = new Add();
        Multiply m = new Multiply();

        System.out.println("Sum: " + a.sum(5, 3));
        System.out.println("Multiply: " + m.mul(5, 3));
    }
}

<img width="927" height="184" alt="image" src="https://github.com/user-attachments/assets/13526b40-8830-407f-ac6f-d1b22492ee69" />


## assi-19

public class Main {
    public static void main(String[] args) {

        // Array Exception
        try {
            int arr[] = new int[5];

            // Valid
            arr[0] = 10;

            // Invalid (index out of bounds)
            arr[5] = 20;

        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Error: Array index is out of bounds!");
        }

        //  Arithmetic Exception
        try {
            int a = 10;
            int b = 0;

            int result = a / b; // divide by zero

        } catch (ArithmeticException e) {
            System.out.println("Error: Cannot divide by zero!");
        }

        System.out.println("Program continues after handling exceptions.");
    }
}

<img width="684" height="173" alt="image" src="https://github.com/user-attachments/assets/f0501d7e-d86d-4126-b70d-6010b1322b8e" />


## assi-20

// Custom Exception Class
class InvalidAgeException extends Exception {
    InvalidAgeException(String message) {
        super(message);
    }
}

public class Main {

    // Method to check age
    static void checkAge(int age) throws InvalidAgeException {
        if (age < 18) {
            throw new InvalidAgeException("Age is less than 18. Not eligible.");
        } else {
            System.out.println("Valid age. Eligible.");
        }
    }

    public static void main(String[] args) {

        try {
            int age = 16;  // change this value to test
            checkAge(age);
        } catch (InvalidAgeException e) {
            System.out.println("Exception: " + e.getMessage());
        }

        System.out.println("Program ended.");
    }
}

<img width="638" height="132" alt="image" src="https://github.com/user-attachments/assets/94335b59-ebf4-4cf8-9814-578948987976" />


## assi-21

package FileHandling;
import java.io.*;

public class Main {
    public static void main(String[] args) {

        try {
            //  WRITE (overwrite)
            FileWriter fw = new FileWriter("test.txt");
            fw.write("Hello, this is file handling in Java.\n");
            fw.close();
            System.out.println("Write done.");

            // APPEND
            FileWriter fa = new FileWriter("test.txt", true);
            fa.write("This line is appended.\n");
            fa.close();
            System.out.println("Append done.");

            // READ
            FileReader fr = new FileReader("test.txt");
            int i;
            System.out.println("\nReading file:");

            while ((i = fr.read()) != -1) {
                System.out.print((char) i);
            }
            fr.close();

        } catch (Exception e) {
            System.out.println("Error: " + e);
        }
    }
}


<img width="752" height="213" alt="image" src="https://github.com/user-attachments/assets/21c794f2-2c3f-4890-96dc-1e89fe68bc1f" />


## assi-22

// Interface
interface Sports {
    void play();
}

// Abstract Class
abstract class Person {
    abstract void work();  // abstract method

    void sleep() {
        System.out.println("Person is sleeping");
    }
}

// Child Class (Inheritance + Interface)
class Student extends Person implements Sports {

    // Implement abstract method
    void work() {
        System.out.println("Student studies");
    }

    // Implement interface method
    public void play() {
        System.out.println("Student plays sports");
    }
}

public class Main {
    public static void main(String[] args) {

        Student s = new Student();

        s.work();   // from abstract class
        s.play();   // from interface
        s.sleep();  // inherited normal method
    }
}

<img width="752" height="143" alt="image" src="https://github.com/user-attachments/assets/d05f1794-3cd9-4f66-a02f-635bb4404b60" />


## Javalab
