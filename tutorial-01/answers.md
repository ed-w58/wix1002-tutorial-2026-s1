\# Tutorial 01 — Answers



\## Part I



\### Question 1



Request two numbers from the user and print the multiplication of the numbers. The program reads two numbers, multiplies them, and prints the product. double is used because either input may contain a fraction. Zero and negative values are allowed.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| Two numbers a and b | product = a × b | The product |



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

&#x20;   A(\[Start]) --> B\[/"Read a and b"/]

&#x20;   B --> C\["product = a × b"]

&#x20;   C --> D\[/"Display product"/]

&#x20;   D --> E(\[Stop])

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise01 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       double a = keyboard.nextDouble();

&#x20;       double b = keyboard.nextDouble();

&#x20;       double product = a \* b;

&#x20;       System.out.println(product);

&#x20;   }

}

```



\### Question 2



Determine whether a random number is greater than 50. The computer generates an integer from 0 to 100 inclusive. A strict greater-than condition is used, so the number 50 itself goes to the "not greater than 50" branch.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| A generated integer n in 0–100 | Compare n > 50 | The number and the comparison result |



Pseudocode:



```text

START

n ← RANDOM\_INTEGER(0, 100)

IF n > 50 THEN

&#x20;   DISPLAY n, "Greater than 50"

ELSE

&#x20;   DISPLAY n, "Not greater than 50"

END IF

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\["Generate n in 0–100"]

&#x20;   B --> C{"n #gt; 50?"}

&#x20;   C -->|Yes| D\[/"Display Greater than 50"/]

&#x20;   C -->|No| E\[/"Display Not greater than 50"/]

&#x20;   D --> F(\[Stop])

&#x20;   E --> F

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise02 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       int number = generator.nextInt(0, 101);

&#x20;       System.out.println("Number: " + number);

&#x20;       if (number > 50) {

&#x20;           System.out.println("Greater than 50");

&#x20;       } else {

&#x20;           System.out.println("Not greater than 50");

&#x20;       }

&#x20;   }

}

```



\### Question 3



Print the pass/fail grade based on the mark entered by the user. The passing mark is at least 40. "At least" means greater than or equal to, so a valid mark of 40 is a pass. Marks are integers from 0 to 100, and any other value is invalid.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| Integer mark | Validate 0–100; compare mark ≥ 40 | Invalid mark, Pass, or Fail |



Pseudocode:



```text

START

READ mark

IF mark < 0 OR mark > 100 THEN

&#x20;   DISPLAY "Invalid mark"

ELSE IF mark >= 40 THEN

&#x20;   DISPLAY "Pass"

ELSE

&#x20;   DISPLAY "Fail"

END IF

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\[/"Read mark"/]

&#x20;   B --> C{"Mark in 0–100?"}

&#x20;   C -->|No| D\[/"Invalid mark"/]

&#x20;   C -->|Yes| E{"mark ≥ 40?"}

&#x20;   E -->|Yes| F\[/"Pass"/]

&#x20;   E -->|No| G\[/"Fail"/]

&#x20;   D --> H(\[Stop])

&#x20;   F --> H

&#x20;   G --> H

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise03 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       int mark = keyboard.nextInt();

&#x20;       if (mark < 0 || mark > 100) {

&#x20;           System.out.println("Invalid mark");

&#x20;       } else if (mark >= 40) {

&#x20;           System.out.println("Pass");

&#x20;       } else {

&#x20;           System.out.println("Fail");

&#x20;       }

&#x20;   }

}

```



\### Question 4



Print the results of the two players' dice game. Each player rolls one six-sided die. The higher value wins, and equal values produce a draw. The tie case is kept separate from either winner.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| Two generated die values in 1–6 | Compare player 1 and player 2 | Both values; winner or draw |



Pseudocode:



```text

START

p1 ← RANDOM\_INTEGER(1, 6)

p2 ← RANDOM\_INTEGER(1, 6)

DISPLAY p1, p2

IF p1 > p2 THEN

&#x20;   DISPLAY "Player 1 wins"

ELSE IF p2 > p1 THEN

&#x20;   DISPLAY "Player 2 wins"

ELSE

&#x20;   DISPLAY "Draw"

END IF

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\[/"Generate and display both rolls"/]

&#x20;   B --> C{"p1 #gt; p2?"}

&#x20;   C -->|Yes| D\[/"Player 1 wins"/]

&#x20;   C -->|No| E{"p2 #gt; p1?"}

&#x20;   E -->|Yes| F\[/"Player 2 wins"/]

&#x20;   E -->|No| G\[/"Draw"/]

&#x20;   D --> H(\[Stop])

&#x20;   F --> H

&#x20;   G --> H

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise04 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       int player1 = generator.nextInt(1, 7);

&#x20;       int player2 = generator.nextInt(1, 7);

&#x20;       System.out.printf("Player 1: %d, Player 2: %d%n", player1, player2);

&#x20;       if (player1 > player2) {

&#x20;           System.out.println("Player 1 wins");

&#x20;       } else if (player2 > player1) {

&#x20;           System.out.println("Player 2 wins");

&#x20;       } else {

&#x20;           System.out.println("Draw");

&#x20;       }

&#x20;   }

}

```



\### Question 5



Print the perimeter of a rectangle. The length and width are read in centimetres and must both be positive, so zero or negative dimensions are rejected. The perimeter is 2 × (length + width), and the parentheses are needed around the sum.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| Length and width in cm | Validate; perimeter = 2 × (length + width) | Perimeter in cm or an invalid-dimensions message |



Pseudocode:



```text

START

READ length, width

IF length <= 0 OR width <= 0 THEN

&#x20;   DISPLAY "Invalid dimensions"

ELSE

&#x20;   perimeter ← 2 × (length + width)

&#x20;   DISPLAY perimeter

END IF

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\[/"Read length and width"/]

&#x20;   B --> C{"Valid dimensions?"}

&#x20;   C -->|Yes| D\["p = 2 × (length + width)"]

&#x20;   C -->|No| E\[/"Display Invalid dimensions"/]

&#x20;   D --> F\[/"Display p"/]

&#x20;   E --> G(\[Stop])

&#x20;   F --> G

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise05 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       double length = keyboard.nextDouble();

&#x20;       double width = keyboard.nextDouble();

&#x20;       if (!Double.isFinite(length) || !Double.isFinite(width)

&#x20;               || length <= 0 || width <= 0) {

&#x20;           System.out.println("Invalid dimensions");

&#x20;       } else {

&#x20;           double perimeter = 2 \* (length + width);

&#x20;           System.out.printf(Locale.US, "Perimeter: %.2f cm%n", perimeter);

&#x20;       }

&#x20;   }

}

```



\### Question 6



Print the minimum number from 10 random numbers generated by computer. Exactly 10 integers from 0 to 100 are generated. The minimum starts as the first value (not 0, because every number might be positive), and then each new number is compared with it.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| 10 generated integers in 0–100 | Track the smallest value while inspecting all 10 | The list and its minimum |



Pseudocode:



```text

START

minimum ← RANDOM\_INTEGER(0, 100)

DISPLAY minimum

count ← 1

WHILE count < 10 DO

&#x20;   n ← RANDOM\_INTEGER(0, 100)

&#x20;   DISPLAY n

&#x20;   IF n < minimum THEN

&#x20;       minimum ← n

&#x20;   END IF

&#x20;   count ← count + 1

END WHILE

DISPLAY minimum

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\["Generate first value; min = value"]

&#x20;   B --> C\["count = 1"]

&#x20;   C --> D{"count #lt; 10?"}

&#x20;   D -->|Yes| E\["Generate next n; display n"]

&#x20;   E --> F{"n #lt; min?"}

&#x20;   F -->|Yes| G\["min = n"]

&#x20;   F -->|No| H\["Keep min"]

&#x20;   G --> I\["count = count + 1"]

&#x20;   H --> I

&#x20;   I --> D

&#x20;   D -->|No| J\[/"Display min"/]

&#x20;   J --> K(\[Stop])

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise06 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       int minimum = generator.nextInt(0, 101);

&#x20;       System.out.print(minimum + " ");

&#x20;       for (int count = 1; count < 10; count++) {

&#x20;           int number = generator.nextInt(0, 101);

&#x20;           System.out.print(number + " ");

&#x20;           if (number < minimum) {

&#x20;               minimum = number;

&#x20;           }

&#x20;       }

&#x20;       System.out.println();

&#x20;       System.out.println("Minimum: " + minimum);

&#x20;   }

}

```



\### Question 7



Print the number of odd and even number from 10 random numbers generated by computer. The random number must be from 10 – 100. Both endpoints are included and exactly ten integers are counted. A remainder of zero after division by two means the number is even, otherwise it is odd.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| 10 generated integers in 10–100 | Test n % 2 == 0; increment even or odd | The list, odd count, and even count |



Pseudocode:



```text

START

even ← 0

odd ← 0

count ← 0

WHILE count < 10 DO

&#x20;   n ← RANDOM\_INTEGER(10, 100)

&#x20;   DISPLAY n

&#x20;   IF n MOD 2 = 0 THEN

&#x20;       even ← even + 1

&#x20;   ELSE

&#x20;       odd ← odd + 1

&#x20;   END IF

&#x20;   count ← count + 1

END WHILE

DISPLAY even, odd

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\["even = 0; odd = 0; count = 0"]

&#x20;   B --> C{"count #lt; 10?"}

&#x20;   C -->|Yes| D\["Generate n in 10–100"]

&#x20;   D --> E{"n % 2 == 0?"}

&#x20;   E -->|Yes| F\["even = even + 1"]

&#x20;   E -->|No| G\["odd = odd + 1"]

&#x20;   F --> H\["count = count + 1"]

&#x20;   G --> H

&#x20;   H --> C

&#x20;   C -->|No| I\[/"Display even and odd"/]

&#x20;   I --> J(\[Stop])

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise07 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       int even = 0, odd = 0;

&#x20;       for (int count = 0; count < 10; count++) {

&#x20;           int number = generator.nextInt(10, 101);

&#x20;           System.out.print(number + " ");

&#x20;           if (number % 2 == 0) {

&#x20;               even++;

&#x20;           } else {

&#x20;               odd++;

&#x20;           }

&#x20;       }

&#x20;       System.out.println();

&#x20;       System.out.printf("Even: %d, Odd: %d%n", even, odd);

&#x20;   }

}

```



\## Part II



\### Question 8



Count the number of alphabet U and M from a sentence entered by user. The whole sentence is read with nextLine(), then the program visits one character at a time. Only uppercase U and uppercase M are counted, so lowercase u and m are not counted.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| One complete sentence | Inspect each character; count 'U' and 'M' | Separate U count and M count |



Pseudocode:



```text

START

READ sentence

uCount ← 0

mCount ← 0

index ← 0

WHILE index < LENGTH(sentence) DO

&#x20;   ch ← CHARACTER\_AT(sentence, index)

&#x20;   IF ch = 'U' THEN

&#x20;       uCount ← uCount + 1

&#x20;   ELSE IF ch = 'M' THEN

&#x20;       mCount ← mCount + 1

&#x20;   END IF

&#x20;   index ← index + 1

END WHILE

DISPLAY uCount, mCount

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\[/"Read sentence"/]

&#x20;   B --> C\["U = 0; M = 0; i = 0"]

&#x20;   C --> D{"i #lt; sentence length?"}

&#x20;   D -->|Yes| E\["Read character at i"]

&#x20;   E --> F{"ch is U or M?"}

&#x20;   F -->|Yes| G\["Increment matching counter"]

&#x20;   F -->|No| H\["Keep both counters"]

&#x20;   G --> I\["i = i + 1"]

&#x20;   H --> I

&#x20;   I --> D

&#x20;   D -->|No| J\[/"Display U and M counts"/]

&#x20;   J --> K(\[Stop])

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise08 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       String sentence = keyboard.nextLine();

&#x20;       int uCount = 0, mCount = 0;

&#x20;       for (int index = 0; index < sentence.length(); index++) {

&#x20;           char ch = sentence.charAt(index);

&#x20;           if (ch == 'U') {

&#x20;               uCount++;

&#x20;           } else if (ch == 'M') {

&#x20;               mCount++;

&#x20;           }

&#x20;       }

&#x20;       System.out.printf("U: %d, M: %d%n", uCount, mCount);

&#x20;   }

}

```



\### Question 9



Display the frequency of a keyword from a web page. The text of the web page is entered by the user, followed by one English keyword. Case is ignored, and only whole words are counted, so "Java" does not match "JavaScript". The program processes the page text only, and does not download or parse HTML.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| Extracted page text and one keyword | Normalize case; split into words; count exact matches | Keyword and frequency |



Pseudocode:



```text

START

READ pageText, keyword

VALIDATE keyword is one non-empty word

words ← TOKENIZE(LOWERCASE(pageText))

count ← 0

FOR EACH word IN words DO

&#x20;   IF word = LOWERCASE(keyword) THEN

&#x20;       count ← count + 1

&#x20;   END IF

END FOR

DISPLAY keyword, count

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\[/"Read page text and keyword"/]

&#x20;   B --> C\["Validate word; normalize; tokenize"]

&#x20;   C --> D\["count = 0"]

&#x20;   D --> E{"More words?"}

&#x20;   E -->|Yes| F{"word equals keyword?"}

&#x20;   F -->|Yes| G\["count = count + 1"]

&#x20;   F -->|No| H\["Keep count"]

&#x20;   G --> I\["Move to next word"]

&#x20;   H --> I

&#x20;   I --> E

&#x20;   E -->|No| J\[/"Display frequency"/]

&#x20;   J --> K(\[Stop])

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise09 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       String pageText = keyboard.nextLine();

&#x20;       String keyword = keyboard.nextLine().trim().toLowerCase(Locale.ROOT);

&#x20;       if (!keyword.matches("\[a-z0-9\_]+")) {

&#x20;           System.out.println("Enter one English keyword");

&#x20;       } else {

&#x20;           String\[] words = pageText.toLowerCase(Locale.ROOT)

&#x20;                   .split("\[^a-z0-9\_]+");

&#x20;           int frequency = 0;

&#x20;           for (String word : words) {

&#x20;               if (word.equals(keyword)) {

&#x20;                   frequency++;

&#x20;               }

&#x20;           }

&#x20;           System.out.println("Frequency: " + frequency);

&#x20;       }

&#x20;   }

}

```



\### Question 10



Display the number of female student from a random list of 100 students. The list is 100 synthetic records, each randomly labelled F, M, or X (X means another or unspecified category). Only records labelled F are counted. The count is different on every run because the list is random.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| 100 randomly generated synthetic records | Inspect each label; count F records | The records and the F count |



Pseudocode:



```text

START

femaleCount ← 0

FOR index FROM 1 TO 100 DO

&#x20;   label ← RANDOM\_CHOICE('F', 'M', 'X')

&#x20;   DISPLAY index, label

&#x20;   IF label = 'F' THEN

&#x20;       femaleCount ← femaleCount + 1

&#x20;   END IF

END FOR

DISPLAY femaleCount

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\["female = 0; index = 1"]

&#x20;   B --> C{"index ≤ 100?"}

&#x20;   C -->|Yes| D\["Generate F, M, or X; display record"]

&#x20;   D --> E{"label is F?"}

&#x20;   E -->|Yes| F\["female = female + 1"]

&#x20;   E -->|No| G\["Keep female"]

&#x20;   F --> H\["index = index + 1"]

&#x20;   G --> H

&#x20;   H --> C

&#x20;   C -->|No| I\[/"Display female count"/]

&#x20;   I --> J(\[Stop])

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise10 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       String\[] labels = {"F", "M", "X"};

&#x20;       int femaleCount = 0;

&#x20;       for (int index = 1; index <= 100; index++) {

&#x20;           String label = labels\[generator.nextInt(labels.length)];

&#x20;           System.out.printf("%03d: %s%n", index, label);

&#x20;           if (label.equals("F")) {

&#x20;               femaleCount++;

&#x20;           }

&#x20;       }

&#x20;       System.out.println("Female records: " + femaleCount);

&#x20;   }

}

```



\### Question 11



Display a list of 5 random numbers in descending order. (Sort) Five integers from 0 to 100 are generated and duplicates are kept. The array is sorted with Arrays.sort, which sorts from smallest to largest, and then the numbers are printed from the last position back to the first so they appear largest first.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| 5 generated integers | Sort the array ascending; traverse it backwards | A descending list |



Pseudocode:



```text

START

GENERATE five random integers into numbers

SORT numbers in ascending order

index ← LENGTH(numbers) - 1

WHILE index >= 0 DO

&#x20;   DISPLAY numbers\[index]

&#x20;   index ← index - 1

END WHILE

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\["Generate five values"]

&#x20;   B --> C\["Sort ascending; i = length − 1"]

&#x20;   C --> D{"i ≥ 0?"}

&#x20;   D -->|Yes| E\[/"Display numbers\[i]"/]

&#x20;   E --> F\["i = i − 1"]

&#x20;   F --> D

&#x20;   D -->|No| G(\[Stop])

```



Java code:



```java

import java.util.Arrays;

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise11 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       int\[] numbers = new int\[5];

&#x20;       for (int index = 0; index < numbers.length; index++) {

&#x20;           numbers\[index] = generator.nextInt(0, 101);

&#x20;       }

&#x20;       System.out.println("Original: " + Arrays.toString(numbers));

&#x20;       Arrays.sort(numbers);

&#x20;       for (int index = numbers.length - 1; index >= 0; index--) {

&#x20;           System.out.print(numbers\[index] + " ");

&#x20;       }

&#x20;       System.out.println();

&#x20;   }

}

```



\### Question 12



Guess a random number generated by computer. The computer chooses the target once (from 1 to 100) before the guessing loop starts, and each guess is compared with it. The program gives a Higher or Lower hint until the guess is correct, then shows the number of attempts. Guesses outside 1–100 are rejected and not counted.



IPO model:



| Input | Process | Output |

|-------|---------|--------|

| A fixed random target and repeated guesses | Compare guess with target; repeat while unequal | Higher, Lower, or Correct; attempt count |



Pseudocode:



```text

START

target ← RANDOM\_INTEGER(1, 100)

attempts ← 0

REPEAT

&#x20;   READ guess

&#x20;   IF guess < 1 OR guess > 100 THEN

&#x20;       DISPLAY "Enter 1–100"

&#x20;   ELSE

&#x20;       attempts ← attempts + 1

&#x20;       IF guess < target THEN

&#x20;           DISPLAY "Higher"

&#x20;       ELSE IF guess > target THEN

&#x20;           DISPLAY "Lower"

&#x20;       ELSE

&#x20;           DISPLAY "Correct", attempts

&#x20;       END IF

&#x20;   END IF

UNTIL guess = target

STOP

```



Flowchart:



```mermaid

flowchart TD

&#x20;   A(\[Start]) --> B\["Generate target once; attempts = 0"]

&#x20;   B --> C\[/"Read guess"/]

&#x20;   C --> D{"Integer in 1–100?"}

&#x20;   D -->|No| E\[/"Show Enter 1–100"/]

&#x20;   E --> C

&#x20;   D -->|Yes| F\["attempts = attempts + 1"]

&#x20;   F --> G{"guess == target?"}

&#x20;   G -->|Yes| H\[/"Show Correct"/]

&#x20;   H --> I(\[Stop])

&#x20;   G -->|No| J\[/"Compare; show Higher or Lower"/]

&#x20;   J --> C

```



Java code:



```java

import java.util.Locale;

import java.util.Random;

import java.util.Scanner;



public class Exercise12 {

&#x20;   public static void main(String\[] args) {

&#x20;       Scanner keyboard = new Scanner(System.in);

&#x20;       keyboard.useLocale(Locale.US);

&#x20;       Random generator = new Random();

&#x20;       int target = generator.nextInt(1, 101);

&#x20;       int attempts = 0;

&#x20;       int guess;

&#x20;       do {

&#x20;           guess = keyboard.nextInt();

&#x20;           if (guess < 1 || guess > 100) {

&#x20;               System.out.println("Enter 1-100");

&#x20;               continue;

&#x20;           }

&#x20;           attempts++;

&#x20;           if (guess < target) {

&#x20;               System.out.println("Higher");

&#x20;           } else if (guess > target) {

&#x20;               System.out.println("Lower");

&#x20;           } else {

&#x20;               System.out.println("Correct in " + attempts + " attempts");

&#x20;           }

&#x20;       } while (guess != target);

&#x20;   }

}

```

