# Session 5: Unit 1 Review and Mini-Project
**Duration:** 60 minutes  
**Learning Goals:** Consolidate foundational concepts through review and project work  
**Materials Needed:** Computers, notebooks, project planning sheets, peer review forms

---

## Opening and Unit 1 Celebration (5 minutes)

**Teacher:** Welcome back, everyone! Before we start today, I want you to think back to Session 1. Remember when printing "Hello, World!" felt like a big accomplishment? 

*[Show Session 1's simple program on screen]:*
```python
print("Hello, World!")
```

**Teacher:** Now look at what you created for homework - story generators with user input, string formatting, and complex interactions! Let's see a few examples.

*[Have 2-3 students share their story generator homework briefly]*

**Teacher:** Amazing progress! In just four sessions, you've learned:
- **Variables** - storing and organizing data
- **User input** - making programs interactive  
- **String manipulation** - professional text formatting
- **F-strings** - elegant output formatting

**Teacher:** Today we're going to solidify these skills through review activities and then create a comprehensive project that shows off everything you've learned. By the end of class, you'll have a portfolio piece that demonstrates your mastery of Python fundamentals!

---

## Rapid Review Game: "Debug the Code" (15 minutes)

**Teacher:** Let's start with a fun review activity. I'm going to show you programs with mistakes, and you need to identify and fix them. We'll work through these together.

*[Display each problem on screen, have students identify issues]*

### **Problem 1: Variable Confusion**
```python
Name = input("What is your name? ")
age = int(input("How old are you? "))
print(f"Hello {name}, you are {age} years old")
```

**Teacher:** What's wrong with this code? Talk to the person next to you for 30 seconds.

*[Wait for discussion, then get answers]*

**Teacher:** Right! Two issues:
1. Variable is defined as `Name` (capital N) but used as `name` (lowercase)
2. Python is case-sensitive, so these are different variables

**Fix:**
```python
name = input("What is your name? ")  # Use consistent lowercase
age = int(input("How old are you? "))
print(f"Hello {name}, you are {age} years old")
```

### **Problem 2: String vs Number Confusion**
```python
age = input("How old are you? ")
print(f"Next year you'll be {age + 1} years old")
```

**Teacher:** What's the issue here?

*[Get student responses]*

**Teacher:** Exactly! We're trying to add a number to text. Input always gives us strings.

**Fix:**
```python
age = int(input("How old are you? "))
print(f"Next year you'll be {age + 1} years old")
```

### **Problem 3: F-string Syntax**
```python
name = "Sarah"
age = 16
print("Hello {name}, you are {age} years old")
```

**Teacher:** This looks almost right... what's missing?

*[Student responses]*

**Teacher:** Missing the `f` before the string! Without it, Python treats `{name}` as literal text.

**Fix:**
```python
name = "Sarah"
age = 16
print(f"Hello {name}, you are {age} years old")
```

### **Problem 4: String Method Confusion**
```python
name = "  SARAH JOHNSON  "
print(name.strip.title())
```

**Teacher:** What's wrong here?

*[Student responses]*

**Teacher:** Missing parentheses after `strip`! Methods need parentheses to work.

**Fix:**
```python
name = "  SARAH JOHNSON  "
print(name.strip().title())  # Method chaining with correct syntax
```

**Teacher:** Great job identifying these common mistakes! Recognizing and fixing errors is a crucial programming skill.

---

## Concept Integration Challenge (10 minutes)

**Teacher:** Now let's practice combining all our concepts. I'll give you a challenge, and you have 8 minutes to solve it.

**Challenge:** Create a program that:
1. Asks for the user's first name and last name separately
2. Asks for their birth year (as a number)
3. Asks for their favorite hobby
4. Calculates their approximate age (2025 - birth year)
5. Displays a formatted profile using proper string formatting

**Teacher:** Here's what the output should look like:

```
================================
        USER PROFILE
================================
Name: Sarah Johnson
Age: Approximately 16 years old
Hobby: Reading
Fun Fact: Sarah has been alive for about 5840 days!
================================
```

**Teacher:** Work individually first, then check with a partner. Use everything we've learned!

*[Give students 8 minutes to work on this, circulate and help]*

**Teacher:** Time's up! Let's see a solution:

*[Show solution on screen]:*
```python
# User Profile Generator - Solution
print("Let's create your profile!")

first_name = input("Enter your first name: ").strip().title()
last_name = input("Enter your last name: ").strip().title()
birth_year = int(input("What year were you born? "))
hobby = input("What's your favorite hobby? ").strip().lower()

age = 2025 - birth_year
days_alive = age * 365  # Approximate

print()
print("=" * 32)
print("        USER PROFILE")
print("=" * 32)
print(f"Name: {first_name} {last_name}")
print(f"Age: Approximately {age} years old")
print(f"Hobby: {hobby.title()}")
print(f"Fun Fact: {first_name} has been alive for about {days_alive} days!")
print("=" * 32)
```

**Teacher:** How did everyone do? This program combines variables, input, conversion, string methods, f-strings, and calculations!

---

## Mini-Project Introduction: Personal Introduction Program (25 minutes)

**Teacher:** Now for our main project! You're going to create a comprehensive "Personal Introduction Program" that showcases all your Unit 1 skills.

**Project Requirements:**
*[Write on board and provide as handout]*

### **Your program must:**
1. **Collect information** using input() with clear prompts:
   - Personal info (name, age, grade/school)
   - Preferences (favorite color, food, hobby, etc.)
   - At least one numeric input for calculations

2. **Process the data** using:
   - Appropriate string methods (.strip(), .title(), etc.)
   - At least 2 calculations with numeric inputs
   - Proper data type conversions

3. **Display results** with:
   - Professional formatting using f-strings
   - Clear sections or headers
   - At least one "fun fact" generated from calculations
   - Proper spacing and visual organization

4. **Handle edge cases:**
   - Clean messy input (extra spaces, wrong capitalization)
   - Include helpful prompts for users

### **Bonus Features (Optional):**
- Create ASCII art borders
- Include multiple calculation-based "fun facts"
- Add input validation hints
- Create a themed version (sports, music, etc.)

### **Project Planning (5 minutes)**
**Teacher:** Before coding, spend 5 minutes planning:

1. What information will you collect?
2. What calculations will you perform?
3. How will you organize your output?
4. What theme or personality will your program have?

*[Distribute planning sheets or have students use notebooks]*

**Teacher:** Take 5 minutes to plan your program. Write down:
- At least 6 pieces of information you'll collect
- At least 2 calculations you'll perform  
- How you want your output to look

*[Students plan while teacher circulates]*

### **Development Time (20 minutes)**
**Teacher:** Now start building! Create a new file called "personal_intro_final". 

**Tips while you work:**
- Start simple and add features gradually
- Test your program frequently (run it every few lines)
- Use descriptive variable names
- Add comments to explain tricky parts
- Ask for help if you get stuck!

**Teacher:** Here's a basic structure to get you started:

```python
# Personal Introduction Program
# Created by: [Your Name]

print("Welcome to my Personal Introduction Program!")
print("Please answer a few questions about yourself.")
print()

# Collect information
# (Add your input statements here)

# Process and calculate
# (Add your calculations here)

# Display results
print()
print("=" * 40)
print("       YOUR PERSONAL PROFILE")
print("=" * 40)
# (Add your formatted output here)
print("=" * 40)
```

*[Give students 20 minutes to develop their projects. Circulate actively, helping with debugging and offering suggestions]*

### **Testing and Refinement**
**Teacher:** *[At 15-minute mark]* Everyone should test their program at least twice with different inputs. Make sure it works with messy input like extra spaces or weird capitalization!

---

## Project Showcase and Peer Review (5 minutes)

**Teacher:** Time to show off your work! We'll do quick demonstrations where volunteers can run their programs for the class.

**Teacher:** Who wants to demonstrate their program? I'm looking for:
- Creative themes or personalities
- Interesting calculations
- Good formatting and user experience
- Handling of messy input

*[Have 3-4 students demonstrate their programs, highlighting different strengths]*

**Teacher:** Excellent work! I'm seeing:
- Professional input handling and formatting  
- Creative calculations and fun facts
- Clean, organized output
- Programs that feel like real applications

### **Quick Peer Feedback**
**Teacher:** Turn to someone near you and trade programs. Run their program and give them one compliment and one suggestion for improvement.

*[Give 2-3 minutes for peer testing and feedback]*

---

## Unit 1 Wrap-up and Looking Ahead (5 minutes)

**Teacher:** What an incredible four sessions! Let's reflect on your journey:

**Session 1:** You printed your first "Hello, World!"  
**Session 2:** You learned to store information in variables  
**Session 3:** You made programs interactive with user input  
**Session 4:** You became text formatting experts  
**Session 5:** You created comprehensive applications combining everything!

**Teacher:** You now have the fundamental building blocks that every programmer needs. But here's what's exciting - next unit, we'll learn to make your programs **smart**. 

**Teacher:** Starting next class, we'll learn about **conditionals** - how to make programs that can make decisions, choose different paths, and respond intelligently to user input. Imagine programs that can:
- Give different responses based on user answers
- Create quiz programs that grade themselves  
- Build choose-your-own-adventure games
- Make smart calculators that handle different operations

**Teacher:** For next class, come ready to learn how to make your programs think!

### **Unit 1 Assessment**
**Teacher:** Your projects today serve as your Unit 1 assessment. I'll be looking at:
- ✅ **Variables:** Proper naming and usage
- ✅ **Input:** Clear prompts and appropriate conversions  
- ✅ **String methods:** Cleaning and formatting text
- ✅ **F-strings:** Professional output formatting
- ✅ **Integration:** Combining concepts effectively

**Teacher:** Save your projects! They'll be part of your programming portfolio that shows your growth throughout the course.

**Teacher:** Any questions about Unit 1 concepts before we move on to making decisions with code?

*[Address final questions]*

**Teacher:** Congratulations on completing Unit 1! You're no longer beginners - you're programmers with real skills!

---

## Teacher Notes for Session 5

### **Assessment Rubric for Mini-Projects:**
**Excellent (4):**
- Uses all required elements correctly and creatively
- Code is well-organized with clear variable names
- Professional formatting and user experience
- Handles input cleaning appropriately
- Includes creative bonus features

**Proficient (3):**  
- Meets all basic requirements
- Code works correctly with minor formatting issues
- Good use of f-strings and string methods
- Appropriate input handling

**Developing (2):**
- Meets most requirements but missing some elements
- Code works but may have minor bugs
- Basic formatting present
- Some confusion with string methods or f-strings

**Beginning (1):**
- Missing several required elements
- Significant bugs or errors
- Poor formatting or user experience
- Confusion about basic concepts

### **Common Issues to Watch For:**
- Students rushing without planning
- Forgetting to test with different inputs
- Not using string methods to clean input
- F-string syntax errors
- Variable naming inconsistencies
- Not including enough calculations

### **Extension Activities for Fast Finishers:**
- Add ASCII art or decorative elements
- Create themed versions (sports stats, music profiles, etc.)
- Add more complex calculations (BMI, days until birthday, etc.)
- Create multiple output formats (formal vs casual)

### **Differentiation Strategies:**
- **Struggling students:** Provide more structured template, pair programming
- **Advanced students:** Challenge with bonus features, help others debug
- **Different learning styles:** Allow various themes and creative expression

### **Preparation for Unit 2:**
- Review conditional logic concepts
- Prepare engaging examples of decision-making in programs  
- Set up comparison operator demonstrations
- Plan Session 6 hook around making programs "smart"

### **Portfolio Documentation:**
- Have students save their Session 5 projects as "Unit_1_Portfolio_Project"
- Consider having students write brief reflections on their learning
- Document individual student progress and areas for Unit 2 focus

### **Real-World Connections:**
- Profile creation in social media apps
- Account setup in online services  
- Form processing in websites
- Data collection in surveys and applications

This session successfully consolidates Unit 1 learning while preparing students for the conceptual leap to conditional logic in Unit 2.