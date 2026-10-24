# Tutorial 03 — Answers

### Question 1


```java
import java.util.Scanner;

public class q1 {
    public static void main(String[] args) {

        //1a
        boolean x = 3 * 8 == 27;
        System.out.println("3 x 8 == 27: " + x);
        
        //1b
        Scanner sc = new Scanner (System.in);
        System.out.print("Enter an interger: ");
        int num = sc.nextInt();
        sc.nextLine();
        if (num % 2 == 0){
            System.out.println(num + " is an even number.");
        }
        else {
            System.out.println(num + " is an odd number.");
        }
        
        //1c
        char letter;
        System.out.print("Enter a letter: ");
        letter = sc.next().charAt(0);
        sc.nextLine();
        if (letter >= 'A' && letter <= 'Z'){
            System.out.println(letter + " is a capital letter.");
        }
        else if (letter >= 'a' && letter  <= 'z'){
            System.out.println(letter + " is not a capital letter.");
        }
        else {
            System.out.println("Invalid");
        }
        
        //1d
        String word1;
        String word2;
        System.out.print("Enter first word: ");
        word1 = sc.nextLine();
        System.out.print("Enter second word: ");
        word2 = sc.nextLine();
        if (word1.compareToIgnoreCase(word2) <= 0){
            System.out.println(word1 + " " + word2);
        }
        else {
            System.out.println(word2 + " " + word1);
        }
        
        //1e
        System.out.print("Enter a day number (0-6): ");
        int dayNum = sc.nextInt();
        switch (dayNum) {
            case 0:
                System.out.println("Sunday");
                break;
            case 1:
                System.out.println("Monday");
                break;
            case 2:
                System.out.println("Tuesday");
                break;
            case 3: 
                System.out.println("Wednesday");
                break;
            case 4:
                System.out.println("Thursday");
                break;
            case 5:
                System.out.println("Friday");
                break;
            case 6:
                System.out.println("Saturday");
                break;
            default: 
                System.out.println("Invalid day number!");
        }
    }
}
```

### Question 2


```java
//2a
if (num1 == num2)
    System.out.println("Number 1 is equal to number 2.");

//2b
if (x > y && x > z)
    System.out.println("x is the largest number");

//2c
String s1 = "Java", s2 = "Java";
if (s1.equals(s2))
    System.out.println("They are equal strings.");
else
    System.out.println("They are not equal strings.");

//2d
if (x > 0 || y > 0)
    System.out.println("Either x or y is positive");
```

### Question 3


```java
//3a
if (x < 10)
    if (y > 10)
        System.out.println("*****");
    else
        System.out.println("#####");
System.out.println("$$$$$");		// Output: #####  then  $$$$$

//3b
if (x < 10) {
    if (y < 10)
	System.out.println("*****");
    else{
	System.out.println("#####");
	System.out.println("$$$$$");
    }
}					// Output: #####  then  $$$$$	

//3c
if (x < 10) {
    if (y < 10)
	System.out.println("*****");
    System.out.println("#####");
}
else {
    System.out.println("$$$$$");
}					// Output: #####

//3d
if (x > 10) {
    if (y > 10) {
	System.out.println("*****");
	System.out.println("#####");
    }
    else
	System.out.println("$$$$$");
}					// Output: (nothing)
```

### Question 4



```java
import java.util.Scanner;

public class q4 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int x;
        int y;
        int z;
        int biggest;
        
        System.out.print("Enter first integer: ");
        x = sc.nextInt();
        sc.nextLine();
        biggest = x;
                
        System.out.print("Enter second integer: ");
        y = sc.nextInt();
        sc.nextLine();
        if (y > biggest){
            biggest = y;
        }

        System.out.print("Enter third integer: ");
        z = sc.nextInt();
        sc.nextLine();
        if (z > biggest){
            biggest = z;
        }
        
        System.out.println("The biggest number is " + biggest);
    }
}
```

### Question 5


```java
import java.util.Scanner;

public class q5 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a year: ");
        int year = sc.nextInt();
        sc.nextLine();
        
        if (year % 400 == 0 || year % 4 == 0 && year % 100 != 0){
            System.out.println(year + " is a leap year.");
        }
        else {
            System.out.println(year + " is not a leap year.");
        }
    }
}
```

