# Tutorial 06 — Answers



### Question 1a

```java
static int max (int a, int b, int c) {
    int max = a;
    if (a < b) {
        max = b;
    }
    if (max < c) {
        max = c;
    }
    return max;
}

int largest = max(4, 9, 7);
```



### Question 1b

```java
static Boolean isSquare(int x) {
    if (n < 0) {
        return false;
    }
    int test = Math.round(Math.sqrt(n));
    test = test * test;
    return test == x;
}

if (isSquare(49)) {
    System.out.println("49 is a square number");
}
```



### Question 1c

```java
static long formula(int a, int b) {
    return factorial(a) / factorial(b) * factorial(a - b);
}
static long factorial (int x) {
    for (int i = 1; i < x; i++) {
	x *= i;
    }
    return x;
}

System.out.println(formula(5, 2));
```



### Question 1d

```java
static boolean isPentagonal(int x) {
    if (x < 1) {
        return false;     
    }
    long p = 0;
    for (long n = 1; p < x; n++) {
        p = n * (3 * n - 1) / 2;       
    }
    return p == x;                    
}


System.out.println(isPentagonal(35)); 
```



### Question 1e

```java
static void countLettersDigits(String text) {
    int letters = 0;
    int digits = 0;
    for (int i = 0; i < text.length(); i++) {
        char ch = text.charAt(i);
        if (Character.isLetter(ch)) {
	    letters++;
	}
	else if (Character.isDigits(ch)) {
	    digits++;
	}
    }
    System.out.println("Letters: " + letters + ", digits: " + digits);
}
countLettersDigits("WIX1002 Java 27!");
```



### Question 1f

```java
static void fillRandom(int[] values) {
    for (int i = 0; i < values.length; i++) {
        values[i] = rand.nextInt(101);     
    }
}

int[] numbers = new int[10];
fillRandom(numbers);          
System.out.println(numbers[0]);
System.out.println(numbers[9]);
```



### Question 1g

```java
static void circle(double radius, double[] result) {
    result[0] = Math.PI * radius * radius; 
    result[1] = 2 * Math.PI * radius;  
}

double[] Result = new double[2];
circle(2.5, Result);
System.out.printf("area %.2f, circumference %.2f%n", Result[0], Result[1]);
```



### Question 1h

```java
static int repeat() {
    boolean[] seen = new boolean[11];
    while(true) {
        int num = rand.nextInt(11);
    	if (seen[num]) {
	    return num;
    	}
        seen[num] = true;
    }
}

System.out.println("First repeat: " + repeat());
```

### Question 2

```java
import java.util.Scanner;

public class DecreasingOrder {
    static void printDecreasing(int a, int b, int c) {
	int hold;
	if (a < b) {
	    hold = a;
	    a = b;
	    b = hold;
	}
	if (a < c) {
	    hold = a;
	    a = c;
	    c = hold;
	}
	if (b < c) {
	    hold = b;
	    b = c;
	    c = hold;
	}
	System.out.println(a + " " + b + " " + c);
    }
    
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter three integers: ");
        int x = sc.nextInt();
        int y = sc.nextInt();
        int z = sc.nextInt();    

	 System.out.print("Decreasing order: ");
        printDecreasing(x, y, z);
    }
}
```





