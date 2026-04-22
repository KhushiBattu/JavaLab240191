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

[PROGRAM-10. Using the concept of multithreading the output of all three threads must be synchronised (use join method).] (#assi-10)

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

## Javalab
