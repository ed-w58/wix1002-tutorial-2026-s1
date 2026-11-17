# Tutorial 05 — Answers

### Question 1
1a
```java
double[] numbers = new double[12];
```
1b
```java
char[] letter = {'A', 'B', 'C', 'D', 'E'};
```
1c
```java
String[] names = new String[100];
```
1d
```java
int[][] values = new int[6][2];
```
1e
```java
int[][] values = {{6, 9}, {2, 5}, {4, 6}};
```
1f
```java
values[1][1] = 4;
values[2][0] = 3;
values[2][1] = 7;
```
1g
```java
for (int i = 0; i < contact.length; i++) {
    System.out.println(contact[i]); 
}
```
       
### Question 2
2a
```java
String[] code = {"AAA", "AAB", "AAC", "AAD"};
```
2b
```java
int[] num = new num[10];
int sum = 0;
for(int k=0; k<num.length(); k++)
    sum += num[k];
```
2c
```java
int [][]t = new int[3][3];
t[1][2] = 5;
```
2d
```java
int i=4;
int []score = new int[5];
score [1] = 78;
score[i] = 100;
```

### Question 3
```java
int[] marks = {961, 31, 1, 31, 31};
```

### Question 4
```java
String[] sentence = {"the", "cat", "and", "The", "dog", "saw", "the", "bird"};
int count = 0;
for (int i = 0; i < sentence.length; i++) {
    if (sentence[i].equals("the")) {
        count++;
    }
}
System.out.println("\"the\" occurs " + count + " time(s)");
```


### Question 5
```java
for (int i = sentence.length - 1; i >= 0; i--) {
    for (int j = sentence[i].length - 1; j >= 0; j--) {
        System.out.print(sentence[i].charAt(j));
    }
    if (i != 0) {
        System.out.print(" "); 
    }
}
System.out.println(""); 
```


### Question 6
```java
import java.util.Random;

public class Q6 {
    public static void main(String[] args) {
        Random rand = new Random();
        int number = random.nextInt(256);   

        int[] bits = new int[8];            
        int value = number;
        for (int i = 7; i >= 0; i--) {
            bits[i] = value % 2;            
            value = value / 2;
        }

        System.out.println("Random number: " + number);
        System.out.print("Binary: ");
        for (int i = 0; i < bits.length; i++) {
            System.out.print(bits[i]);
        }
        System.out.println();
    }
}
```
