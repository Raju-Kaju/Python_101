# Session 2: Variables and Basic Data Types
**Duration:** 60 minutes  
**Learning Goals:** Store and manipulate different types of data  
**Materials Needed:** Computers, notebooks, sticky notes (optional for variable analogy)

---

## Opening Review and Hook (5 minutes)

**Teacher:** Welcome back, programmers! Before we dive into new material, let's quickly review. Who can tell me what this code does?

*[Write on board]:*
```python
print("Hello, Python!")
```

*[Wait for responses - "displays Hello, Python!"]*

**Teacher:** Perfect! And what do we call the text inside the quotation marks?

*[Wait for "string"]*

**Teacher:** Excellent! Now, let's look at some homework. Who wants to share one creative line from their expanded introduction program?

*[Have 2-3 students share a creative print statement from their homework]*

**Teacher:** Great work! Now, I have a question that might seem odd: What if I told you that every time you wanted to use your name in a program, you had to type it out completely each time? And if you ever wanted to change it, you'd have to find every single place you used it and change each one individually?

*[Demonstrate the problem by writing repetitive code on board]:*
```python
print("My name is Alexander")
print("Alexander is 15 years old")
print("Alexander likes pizza")
print("Nice to meet you, Alexander!")
```

**Teacher:** That's a lot of typing! And what if I wanted to change "Alexander" to "Alex"? I'd have to change it in four places! There must be a better way... and there is! Today we're learning about **variables**.

---

## What are Variables? (10 minutes)

**Teacher:** Variables are like labeled boxes where we can store information. Once we put something in the box and give it a label, we can use that label whenever we need what's inside.

*[Optional: Use physical boxes/containers with labels if available, or draw on board]*

**Teacher:** Let me show you how this works in Python:

*[Type on projector while students watch]:*
```python
name = "Alexander"
print(name)
```

**Teacher:** Run this code with me. What happened? It printed "Alexander" even though we didn't put "Alexander" directly in the print statement!

**Teacher:** Let's break this down:
- `name` is our **variable name** (the label on our box)
- `=` is the **assignment operator** (it puts something in the box)
- `"Alexander"` is the **value** (what goes in the box)
- When we write `print(name)`, Python looks in the box labeled "name" and uses what's inside

**Teacher:** The magic happens when we want to use "Alexander" multiple times:

```python
name = "Alexander"
print("My name is", name)
print(name, "is 15 years old")
print(name, "likes pizza")
print("Nice to meet you,", name)
```

**Teacher:** Notice something cool? When we use commas in print statements, Python automatically adds spaces between the parts. And if we want to change the name, we only change it in one place!

**Teacher:** Let's try it. Everyone open your Replit from last time or create a new file called "variables_practice". Type the code exactly as I show you:

```python
name = "Your_Name_Here"
print("Hello, my name is", name)
print(name, "is learning Python!")
```

**Teacher:** Replace "Your_Name_Here" with your actual name, keeping the quotation marks. Run your program!

*[Circulate and help students]*

---

## Different Types of Data (15 minutes)

**Teacher:** Variables can hold different types of information. In our name example, we stored text (a **string**). But variables can also store numbers and other types of data.

*[Write on board: "Data Types"]*

### **Strings (Text)**
**Teacher:** We've already seen strings. They're always wrapped in quotation marks:

```python
favorite_color = "blue"
favorite_movie = "Spider-Man"
```

### **Integers (Whole Numbers)**
**Teacher:** Integers are whole numbers - no decimal points, no quotation marks:

```python
age = 15
number_of_pets = 2
favorite_number = 42
```

### **Floats (Decimal Numbers)**
**Teacher:** Floats have decimal points:

```python
height = 5.5
gpa = 3.75
temperature = 98.6
```

**Teacher:** Let's practice with all three types. Everyone create a new program:

```python
# This is a comment - it doesn't run, it's just notes for us
name = "Alex"           # String
age = 16               # Integer  
height = 5.8           # Float

print("Name:", name)
print("Age:", age)
print("Height:", height, "feet")
```

**Teacher:** Type this exactly, including the comments (the lines starting with #). Comments help us remember what our code does.

*[Give students time to type and run]*

**Teacher:** What do you notice about how Python displays the different types? 
- Strings appear exactly as we typed them
- Numbers appear without quotation marks
- We can mix them in print statements

**Important Note:**
**Teacher:** Here's something crucial - look at these two variables:

```python
age_as_number = 16      # This is a number
age_as_text = "16"      # This is text
```

**Teacher:** They look similar, but they're completely different! We can do math with the first one but not the second. We'll explore this more in future classes.

---

## Variable Naming Rules and Best Practices (8 minutes)

**Teacher:** Just like we have rules for naming pets or choosing usernames, Python has rules for naming variables.

*[Write on board as we go through each rule]:*

### **Rules (Must Follow These):**
1. **Start with a letter or underscore** (not a number)
   - ✅ `name`, `_secret`, `age`
   - ❌ `2cool`, `9lives`

2. **Only use letters, numbers, and underscores**
   - ✅ `first_name`, `player1`, `high_score`
   - ❌ `first-name`, `player#1`, `high score`

3. **No spaces allowed**
   - ✅ `favorite_food`, `best_friend`
   - ❌ `favorite food`, `best friend`

4. **Case sensitive** (Python treats these as different variables)
   - `Name` ≠ `name` ≠ `NAME`

### **Best Practices (Should Follow These):**
1. **Use descriptive names**
   - ✅ `student_grade`, `favorite_color`
   - ❌ `x`, `thing`, `stuff`

2. **Use lowercase with underscores**
   - ✅ `first_name`, `high_score`
   - ❌ `FirstName`, `highScore`

3. **Avoid Python keywords** (words Python uses for other things)
   - ❌ `print`, `if`, `for` (we'll learn about these later)

**Teacher:** Let's practice! I'll show you some variable names, and you tell me if they're valid:

*[Show on board, have students respond]:*
- `my_age` (✅ Valid and good)
- `2cool` (❌ Starts with number)
- `favorite-movie` (❌ Has dash)
- `FavoriteMovie` (✅ Valid but not best practice)
- `favorite_movie` (✅ Valid and follows best practices)

---

## Hands-On Activity: Digital Business Card (15 minutes)

**Teacher:** Now we're going to create a digital business card using variables. This will store all your information in variables first, then display it nicely.

**Teacher:** Here's the template - everyone start a new file called "business_card":

```python
# My Digital Business Card
# Store information in variables first

name = "Your Name"
age = 16
grade = "10th"
school = "Your School Name"
favorite_subject = "Your Subject"
hobby = "Your Hobby"
fun_fact = "Something interesting about you"

# Now display the business card
print("=" * 30)
print("    DIGITAL BUSINESS CARD")
print("=" * 30)
print("Name:", name)
print("Age:", age, "years old")
print("Grade:", grade)
print("School:", school)
print("Favorite Subject:", favorite_subject)
print("Hobby:", hobby)
print("Fun Fact:", fun_fact)
print("=" * 30)
```

**Teacher:** Fill in your actual information, replacing the placeholder text. Keep the quotation marks around text, but not around your age (that should be a number).

*[Give students 8-10 minutes to complete this]*

**Teacher:** As you work, notice a few cool things:
- `"=" * 30` creates a line of 30 equal signs - Python can multiply strings!
- We store everything in variables first, then use the variables in our print statements
- This makes it easy to update - if you change schools, you only need to change one line

**Teacher:** Who wants to run their business card and share it with the class?

*[Have 3-4 students share their business cards]*

---

## Troubleshooting Common Mistakes (5 minutes)

**Teacher:** Let's look at some common mistakes I saw as I walked around:

### **Mistake 1: Forgetting Quotes Around Text**
```python
name = Alexander    # ❌ Wrong - Python thinks Alexander is a variable
name = "Alexander"  # ✅ Correct - This is text
```

### **Mistake 2: Quotes Around Numbers**
```python
age = "16"     # This makes age text, not a number
age = 16       # This makes age a number we can do math with
```

### **Mistake 3: Misspelling Variable Names**
```python
name = "Alex"
print(nam)     # ❌ Error! 'nam' doesn't exist
```

**Teacher:** Python error messages might seem scary, but they're actually helpful! If you get an error, read it carefully - it usually tells you exactly what's wrong.

**Quick Practice:** Everyone try this deliberately wrong code to see the error message:
```python
name = "Alex"
print(nome)
```

**Teacher:** See how Python tells you "name 'nome' is not defined"? That's Python's way of saying "I don't know what 'nome' is - did you mean 'name'?"

---

## Wrap-up and Looking Ahead (2 minutes)

**Teacher:** Excellent work today! Let's review what we learned:

*[Write on board as we review]:*

1. **Variables** = labeled boxes that store information
2. **Three data types:**
   - **Strings** = text in quotation marks
   - **Integers** = whole numbers
   - **Floats** = decimal numbers
3. **Variable naming rules** and best practices
4. **Assignment operator** (=) puts values into variables

**Teacher:** For homework, create a "favorites" program that stores and displays:
- Your favorite color
- Your favorite number (as a number, not text)
- Your favorite food
- Your favorite season
- Your favorite time of day (like "morning" or "evening")

Use the business card format as inspiration, but make it your own!

**Teacher:** Next class, we'll learn how to make our programs interactive by getting input from users. Instead of us typing the information into our code, we'll ask the user to type it when the program runs!

**Teacher:** Any questions about variables or today's homework?

*[Address final questions]*

**Teacher:** Great job becoming more sophisticated programmers today! See you next time!

---

## Teacher Notes for Session 2

### **Common Student Questions & Answers:**
- **"Can I use spaces in variable names?"** No, use underscores instead: `first_name` not `first name`
- **"What happens if I forget quotes around text?"** Python will think it's a variable name and give you an error if that variable doesn't exist
- **"Can I change a variable after I create it?"** Yes! Just assign it a new value: `name = "Alex"` then later `name = "Alexander"`
- **"Why do we need different data types?"** Different types let us do different things - we can do math with numbers but not with text

### **Extension Activities for Fast Finishers:**
- Create a business card for a fictional character
- Try using the multiplication trick with other characters: `"-" * 20`, `"*" * 15`
- Research what happens when you try to do math with strings
- Create variables for family members' information

### **Assessment Checkpoints:**
- [ ] Student can create variables with appropriate names
- [ ] Student understands difference between strings, integers, and floats
- [ ] Student can use variables in print statements
- [ ] Student follows variable naming conventions
- [ ] Student can debug simple variable-related errors

### **Common Errors to Watch For:**
- Forgetting quotes around strings
- Adding quotes around numbers
- Using spaces or hyphens in variable names
- Misspelling variable names when using them
- Mixing up assignment (=) with comparison (==, which we'll learn later)

### **Differentiation Strategies:**
- **For struggling students:** Provide a checklist of variable naming rules, work in pairs
- **For advanced students:** Challenge them to create nested information (like variables for multiple family members)
- **For visual learners:** Use box-and-label diagrams to explain variable storage

### **Preparation for Next Session:**
- Review input() function and string conversion
- Prepare examples showing difference between input as text vs. numbers
- Have troubleshooting examples ready for common input() mistakes
- Consider preparing a simple interaction demo to hook students

### **Materials to Prepare for Next Session:**
- Examples of interactive programs (calculator, questionnaire)
- Demonstration of input() function
- Common conversion functions (int(), float(), str())
- Real-world examples of user input (ATMs, online forms, games)