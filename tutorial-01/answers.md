# Tutorial 01 — Answers

## Part I

### Question 1

Request two numbers from the user and print the multiplication of the numbers. The program reads two numbers, multiplies them, and prints the product. double is used because either input may contain a fraction. Zero and negative values are allowed.

IPO model:

|Input|Process|Output|
|-|-|-|
|Two numbers a and b|product = a × b|The product|

Pseudocode:

```text
START
READ a, b
product ← a × b
DISPLAY product
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\[/"Read a and b"/]
    B --> C\["product = a × b"]
    C --> D\[/"Display product"/]
    D --> E(\[Stop])
```

Java code:

```java
import java.util.Locale;
import java.util.Scanner;

public class Exercise01 {
    public static void main(String\[] args) {
        Scanner scanner = new Scanner(System.in).useLocale(Locale.US);
        double a = scanner.nextDouble();
        double b = scanner.nextDouble();
        double product = a \* b;
        System.out.printf(Locale.US, "%.2f%n", product);
    }
}
```

### Question 2

Determine whether a random number is greater than 50. The computer generates an integer from 0 to 100 inclusive. A strict greater-than condition is used, so the number 50 itself goes to the "not greater than 50" branch.

IPO model:

|Input|Process|Output|
|-|-|-|
|Generate an integer between 0–100|Compare  if n > 50|Comparison result|

Pseudocode:

```text
START
n ← RANDOM\_INTEGER(0, 100)
IF n > 50 THEN
    DISPLAY n, "Greater than 50"
ELSE
    DISPLAY n, "Not greater than 50"
END IF
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\["Generate n in 0–100"]
    B --> C{"n #gt; 50?"}
    C -->|Yes| D\[/"Display Greater than 50"/]
    C -->|No| E\[/"Display Not greater than 50"/]
    D --> F(\[Stop])
    E --> F
```

Java code:

```java
import java.util.Random;

public class Exercise02 {
    public static void main(String\[] args) {
        Random generator = new Random();
        int number = generator.nextInt(101);
        System.out.println("Number: " + number);
        if (number > 50) {
            System.out.println("Greater than 50");
        } 

&#x09;else {
            System.out.println("Not greater than 50");
        }
    }
}
```

### Question 3

Print the pass/fail grade based on the mark entered by the user. The passing mark is at least 40. "At least" means greater than or equal to, so a valid mark of 40 is a pass. Marks are integers from 0 to 100, and any other value is invalid.

IPO model:

|Input|Process|Output|
|-|-|-|
|Mark|Make sure mark is within 0–100; compare if mark ≥ 40|Invalid mark, Pass, or Fail|

Pseudocode:

```text
START
READ mark
IF mark < 0 OR mark > 100 THEN
    DISPLAY "Invalid mark"
ELSE IF mark >= 40 THEN
    DISPLAY "Pass"
ELSE
    DISPLAY "Fail"
END IF
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\[/"Read mark"/]
    B --> C{"Mark in 0–100?"}
    C -->|No| D\[/"Invalid mark"/]
    C -->|Yes| E{"mark ≥ 40?"}
    E -->|Yes| F\[/"Pass"/]
    E -->|No| G\[/"Fail"/]
    D --> H(\[Stop])
    F --> H
    G --> H
```

Java code:

```java
import java.util.Scanner;

public class Exercise03 {
    public static void main(String\[] args) {
        Scanner scanner = new Scanner(System.in);
        int mark = scanner.nextInt();
        if (mark < 0 || mark > 100) {
            System.out.println("Invalid mark");
        } 

&#x09;else if (mark >= 40) {
            System.out.println("Pass");
        } 

&#x09;else {
            System.out.println("Fail");
        }
    }
}
```

### Question 4

Print the results of the two players' dice game. Each player rolls one six-sided die. The higher value wins, and equal values produce a draw. The tie case is kept separate from either winner.

IPO model:

|Input|Process|Output|
|-|-|-|
|Generate two die values between 1–6|Compare die values from player 1 and player 2|Both values; winner or draw|

Pseudocode:

```text
START
p1 ← RANDOM\_INTEGER(1, 6)
p2 ← RANDOM\_INTEGER(1, 6)
DISPLAY p1, p2
IF p1 > p2 THEN
    DISPLAY "Player 1 wins"
ELSE IF p2 > p1 THEN
    DISPLAY "Player 2 wins"
ELSE
    DISPLAY "Draw"
END IF
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\[/"Generate and display both rolls"/]
    B --> C{"p1 #gt; p2?"}
    C -->|Yes| D\[/"Player 1 wins"/]
    C -->|No| E{"p2 #gt; p1?"}
    E -->|Yes| F\[/"Player 2 wins"/]
    E -->|No| G\[/"Draw"/]
    D --> H(\[Stop])
    F --> H
    G --> H
```

Java code:

```java
import java.util.Random;

public class Exercise04 {
    public static void main(String\[] args) {
        Random generator = new Random();
        int player1 = generator.nextInt(1, 7);
        int player2 = generator.nextInt(1, 7);
        System.out.printf("Player 1: %d, Player 2: %d%n", player1, player2);
        if (player1 > player2) {
            System.out.println("Player 1 wins");
        } 

&#x09;else if (player2 > player1) {
            System.out.println("Player 2 wins");
        } 

&#x09;else {
            System.out.println("Draw");
        }
    }
}
```

### Question 5

Print the perimeter of a rectangle. The length and width are read in centimetres and must both be positive, so zero or negative dimensions are rejected. The perimeter is 2 × (length + width), and the parentheses are needed around the sum.

IPO model:

|Input|Process|Output|
|-|-|-|
|Length and width in cm|is length and width > 0; perimeter = 2 × (length + width)|Perimeter in cm or an invalid-dimensions message|

Pseudocode:

```text
START
READ length, width
IF length <= 0 OR width <= 0 THEN
    DISPLAY "Invalid dimensions"
ELSE
    perimeter ← 2 × (length + width)
    DISPLAY perimeter
END IF
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\[/"Read length and width"/]
    B --> C{"Valid dimensions?"}
    C -->|Yes| D\["p = 2 × (length + width)"]
    C -->|No| E\[/"Display Invalid dimensions"/]
    D --> F\[/"Display p"/]
    E --> G(\[Stop])
    F --> G
```

Java code:

```java
import java.util.Locale;
import java.util.Scanner;

public class Exercise05 {
    public static void main(String\[] args) {
        Scanner scanner = new Scanner(System.in).useLocale(Locale.US);

&#x09;System.out.print("Enter length in cm: ");

&#x20;       double length = scanner.nextDouble();

&#x09;System.out.print("Enter width in cm: ");
        double width = scanner.nextDouble();
        if (!Double.isFinite(length) || !Double.isFinite(width)
                || length <= 0 || width <= 0) {
            System.out.println("Invalid dimensions");
        } 

&#x09;else {
            double perimeter = 2 \* (length + width);
            System.out.printf(Locale.US, "Perimeter: %.2f cm%n", perimeter);
        }
    }
}
```

### Question 6

Print the minimum number from 10 random numbers generated by computer. Exactly 10 integers from 0 to 100 are generated. The minimum starts as the first value (not 0, because every number might be positive), and then each new number is compared with it.

IPO model:

|Input|Process|Output|
|-|-|-|
|Generate ten integers from 0–100|Track the smallest value while inspecting all 10|The list of generated integers and its minimum|

Pseudocode:

```text
START
minimum ← RANDOM\_INTEGER(0, 100)
DISPLAY minimum
count ← 1
WHILE count < 10 DO
    n ← RANDOM\_INTEGER(0, 100)
    DISPLAY n
    IF n < minimum THEN
        minimum ← n
    END IF
    count ← count + 1
END WHILE
DISPLAY minimum
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\["Generate first value; min = value"]
    B --> C\["count = 1"]
    C --> D{"count #lt; 10?"}
    D -->|Yes| E\["Generate next n; display n"]
    E --> F{"n #lt; min?"}
    F -->|Yes| G\["min = n"]
    F -->|No| H\["Keep min"]
    G --> I\["count = count + 1"]
    H --> I
    I --> D
    D -->|No| J\[/"Display min"/]
    J --> K(\[Stop])
```

Java code:

```java
import java.util.Random;

public class Exercise06 {
    public static void main(String\[] args) {

&#x20;       Random generator = new Random();
        int minimum = generator.nextInt(0, 101);
        System.out.print(minimum + " ");
        for (int count = 1; count < 10; count++) {
            int number = generator.nextInt(101);
            System.out.print(number + " ");
            if (number < minimum) {
                minimum = number;
            }
        }
        System.out.println();
        System.out.println("Minimum: " + minimum);
    }
}
```

### Question 7

Print the number of odd and even number from 10 random numbers generated by computer. The random number must be from 10 – 100. Both endpoints are included and exactly ten integers are counted. A remainder of zero after division by two means the number is even, otherwise it is odd.

IPO model:

|Input|Process|Output|
|-|-|-|
|Generate 10 integers from 10–100|Use n % 2 == 0 to test even integers; increment even or odd|The list, odd count, and even count|

Pseudocode:

```text
START
even ← 0
odd ← 0
count ← 0
WHILE count < 10 DO
    n ← RANDOM\_INTEGER(10, 100)
    DISPLAY n
    IF n MOD 2 = 0 THEN
        even ← even + 1
    ELSE
        odd ← odd + 1
    END IF
    count ← count + 1
END WHILE
DISPLAY even, odd
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\["even = 0; odd = 0; count = 0"]
    B --> C{"count #lt; 10?"}
    C -->|Yes| D\["Generate n in 10–100"]
    D --> E{"n % 2 == 0?"}
    E -->|Yes| F\["even = even + 1"]
    E -->|No| G\["odd = odd + 1"]
    F --> H\["count = count + 1"]
    G --> H
    H --> C
    C -->|No| I\[/"Display even and odd"/]
    I --> J(\[Stop])
```

Java code:

```java
import java.util.Random;


public class Exercise07 {
    public static void main(String\[] args) {
        Random generator = new Random();
        int even = 0;

&#x09;int odd = 0;
        for (int count = 0; count < 10; count++) {
            int number = generator.nextInt(10, 101);
            System.out.print(number + " ");
            if (number % 2 == 0) {
                even++;
            } 

&#x09;    else {
                odd++;

&#x09;    }
        }
        System.out.println();
        System.out.printf("Even: %d, Odd: %d%n", even, odd);
    }
}
```

## Part II

### Question 8

Count the number of alphabet U and M from a sentence entered by user. The whole sentence is read with nextLine(), then the program visits one character at a time. Only uppercase U and uppercase M are counted, so lowercase u and m are not counted.

IPO model:

|Input|Process|Output|
|-|-|-|
|One complete sentence|Inspect each character; count 'U' and 'M'|U count and M count|

Pseudocode:

```text
START
READ sentence
uCount ← 0
mCount ← 0
index ← 0
WHILE index < LENGTH(sentence) DO
    ch ← CHARACTER\_AT(sentence, index)
    IF ch = 'U' THEN
        uCount ← uCount + 1
    ELSE IF ch = 'M' THEN
        mCount ← mCount + 1
    END IF
    index ← index + 1
END WHILE
DISPLAY uCount, mCount
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\[/"Read sentence"/]
    B --> C\["U = 0; M = 0; i = 0"]
    C --> D{"i #lt; sentence length?"}
    D -->|Yes| E\["Read character at i"]
    E --> F{"ch is U or M?"}
    F -->|Yes| G\["Increment matching counter"]
    F -->|No| H\["Keep both counters"]
    G --> I\["i = i + 1"]
    H --> I
    I --> D
    D -->|No| J\[/"Display U and M counts"/]
    J --> K(\[Stop])
```

Java code:

```java
import java.util.Random;
import java.util.Scanner;

public class Exercise08 {
    public static void main(String\[] args) {
        Scanner scanner = new Scanner(System.in);

&#x20;       Random generator = new Random();
        String sentence = scanner.nextLine();
        int uCount = 0;

&#x09;int mCount = 0;
        for (int index = 0; index < sentence.length(); index++) {
            char letter = sentence.charAt(index);
            if (letter == 'U') {
                uCount++;
            } 

&#x09;    else if (letter == 'M') {
                mCount++;
            }
        }
        System.out.printf("U: %d, M: %d%n", uCount, mCount);
    }
}
```

### Question 9

Display the frequency of a keyword from a web page. The text of the web page is entered by the user, followed by one English keyword. Case is ignored, and only whole words are counted, so "Java" does not match "JavaScript". The program processes the page text only, and does not download or parse HTML.

IPO model:

|Input|Process|Output|
|-|-|-|
|Page text and one keyword by user|Ignore case; split into words; count exact matches|Keyword and frequency|

Pseudocode:

```text
START
READ pageText, keyword
VALIDATE keyword is one non-empty word
words ← TOKENIZE(LOWERCASE(pageText))
count ← 0
FOR EACH word IN words DO
    IF word = LOWERCASE(keyword) THEN
        count ← count + 1
    END IF
END FOR
DISPLAY keyword, count
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\[/"Read page text and keyword"/]
    B --> C\["Validate word; normalize; tokenize"]
    C --> D\["count = 0"]
    D --> E{"More words?"}
    E -->|Yes| F{"word equals keyword?"}
    F -->|Yes| G\["count = count + 1"]
    F -->|No| H\["Keep count"]
    G --> I\["Move to next word"]
    H --> I
    I --> E
    E -->|No| J\[/"Display frequency"/]
    J --> K(\[Stop])
```

Java code:

```java
import java.util.Locale;
import java.util.Scanner;

public class Exercise09 {
    public static void main(String\[] args) {
        Scanner scanner = new Scanner(System.in).useLocale(Locale.US);



&#x09;System.out.print("Enter page text: ");
        String pageText = scanner.nextLine();



&#x09;System.out.print("Enter a keyword: ");
        String keyword = scanner.nextLine().trim().toLowerCase(Locale.ROOT);


        if (!keyword.matches("\[a-z0-9\_]+")) {
            System.out.println("Enter one English keyword");
        } 

&#x09;else {
            String\[] words = pageText.toLowerCase(Locale.ROOT).split("\[^a-z0-9\_]+");
            int frequency = 0;
            for (String word : words) {
                if (word.equals(keyword)) {
                    frequency++;
                }
            }

&#x09;System.out.println("Keyword: " + keyword);
        System.out.println("Frequency: " + frequency);
        }
    }
}
```

### Question 10

Display the number of female student from a random list of 100 students. The list is 100 synthetic records, each randomly labelled F, M, or X (X means another or unspecified category). Only records labelled F are counted. The count is different on every run because the list is random.

IPO model:

|Input|Process|Output|
|-|-|-|
|100 randomly generated synthetic records|Inspect each label; count F records|F count|

Pseudocode:

```text
START
femaleCount ← 0
FOR index FROM 1 TO 100 DO
    label ← RANDOM\_CHOICE('F', 'M', 'X')
    DISPLAY index, label
    IF label = 'F' THEN
        femaleCount ← femaleCount + 1
    END IF
END FOR
DISPLAY femaleCount
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\["female = 0; index = 1"]
    B --> C{"index ≤ 100?"}
    C -->|Yes| D\["Generate F, M, or X; display record"]
    D --> E{"label is F?"}
    E -->|Yes| F\["female = female + 1"]
    E -->|No| G\["Keep female"]
    F --> H\["index = index + 1"]
    G --> H
    H --> C
    C -->|No| I\[/"Display female count"/]
    I --> J(\[Stop])
```

Java code:

```java
import java.util.Random;

public class Exercise10 {
    public static void main(String\[] args) {
        Random generator = new Random();
        String\[] labels = {"F", "M", "X"};
        int femaleCount = 0;
        for (int index = 1; index <= 100; index++) {
            String label = labels\[generator.nextInt(labels.length)];
            System.out.printf("%03d: %s%n", index, label);
            if (label.equals("F")) {
                femaleCount++;
            }
        }
        System.out.println("Female records: " + femaleCount);
    }
}
```

### Question 11

Display a list of 5 random numbers in descending order. (Sort) Five integers from 0 to 100 are generated and duplicates are kept. The array is sorted with Arrays.sort, which sorts from smallest to largest, and then the numbers are printed from the last position back to the first so they appear largest first.

IPO model:

|Input|Process|Output|
|-|-|-|
|Generate 5 integers|Sort the array ascending; traverse it backwards|A descending list|

Pseudocode:

```text
START
GENERATE five random integers into numbers
SORT numbers in ascending order
index ← LENGTH(numbers) - 1
WHILE index >= 0 DO
    DISPLAY numbers\[index]
    index ← index - 1
END WHILE
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\["Generate five values"]
    B --> C\["Sort ascending; i = length − 1"]
    C --> D{"i ≥ 0?"}
    D -->|Yes| E\[/"Display numbers\[i]"/]
    E --> F\["i = i − 1"]
    F --> D
    D -->|No| G(\[Stop])
```

Java code:

```java
import java.util.Arrays;
import java.util.Random;

public class Exercise11 {
    public static void main(String\[] args) {
        Random generator = new Random();
        int\[] numbers = new int\[5];
        for (int index = 0; index < numbers.length; index++) {
            numbers\[index] = generator.nextInt(0, 101);
        }
        System.out.println("Original: " + Arrays.toString(numbers));
        Arrays.sort(numbers);
        for (int index = numbers.length - 1; index >= 0; index--) {
            System.out.print(numbers\[index] + " ");
        }
        System.out.println();
    }
}
```

### Question 12

Guess a random number generated by computer. The computer chooses the target once (from 1 to 100) before the guessing loop starts, and each guess is compared with it. The program gives a Higher or Lower hint until the guess is correct, then shows the number of attempts. Guesses outside 1–100 are rejected and not counted.

IPO model:

|Input|Process|Output|
|-|-|-|
|A fixed random target and repeated guesses|Compare guess with target; repeat while unequal|Higher, Lower, or Correct; attempt count|

Pseudocode:

```text
START
target ← RANDOM\_INTEGER(1, 100)
attempts ← 0
REPEAT
    READ guess
    IF guess < 1 OR guess > 100 THEN
        DISPLAY "Enter 1–100"
    ELSE
        attempts ← attempts + 1
        IF guess < target THEN
            DISPLAY "Higher"
        ELSE IF guess > target THEN
            DISPLAY "Lower"
        ELSE
            DISPLAY "Correct", attempts
        END IF
    END IF
UNTIL guess = target
STOP
```

Flowchart:

```mermaid
flowchart TD
    A(\[Start]) --> B\["Generate target once; attempts = 0"]
    B --> C\[/"Read guess"/]
    C --> D{"Integer in 1–100?"}
    D -->|No| E\[/"Show Enter 1–100"/]
    E --> C
    D -->|Yes| F\["attempts = attempts + 1"]
    F --> G{"guess == target?"}
    G -->|Yes| H\[/"Show Correct"/]
    H --> I(\[Stop])
    G -->|No| J\[/"Compare; show Higher or Lower"/]
    J --> C
```

Java code:

```java
import java.util.Random;
import java.util.Scanner;

public class Exercise12 {
    public static void main(String\[] args) {
        Scanner scanner = new Scanner(System.in);

&#x20;       Random generator = new Random();
        int target = generator.nextInt(1, 101);
        int attempts = 0;
        int guess;
        do {

&#x09;    System.out.print("Enter your guess (1-100): ");
            guess = scanner.nextInt();
            if (guess < 1 || guess > 100) {
                System.out.println("Enter 1-100");
                continue;
            }
            attempts++;
            if (guess < target) {
                System.out.println("Higher");
            } else if (guess > target) {
                System.out.println("Lower");
            } else {
                System.out.println("Correct in " + attempts + " attempts");
            }
        } while (guess != target);
    }
}
```

