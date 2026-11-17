# Tutorial 04 — Answers

### Question 1

1a
```java
public class Q1a {
    public static void main(String[] args) {
        int cube = 2000;
        int n = 0;
        
        while ( (n * n * n) < cube && ( (n + 1) * (n + 1) * (n + 1) < cube) ) {
            n++;
        }
        System.out.println("n is " + n);
    }
}
```

1b
```java
public class Q1b {
    public static void main(String[] args) {
        int n = 1;
        while (n < 13) {
            int sq = n * n;
            System.out.println("square of " + n + " is " + sq);
            n++;
        }
    }
}
```

1c
```java
import java.util.Random;

public class Q1c {
    public static void main(String[] args) {
        Random rand = new Random();
        for (int i = 0; i < 4; i++){
            for (int j = 0; j < 5; j++) {
                int column = rand.nextInt(101);
                System.out.printf("%4d ", column);
            }
        System.out.println("");
        }
    }
}
```

1d
```java
import java.util.Scanner;

public class Q1d {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = sc.nextInt();
        sc.nextLine();
        int total = 0;
        
        for (int i = 0; i <= n; i++) {
            total += i;
        }
        System.out.println("The sum is " + total);
    }
}
```

1e
```java
public class Q1e {
    public static void main(String[] args) {
        double sum = 0;
        int n = 26;
        for (int i = 1; i < n; i++) {
            sum += (double) i / (n - i);
        }
        System.out.printf("Sum: %.2f%n", sum);
        
    }
}
```

### Question 2

2a

```java
int sum = 0;
for (int x = 10; x > 0; x--)
    sum += x;
```

2b

```java
int x = 0;
int y = 0;
do {
    x += 2;
    y += x;
    System.out.println(x + " and " + y);
} while (x < 100);
```

2c

```java
int x;
int y;
for (x = 1, y = 20; x < y; x++, y-=2) {
    System.out.println(x + " " + y);
}
```

2d

```java
int i = 1;
while (i <= 10) {
    if (i == 10)
        System.out.println("Program End");
    i++;
}
```

### Question 3

```java
public class Q3 {
    public static void main(String[] args) {
        int previous = 0;
        int current = 1;
        int sum = 1;
        for (int i = 1; i <= 10; i++) {
            System.out.println(sum + " ");
            sum = previous + current;
            previous = sum - previous;
            current = sum;
        }
    }    
}
```

### Question 4

```java
import java.util.Scanner;

public class Q4 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a sentence to reverse: ");
        String reverse = sc.nextLine();
        for (int i = reverse.length() - 1; i >= 0; i--) {
            char letter = reverse.charAt(i);
            System.out.print(letter);
        }
        System.out.println("");
    }    
}
```
