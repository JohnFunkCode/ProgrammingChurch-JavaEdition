# Programming Church - 2021 JavaEdition
## Overall Goals
The main goal is to expand our ability to build stuf in Java using modern practices for 2021 and have some fun along the way. We've keeping the irreverant 'Programming Church' moniker because we meet on Sunday morning for and there's a whole lot of preaching and teaching going on.   He're is a list of concepts we'll take on:
1. Java language basics
2. OO Design - making the leap to Objects rather than funtions
3. Dependancy Management (package mangement) with Maven and Gradle
4. Spring and Spring boot
5. Enterprise Patterns for Java
  - Source Control
  - CI/CD patterns
6. Enterprise Architecture
  - Databases / schema change management
  - Config management
  - Security
  - End Point Management
  - Messaging Systems
  - Caching patterns
7. Various Cloud Deployments
  - Docker and K8s
  - Azure
  - GCP native
  - Amazon native

# 01/17/2021 First Assignment
- Do all the modules in the [w3schools program Java Tutorial](https://www.w3schools.com/java/default.asp) up to the Java Classes section
- Read [Introdution to the Java Environment](https://www.oreilly.com/library/view/java-in-a/9781492037248/ch01.html)
- Do the first 10 modules of [Mike Dane's Java Programming Language Tutorial](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpPpdR_9IQBUDLjYalvdrGGb)
- Do stage 1 of JetBrains Academy Java material on [Mindsweeper Project](https://hyperskill.org/curriculum)
## Notes from our 1/24/2021 live discussion
- Java Compiler, JVM, and basics of the Classloader and Packages
- Building and running 'hello world' without a package and inside a package - Related Article: [Introduction to Default Package in Java](https://www.educba.com/default-package-in-java/)

# 01/31/2021
## Goals for Today:
- Review progress with [JetBrains Mindsweeper Exercises](https://hyperskill.org/curriculum)
- Move the discussions to [Discord](https://discord.com/) to get low-latency multi-screen shareing capability
- Introduce Object-Oriented design / coding topics

## Notes from 1/31/21 live discussion
* type casting 
  * The example below calculates the slope using int math, then casts it to a double
    * To properly complete the math, we could either cast the scanner ints to doubles, or cast each side of the division to double 
  * When doing math, it's a good idea to avoid int data types becuase division can cause hard to find bugs.

```java
  int x1 = scanner.nextInt();
  int y1 = scanner.nextInt();
  int x2 = scanner.nextInt();
  int y2 = scanner.nextInt();

  double slope = Math.abs(y1 - y2) / Math.abs(x1 - x2);
```
* Object Oriented Programming
  * Passing messages between objects for it to handle the message - don't care how outside the object
  * Diagrams - describe code, use as a plan for writing code, UML (Unified Modeling Language)
    * Sequence diagram
    * Package diagram
    * State diagram
  * Principles of Object Oriented Design - SOLID
    * Single Responsibility - each class should have a single responsibility
    * Open-Closed - open for extension, closed for modification
    * Liskov Substitution Principle - coding to the interface not the base class
    * Interface Segregation - create an Object that's a composite of other Objects
    * Dependency Injection 

## Assignments for next week
- Finish Stage 1 of the  [JetBrains Mindsweeper Exercises](https://hyperskill.org/curriculum) (~3 hours)
- Start Stage 2 of the [JetBrains Mindsweeper Exercises](https://hyperskill.org/curriculum) but stop after the Functional Decomposition module (~1.5 hour)
- Read [An introduction to the Unified Modeling Language](https://developer.ibm.com/articles/an-introduction-to-uml/) (15 minutes)
- Read [Unified Modeling Language: An Introduction](https://www.geeksforgeeks.org/unified-modeling-language-uml-introduction/) and the Recommended articles linked at the bottom of the page. (20 minutes)
- Review [The Five SOLID Principals of Object-Oriented Design](https://www.youtube.com/watch?v=HyQlCMU_Ylw) Video  (15 minutes)
- Read [Design Patterns](https://en.wikipedia.org/wiki/Design_Patterns] article on Wikipiedia (10 minutes)

# 2/7/2021
## Goals for the Week
- Finish Sage 2 of  [JetBrains Academy Mine Sweeper Project](https://hyperskill.org/projects/77?track=1).

# 2/14/2021
## Goals for the Week
- Finish up the [JetBrains Academy ChattyBot Project](https://hyperskill.org/projects/113?track=1).  Finishing it will earn you another month of free time on JetBrains Acadmy
## Assignments for next week
- Finish up the  [JetBrains Academy ChattyBot Project](https://hyperskill.org/projects/113?track=1).

# 2/7/2021
## Goals for the Week
- Discuss plan to move forward with JetBrain Academy even after the free trial period expires.
- Additional projects to tackle include:
  - [Phone Book](https://hyperskill.org/projects/63?track=1) - Algorithm knowledge - 25 hours (Hard)
  - [Encryption-Decryption](https://hyperskill.org/projects/46?track=1) - OO & File Handling - 22 hours (Medium)
  - [Sorting Tool](https://hyperskill.org/projects/45?track=1) - Collection framework, files, exception hiearchy - 30 hours (Hard)
  - [Contacts](https://hyperskill.org/projects/43?track=1) - Polymorphism - 34 hours (Challenging)
  - [Simple Banking](https://hyperskill.org/projects/93?track=1) - SQL - 24 hours (Hard)
  - [Web Quiz Engine](https://hyperskill.org/projects/91?track=1) - Spring Rest - 32 hours (Challenging)
  - [Music Advisor](https://hyperskill.org/projects/62?track=1) - Calling Spoity's API, Generics, Design Patterns - 28 hours (Hard)
  - [Code Sharing Platform](https://hyperskill.org/projects/130?track=1) - Spring Boot, databases, - 33 hours (Challenging)
  - [Game of Life](https://hyperskill.org/projects/54?track=1) - Swing - 26 hours (Hard)
## Assignments for next week
- Start the coding examples in stage 3 and 4 of [JetBrains Academy Mine Sweeper project](https://hyperskill.org/projects/77?track=1).

# 2/14/2021
## Goals for the Week
## Discussion Notes
 We reviewed the Sudoku problem from the [JetBrains Academy Mine Sweeper project](https://hyperskill.org/projects/77?track=1).
<img width="1055" alt="Screen Shot 2021-02-28 at 12 53 00 PM" src="https://user-images.githubusercontent.com/28072589/109432521-d3470880-79c8-11eb-8e19-9fbd20e5c400.png">


  We discussed the code that was in many of the solutions.   The algorithm that seems to be predominant in the solutions on JetBrains Academy is to simply look for any duplicate number in the rows, column, and each mini-square. There was another solution that used an additive checksum algorithm to determine if a row or column matched the business rules.  Below is a sample of the second solution.
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int nsq = n * n; 
        boolean solved = true;
//        The sum of each row, column, and nxn square will be the same in a solved sudoku
        int sum = 0;
        for (int i = nsq; i > 0; i--) {
            sum += i;
        }

        int[][] arr = new int[nsq][nsq];

        // Check row validity while adding data
        for (int col = 0; col < nsq; col++) {
            int rowSum = 0;
            for (int row = 0; row < nsq; row++) {
                arr[col][row] = scanner.nextInt();
                rowSum += arr[col][row];
            }
            if (rowSum != sum) {
                solved = false;
                break;
            }
        }
        
        // flip the row/column loops to calculate columns
        for (int row = 0; row < nsq; row++) {
            int columnSum = 0;
            for (int col = 0; col < nsq; col++) {
                columnSum += arr[col][row];
            }
            if (columnSum != sum) {
                solved = false;
                break;
            }
        }

        // check the nxn squares - use same loops, but incease start place by n
        for (int i = 0; i < nsq; i += n) {
            int squareSum = 0;
            for (int col = i; col < n + i; col++) {
                for (int row = i; row < n + i; row++) {
                    squareSum += arr[col][row];
                }
            }
            if (squareSum != sum) {
                solved = false;
                break;
            }
        }
        
        System.out.println(solved ? "YES" : "NO");
    }
}
```
  Both algorithms are incomplete and fail in-depth verification, setting off alarm bells because neither approach is verifiability correct.  They rely on the fact that if both the rows and the columns passed the check everything was good, although independantly either check is incomplete.   They might generate the needed output for this simple exercise, but in either case it is easy to develop a test case that makes the code fail.  
  Even worse, refering to the additive checksum solution above, there is an implicit dependency between code blocks.  Columns and rows and mini-squares must add up for the code to be correct.  That means checkRows() can return true, but it's really only true if checkColumns() and checkSquares is also true, that introduces a really dangerous logic dependancy between these two code modules.  It's easy enough to write an if statement that says "if( checkRows() && checkColumns) the model is correct".  However if in the future someone tries to re-use checkRows() independently they will find it can't work on it's own.  In big systems those bugs are very difficult to find and fix.   
    As an alternative, we decided it would be better to use TDD and develop several test cases to exercise the code before we wrote a solution.  Those test cases included rows and columns that didn't have duplicates, but failed the sudoku business rules, and rows and columns that passed an additive checksum but failed the sudoku roles due the the communitive property of addition.   In the end our solution was to keep track of the digits we saw in a separate array.   If we saw all the digits we expect know the row or column is correct.

## Assignments for next week
- Continue to work through the coding examples in stage 3 and 4 of [JetBrains Academy Mine Sweeper project)](https://hyperskill.org/projects/77?track=1).
- Read the Java Coding Conventions at: https://www.oracle.com/java/technologies/javase/codeconventions-introduction.html
- Listen to: [Security Now Podcast 807](https://twit.tv/shows/security-now/episodes/807) Dependancy Coversion story at 1:28:30
- Listen to the [Security Now Podcast 807](https://twit.tv/shows/security-now/episodes/807) story on Microsoft's final “Solorigate” update at 50:00.  It emphasized the importance of keeping secrets separate from your code.
[![Security Now Podcast 807](SecurityNow807.png)](https://twit.tv/shows/security-now/episodes/807)

# 3/1/2021
## Goals for the Week
- Discuss coding style
- Discuss recursion vs loops for problem solving
- Discuss the Dependancy Confusion sectin of Security Now 807.  It demonstrate that the industry puts too much trust on external dependancies, and also shows how one creative bounty hunter put dependancy management strategies of today's dynamic languages to work to earn significant payouts from several bug bounty programs.
- Discuss the story on Microsoft's final “Solorigate” update at 50:00 of Security Now 807.  It emphasized the importance of keeping secrets separate from your code.
- Review Interesting coding issues that came up in this weeks exercises from JetBrains Academy Mine Sweeper project.
## Discussion Notes
### Random Topics:
- [Lithium Ion Car Jumpstarters](https://www.amazon.com/s?k=car+jump+starter&i=automotive&ref=nb_sb_noss_1) are a great way to jumpstart cars in winter.  They also make great general use portable power packs for all sorts of purposes.
- Gaming Headphones for Remote Pairing - [The Sennheiser Gaming Headset](https://www.amazon.com/Sennheiser-GAME-Gaming-Headset-Black/dp/B00KNPYAEY/ref=sr_1_3?crid=2194G9CC7H1R9&dchild=1&keywords=senhiesers+headphones+gaming&qid=1614535781&s=electronics&sprefix=senh%2Celectronics%2C208&sr=1-3) is the most popular among John's collegues.
- Work From Home Desk Enhancements - John's latest addition to his WFH office is an [adjustable vesa arm mounting system](https://www.amazon.com/gp/product/B086W3L2XB/ref=ppx_yo_dt_b_asin_title_o08_s01?ie=UTF8&psc=1) to hold his laptop, monitor, and other accessories.
![Viozon vesa arm mount system](https://images-na.ssl-images-amazon.com/images/I/61n%2BYzdSCPL._AC_SL1500_.jpg)

## Assignments for next week
- Continue to work through the coding examples in stage 3 and 4 of [JetBrains Academy Mine Sweeper Project](https://hyperskill.org/projects/77?track=1).
- Listen to the [Computerphile episode on Programming Loops vs Recursion](https://www.youtube.com/watch?v=HXNhEYqFo0o)
[![Programming Loops vs Recursion](ProgrammingLoopsvsRecursion-Computerphile.png)](https://www.youtube.com/watch?v=HXNhEYqFo0o)

# 3/7/2021
## Goals for the Week
- Review Interesting coding issues that came up in this weeks exercises from JetBrains Academy Mine Sweeper project.
## Discussion Notes
  This week we concentrated on the following problem taken from [JetBrains Academy Mine Sweeper Project](https://hyperskill.org/projects/77?track=1) titled "ArrayList - Find the nearest number"
<img width="1094" alt="Screen Shot 2021-03-09 at 9 08 57 PM" src="https://user-images.githubusercontent.com/28072589/110575198-bb375d80-811b-11eb-8ff0-16fb3fc5c173.png">
  One approach we liked is shown in code below. We've included only the main functionality for sake of brevity. After recording the inputs (variables `list` and `value`), we create a second array, `distanceFromValue` recording the absolute difference between the array value and the target number.  We considered, instead of creating a separate array, utilizing a custom class that contained both the original value and the difference value as the basis of the new list as separate lists have the possiblity of getting out of sync. 
  Next in our solution we identify the minimum difference value. Finally, we store any and all original values that correspond in an output array, `nearest`, sorting `nearest` before printing as asked.  
  An immediately noticeable refactor that would improve readability would be to use `Collections.sort` since we are comparing `int` values, a common sort that doesn't require a special comparison function.

```java
private static ArrayList<Integer> getNearestNumbers(ArrayList<Integer> list, int value) {
    ArrayList<Integer> distanceFromValue = new ArrayList<>(list);
    for (int i = 0; i < distanceFromValue.size(); i++) {
        distanceFromValue.set(i, Math.abs(list.get(i) - value));
    }

    Optional<Integer> min = distanceFromValue.stream().min(Comparator.comparing(Integer::intValue));

    ArrayList<Integer> nearest = new ArrayList<>();
    for (int i = 0; i < distanceFromValue.size(); i++) {
        if (distanceFromValue.get(i).equals(min.get())) {
            nearest.add(list.get(i));
        }
    }
    nearest.sort(Comparator.comparing(Integer::intValue));
    return nearest;
  }
```

  This solution is serviceable but we found and discussed a nice solution posted by user "Lazar" shown in full below.  Lazar posted 2 solutions, which allowed us to see thier optimization technique. They started off similar to our solution, creating a new output array and adding the original value if it matched a calculated minimum difference value.  Neither solution recorded the difference values, prefering a temporary variable the first time around and the map you see below the second.  Note in the below solution, Lazar sets `minArrayValue` to 0 if a minimum isn't found which more accuratly reflects the required business logic than the unhandled `Optional<Integer>` above. 

```java
import java.util.*;
import java.util.stream.Collectors;

public class Main {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        ArrayList<Integer> numbersList = Arrays.stream(scanner.nextLine().split("\\s"))
                .map(Integer::parseInt)
                .sorted()
                .collect(Collectors.toCollection(ArrayList::new));

        int num = scanner.nextInt();

        int minArrayValue = numbersList.stream()
                .mapToInt(n -> Math.abs(n - num))
                .min().orElse(0);

        numbersList.forEach(n -> {
            if (Math.abs(n - num) == minArrayValue) {
                System.out.print(n + " ");
            }
        });
    }
}
```

## Assignments for next week
- Continue to work through the coding examples in stage 3 and 4 of [JetBrains Academy Mine Sweeper Project](https://hyperskill.org/projects/77?track=1).

