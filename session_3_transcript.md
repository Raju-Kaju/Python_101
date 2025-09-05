# Session 3: Getting User Input
**Duration:** 60 minutes  
**Learning Goals:** Make programs interactive  
**Materials Needed:** Computers, notebooks, sample programs for demonstration

---

## Opening Review and Hook (5 minutes)

**Teacher:** Welcome back! Let's start by checking out some of your "favorites" homework. Who created a program they're proud of?

*[Have 2-3 students share their favorites programs]*

**Teacher:** Nice work! I noticed everyone's programs displayed the same information every time you ran them. Sarah's program always says her favorite color is purple, Mike's always says his favorite number is 7. But what if we wanted to make a program that could work for anyone?

*[Demonstrate the limitation by running a sample program]:*
```python
name = "Teacher Example"
favorite_color = "blue"
print("Hello", name)
print("Your favorite color is", favorite_color)
```

**Teacher:** This program only works for one person. But what if I wanted to create a program that could ask YOU what your favorite color is, then display YOUR answer? What if the program could have a conversation with whoever is using it?

**Teacher:** That's exactly what we're learning today - how to make our programs **interactive**. By the end of class, you'll create programs that can talk to any user and respond to their answers!

---

## Introduction to User Input (12 minutes)

**Teacher:** The key to interactive programs is getting **input** from the user. In Python, we use a special function called `input()` to ask questions and get answers.

*[Write on board: "input() - Gets information from the user"]*

**Teacher:** Let me show you the most basic example:

*[Type on projector while students watch]:*
```python
name = input("What is your name? ")
print("Hello", name)
```

**Teacher:** Let's run this together. When I click run, watch what happens...

*[Run the program, demonstrate typing in a response]*

**Teacher:** See what happened? The program paused and waited for me to type something! When I pressed Enter, it stored my answer in the variable `name` and then used it.

**Teacher:** Everyone try this now. Create a new file called "interactive_hello" and type that exact code. Then run it and see what happens!

*[Give students time to try this, circulate and help]*

**Teacher:** Awesome! Let's break down what just happened:

1. `input("What is your name? ")` does two things:
   - Displays the question "What is your name? "
   - Waits for the user to type an answer and press Enter
   - Returns whatever the user typed

2. `name =` stores the user's answer in a variable

3. `print("Hello", name)` uses that stored answer

**Teacher:** The text inside the `input()` function is called a **prompt** - it tells the user what to type.

**Teacher:** Let's make this more interesting. Add a second line to your program:

```python
name = input("What is your name? ")
age = input("How old are you? ")
print("Hello", name)
print("You are", age, "years old!")
```

**Teacher:** Run this new version. Notice how the program asks two questions in order, then uses both answers!

### **Important Discovery: Everything is Text!**

**Teacher:** Here's something crucial to understand. Let me ask someone to run their program and enter their age as a number... 

*[Have a student demonstrate]*

**Teacher:** Now, here's a question: Is the age stored as a number or as text? Let's find out with an experiment:

```python
name = input("What is your name? ")
age = input("How old are you? ")
print("Hello", name)
print("Next year you will be", age + 1, "years old")
```

**Teacher:** Everyone try adding that last line to your program. What happens when you run it?

*[Students will get an error]*

**Teacher:** You got an error! The error message probably says something like "can't concatenate str and int". This is Python telling us that `age` is stored as text (a string), not as a number, so we can't add 1 to it.

**Teacher:** **Key point:** The `input()` function ALWAYS gives us text, even if the user types a number.

---

## Converting Input to Numbers (10 minutes)

**Teacher:** So how do we fix this? We need to convert the text to a number. Python gives us special functions for this:

*[Write on board]:*
- `int()` - converts to integer (whole number)
- `float()` - converts to decimal number
- `str()` - converts to text (string)

**Teacher:** Let's fix our program:

```python
name = input("What is your name? ")
age_text = input("How old are you? ")
age = int(age_text)
print("Hello", name)
print("You are", age, "years old")
print("Next year you will be", age + 1, "years old")
```

**Teacher:** Or we can do it in one line:

```python
name = input("What is your name? ")
age = int(input("How old are you? "))
print("Hello", name)
print("You are", age, "years old")
print("Next year you will be", age + 1, "years old")
```

**Teacher:** Everyone try the second version. Now it should work!

*[Give students time to test this]*

**Teacher:** Perfect! Now let's try with decimals:

```python
name = input("What is your name? ")
height = float(input("How tall are you in feet? "))
print("Hello", name)
print("You are", height, "feet tall")
print("That's", height * 12, "inches!")
```

**Teacher:** Try this version. Enter your height with a decimal, like 5.5 or 6.2.

### **What Happens if Someone Types Wrong?**

**Teacher:** What do you think happens if someone types "five" instead of "5" when we're expecting a number?

*[Demonstrate this error deliberately]*

**Teacher:** We get an error! For now, we'll assume users type the right kind of information. Later in the course, we'll learn how to handle these errors gracefully.

---

## Hands-On Activity: Personal Profile Generator (15 minutes)

**Teacher:** Now let's create something more substantial. We're going to make a program that asks several questions and creates a complete profile. 

**Teacher:** Start a new file called "profile_generator". Here's our plan:

1. Ask for the user's name
2. Ask for their age (as a number)
3. Ask for their favorite color
4. Ask for their favorite food
5. Ask for their favorite number (as a number)
6. Display a nice profile with some calculations

**Teacher:** Here's the template to get you started:

```python
# Personal Profile Generator
print("Welcome to the Personal Profile Generator!")
print("Please answer the following questions:")
print()  # This prints a blank line

# Get user information
name = input("What is your name? ")
age = int(input("How old are you? "))
favorite_color = input("What is your favorite color? ")
favorite_food = input("What is your favorite food? ")
favorite_number = int(input("What is your favorite number? "))

# Display the profile
print()
print("=" * 40)
print("       PERSONAL PROFILE")
print("=" * 40)
print("Name:", name)
print("Age:", age, "years old")
print("Favorite Color:", favorite_color)
print("Favorite Food:", favorite_food)
print("Favorite Number:", favorite_number)
print()
print("Fun Facts:")
print("- In 10 years, you'll be", age + 10, "years old")
print("- Your favorite number doubled is", favorite_number * 2)
print("- Your name has", len(name), "letters")
print("=" * 40)
```

**Teacher:** Type this carefully. Notice a few new things:
- `print()` with nothing inside prints a blank line for spacing
- `len(name)` tells us how many characters are in the name
- We're doing math with the numbers we collected

*[Give students 10-12 minutes to type and test this]*

**Teacher:** Test your program with different inputs. Try it with your own information, then try pretending to be someone else!

*[Circulate and help students debug]*

---

## Creative Challenge: Simple Calculator (10 minutes)

**Teacher:** For those who finish early, or as our next activity, let's create a simple calculator that asks the user for two numbers and performs some calculations.

```python
# Simple Calculator
print("Welcome to the Simple Calculator!")

# Get two numbers from user
first_number = float(input("Enter your first number: "))
second_number = float(input("Enter your second number: "))

# Perform calculations
sum_result = first_number + second_number
difference = first_number - second_number
product = first_number * second_number
quotient = first_number / second_number

# Display results
print()
print("Results:")
print(first_number, "+", second_number, "=", sum_result)
print(first_number, "-", second_number, "=", difference)
print(first_number, "*", second_number, "=", product)
print(first_number, "/", second_number, "=", quotient)
```

**Teacher:** Notice that I used `float()` instead of `int()` for the numbers. Why do you think that is?

*[Wait for responses - because we might want to do division or use decimal numbers]*

**Teacher:** Exactly! Using `float()` lets us work with any kind of number.

*[Give students time to create and test the calculator]*

---

## Common Mistakes and Debugging (5 minutes)

**Teacher:** Let's talk about some common mistakes I've seen today:

### **Mistake 1: Forgetting to Convert Numbers**
```python
age = input("How old are you? ")
next_year = age + 1  # ❌ Error! Can't add number to text
```

**Fix:**
```python
age = int(input("How old are you? "))
next_year = age + 1  # ✅ Works! Both are numbers
```

### **Mistake 2: Converting When You Don't Need To**
```python
name = int(input("What is your name? "))  # ❌ Names aren't numbers!
```

**Fix:**
```python
name = input("What is your name? ")  # ✅ Names are text
```

### **Mistake 3: Forgetting the Prompt Message**
```python
name = input()  # This works, but users don't know what to type
```

**Better:**
```python
name = input("Please enter your name: ")  # Clear instruction
```

**Teacher:** **Quick Rule:** If you need to do math with the input, convert it to a number. If it's just text to display, leave it as a string.

---

## Program Showcase and Wrap-up (3 minutes)

**Teacher:** Let's see some of your creations! Who wants to run their profile generator for the class?

*[Have 2-3 students demonstrate their programs with different inputs]*

**Teacher:** Excellent! Look how much more powerful your programs are now. Instead of only working for one person, they work for anyone!

**Teacher:** Let's review what we learned today:

*[Write on board as we review]:*

1. **input()** - Gets text from the user
2. **int()** - Converts text to whole numbers
3. **float()** - Converts text to decimal numbers
4. **Interactive programs** - Programs that respond to user input
5. **Always include clear prompts** - Tell users what to type

**Teacher:** For homework, create an "About Me" questionnaire program that:
- Asks at least 5 questions (mix of text and numbers)
- Performs at least 2 calculations with the numbers
- Displays the results in a nice format
- Be creative! Maybe calculate how many days old someone is, or what year they were born

**Teacher:** Next class, we'll learn about **string operations** - cool ways to manipulate and format text, including making text uppercase, lowercase, and combining strings in clever ways.

**Teacher:** Any questions about input, conversion, or today's homework?

*[Address final questions]*

**Teacher:** Fantastic work making your first interactive programs! You're becoming real programmers now!

---

## Teacher Notes for Session 3

### **Common Student Questions & Answers:**
- **"Why do I need to convert numbers?"** Because input() always gives text. Python can't do math with text that looks like numbers.
- **"What if someone types the wrong thing?"** Right now we assume correct input. Later we'll learn error handling.
- **"Can I ask the same question multiple times?"** Yes! Each input() call asks a new question.
- **"What's the difference between int() and float()?"** int() is for whole numbers only, float() can handle decimals.

### **Extension Activities for Fast Finishers:**
- Create a program that asks for someone's birth year and calculates their age
- Make a "favorites comparison" program that asks two people the same questions
- Build a simple unit converter (feet to inches, Celsius to Fahrenheit)
- Create a program that asks for dimensions and calculates area

### **Assessment Checkpoints:**
- [ ] Student can use input() function with clear prompts
- [ ] Student understands the difference between text input and converted numbers
- [ ] Student can use int() and float() conversions appropriately
- [ ] Student can combine input with variables and calculations
- [ ] Student can create a complete interactive program

### **Common Errors to Watch For:**
- Trying to do math with unconverted input strings
- Converting text inputs that should stay as text
- Forgetting prompt messages in input() functions
- Syntax errors in conversion functions: `int(input("question"))` not `int input("question")`
- Not understanding that input() pauses program execution

### **Differentiation Strategies:**
- **For struggling students:** Provide step-by-step conversion examples, use pair programming
- **For advanced students:** Challenge them to create programs with multiple calculations and formatting
- **For visual learners:** Draw diagrams showing input → conversion → calculation → output flow

### **Preparation for Next Session:**
- Review string methods (.upper(), .lower(), .strip(), .replace())
- Prepare examples of string formatting and f-strings
- Have examples ready of practical string manipulation uses
- Consider preparing a mad libs template for the main activity

### **Materials to Prepare for Next Session:**
- Examples of string methods in action
- Mad libs templates or story frameworks
- Demonstration of practical string formatting uses
- Reference sheet of common string operations

### **Troubleshooting Tips for Teachers:**
- If students get "invalid literal" errors, check that they're typing numbers when prompted for numbers
- Watch for students forgetting parentheses in conversion functions
- Be ready to explain the difference between "5" (text) and 5 (number)
- Have backup simple examples ready for students who struggle with the concepts