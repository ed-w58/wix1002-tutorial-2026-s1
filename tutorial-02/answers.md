# Tutorial 02 — Answers

### Question 1


```java
public class q1 {
    public static void main(String[] args) {
	//(a)
        System.out.print("Faculty ");
        System.out.print("of ");
        System.out.print("Computer ");
	System.out.print("and ");
	System.out.print("Information ");
	System.out.println("Technology");

	//(b)
        System.out.println("Faculty\nof\nComputer\nScience\nand\nInformation\nTechnology");
    }
}
```

### Question 2


Java code:

```java
public class q2 {
    public static void main(String[] args) {
        System.out.println("\"SDN\" - Software-defined networking");
    }
}
```

### Question 3

Java code:

```java
public class q3 {
    public static void main(String[] args) {

	//(a)
        System.out.println("Hello Java!");

	//(b)
        System.out.println("Introduction to Java!");

	//(c)
        System.out.println("\\t is the horizontal tab character");

	//(d)
        System.out.println("Java is case sensitive!");
    }
}
```

### Question 4


Java code:

```java
public class q4 {
    public static void main(String[] args) {
	
	//(a)
        String matricNumber;

	//(b)
        double pi;

	//(c)
        boolean M = false;

	//(d)
        long P = 8800000000L;

	//(e)
        char letter = 'U';

	//(f)
        final String PRO = "Java";
    }
}
```

### Question 5

Java code:

```java
import java.util.Scanner;

public class q5 {
    public static void main(String[] args) {

	//(a)
        double AMOUNT = 32.5;
        AMOUNT += 10;
        System.out.println("The amount is " + AMOUNT);

	//(b)
        String chapter = "Summary";
        System.out.println(chapter);

	//(c)
        int num = 0;
        ++num;
        int num1 = num;
        System.out.println(num1);

	//(d)
        int num2 = 3000;
        System.out.printf("%4.2f%n", (double) num2);

	//(e)
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter your contact number: ");
        String contact = scanner.nextLine();
        System.out.println("Contact number: " + contact);
    }
}
```


### Question 6


Java code:

```java
import java.util.Scanner;
import java.util.Locale;

public class q6 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in).useLocale(Locale.US);
        System.out.print("Diameter: ");
        double diameter = scanner.nextDouble();
        double radius = diameter / 2.0;
        double circumference = 2 * Math.PI * radius;
        System.out.printf(Locale.US, "The circumference of the circle is: %.3f%n", circumference);
    }
}
```

### Question 7


Java code:

```java
import java.util.Scanner;
import java.util.Locale;

public class q7 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in).useLocale(Locale.US);

        System.out.print("Enter value in inch: ");
        double inch = scanner.nextDouble();
	
	double meters = inch * 2.54 / 100;

	System.out.printf(Locale.US, "%.2f inches = %.2f metres%n", inch, meters);
    }
}
```