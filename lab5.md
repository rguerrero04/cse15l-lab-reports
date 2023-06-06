# Lab Report 5
[Student Submission]\
**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?**\
I am using a Linux computer with Ubuntu 20.04, Java 11, and the OpenJDK compiler.

**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying "it doesn't work".**\
I wrote a program to calculate the sum of numbers from 1 to n, but I'm getting an unexpected output. Instead of the correct sum, I'm getting a negative value.

**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.**\
Here's the relevant code snippet from my Java program:
```java
public class Summation {
    public static void main(String[] args) {
        int n = 100;
        int sum = 0;
        
        for (int i = 1; i <= n; i++) {
            sum += i;
        }
        
        System.out.println("The sum is: " + sum);
    }
}
```
I expected the program to calculate the sum of numbers from 1 to 100 and print the result, which should be 5050. However, I'm getting a negative value as the output.\

**[TA's Response]**

TA: Hi there! I noticed that you are using an int variable to store the sum. The issue you're experiencing might be related to integer overflow. When the sum of the numbers exceeds the maximum value that an int can hold, it wraps around and becomes negative. One way to solve this issue is to use a larger data type to store the sum.

Could you try changing the int data type for the sum variable to long and run the program again? This should prevent the overflow issue.

Let me know if that helps!

**[Student's Follow-up Post]**

Title: Summation Bug - Unexpected Output (Follow-up)

Symptom: I followed your suggestion and changed the data type of the sum variable from int to long. However, I'm still getting a negative value as the output.

After making the suggested change, I expected the issue to be resolved. However, I'm still getting a negative value as the output. This suggests that the bug might be caused by something else.
```java
public class Summation {
    public static void main(String[] args) {
        int n = 100;
        long sum = 0;
        
        for (int i = 1; i <= n; i++) {
            sum += i;
        }
        
        System.out.println("The sum is: " + sum);
    }
}
```

## Setup Information

File & Directory Structure:

* Summation.java: The Java source code file containing the program.

**Contents of Summation.java before fixing the bug:**
```java
public class Summation {
    public static void main(String[] args) {
        int n = 100;
        long sum = 0;
        
        for (int i = 1; i <= n; i++) {
            sum += i;
        }
        
        System.out.println("The sum is: " + sum);
    }
}
```

**Full Command Line:**
```bash
javac Summation.java
java Summation
```

**Bug Fix:**

To fix the bug and avoid the negative value issue, we need to update the loop termination condition in the for loop. Instead of i <= n, we should use i < n to ensure that the loop stops when i becomes equal to n.

Here's the corrected code:
```java
public class Summation {
    public static void main(String[] args) {
        int n = 100;
        long sum = 0;
        
        for (int i = 1; i < n; i++) {
            sum += i;
        }
        
        System.out.println("The sum is: " + sum);
    }
}
```
After applying this fix, the program should correctly calculate the sum of numbers from 1 to 100 without producing a negative value.

## Reflection
Something that I learned while in lab is the use of remote access which was a very beneficial tool for conducting work on other computers. The added skills learned from bash and the use of the command line was also a plus in the course it has helped in CSE 12. Especially with the use of VIM which I heard would be beneficiary for the next course on my path CSE 30! Overall, this class has greatly been beneficial on the skils that most likely would have never been taught to me to later on in the industry.
