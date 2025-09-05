# Session 4: String Operations and Formatting
**Duration:** 60 minutes  
**Learning Goals:** Manipulate text effectively  
**Materials Needed:** Computers, notebooks, mad libs templates (optional)

---

## Opening Review and Hook (5 minutes)

**Teacher:** Welcome back! Let's start by seeing some of your "About Me" questionnaire programs. Who created something they want to share?

*[Have 2-3 students demonstrate their homework programs]*

**Teacher:** Excellent work! I love how interactive your programs have become. Now, I noticed something in everyone's programs. When people type their names, sometimes they type them in all lowercase, sometimes all uppercase, sometimes with weird spacing. Watch this:

*[Demonstrate on projector with a simple input program]:*
```python
name = input("What is your name? ")
print("Hello", name, "!")
```

**Teacher:** *[Type responses like "  sarah  ", "MIKE", "jessica"]*

See how the output looks a bit messy? Sometimes we get "Hello   sarah   !" or "Hello MIKE!" when we really want "Hello Sarah!".

**Teacher:** What if I told you that Python has built-in tools to clean up text, change its case, and format it beautifully? Today we're going to learn how to manipulate strings like a pro. By the end of class, your programs will handle text input like professional applications!

---

## String Methods: The Basics (12 minutes)

**Teacher:** Strings in Python aren't just chunks of text - they're objects with **methods** built into them. Think of methods as special abilities that every string has.

*[Write on board: "String Methods - Special abilities every string has"]*

**Teacher:** Let me show you the most useful ones:

### **Changing Case**
*[Type on projector while students follow along]:*
```python
name = "sarah johnson"
print("Original:", name)
print("Uppercase:", name.upper())
print("Lowercase:", name.lower())
print("Title Case:", name.title())
```

**Teacher:** Everyone create a new file called "string_methods" and type this code. Run it and see what happens!

*[Give students time to try this]*

**Teacher:** Cool, right? Notice the syntax: `name.upper()`. We take our string variable, add a dot, then the method name with parentheses. The string doesn't change permanently - these methods give us new versions.

### **Cleaning Up Spaces**
**Teacher:** Add this to your file:

```python
messy_input = "  hello world  "
print("Original: '" + messy_input + "'")
print("Cleaned: '" + messy_input.strip() + "'")
```

**Teacher:** The quotes help us see the spaces. `.strip()` removes spaces from both ends - super useful for cleaning up user input!

### **Replacing Text**
**Teacher:** Add this too:

```python
sentence = "I love apples and apples are great!"
print("Original:", sentence)
print("Modified:", sentence.replace("apples", "oranges"))
```

**Teacher:** `.replace()` finds all instances of the first word and replaces them with the second word.

### **Checking Contents**
**Teacher:** These methods return True or False:

```python
email = "student@school.edu"
print("Contains @:", email.count("@"))
print("Ends with .edu:", email.endswith(".edu"))
print("Starts with student:", email.startswith("student"))
```

**Teacher:** Try all of these! Methods that ask questions often start with words like "starts", "ends", "contains", or "is".

---

## Practical Application: Name Formatter (8 minutes)

**Teacher:** Let's solve that messy name input problem from the beginning of class. We'll create a program that takes any name input and formats it nicely.

*[Create new file on projector]:*
```python
# Name Formatter Program
print("Name Formatter - Makes any name look professional!")

# Get user input (might be messy)
raw_name = input("Enter your full name: ")

# Clean and format the name
cleaned_name = raw_name.strip()  # Remove extra spaces
formatted_name = cleaned_name.title()  # Make Each Word Start With Capital

# Display results
print()
print("You entered:", "'" + raw_name + "'")
print("Formatted name:", formatted_name)
print("Length:", len(formatted_name), "characters")
print("Number of words:", formatted_name.count(" ") + 1)
```

**Teacher:** Everyone create this program. Test it with messy input like "  sarah johnson  " or "MIKE SMITH" or "jessica brown".

*[Give students time to create and test]*

**Teacher:** See how professional this makes the output look? This is exactly what real applications do when you create accounts or fill out forms!

---

## String Formatting with f-strings (12 minutes)

**Teacher:** So far we've been using commas in print statements to combine text and variables. But Python has a much more elegant way called **f-strings** (formatted string literals).

*[Write on board: "f-strings - A better way to format text"]*

**Teacher:** Look at the difference:

*[Show both methods]:*
```python
name = "Alex"
age = 16
grade = 10

# Old way (what we've been doing)
print("Hi, my name is", name, "and I am", age, "years old in grade", grade)

# New way (f-strings)
print(f"Hi, my name is {name} and I am {age} years old in grade {grade}")
```

**Teacher:** The f-string starts with an `f` before the quote, and we put variables inside curly braces `{}`. Much cleaner!

**Teacher:** Create a new file called "f_string_practice" and try this:

```python
# F-string Practice
name = input("What's your name? ").strip().title()
age = int(input("How old are you? "))
hobby = input("What's your favorite hobby? ").strip().lower()

print(f"Nice to meet you, {name}!")
print(f"At {age} years old, you're interested in {hobby}.")
print(f"In 5 years, you'll be {age + 5} years old.")
print(f"Your name backwards is {name[::-1]}")  # Advanced trick!
```

**Teacher:** Notice how I'm chaining methods: `.strip().title()` cleans the input AND formats it in one line!

*[Give students time to test this]*

### **F-strings Can Do Calculations**
**Teacher:** Add this to see something cool:

```python
# F-strings with calculations
width = float(input("Enter width: "))
height = float(input("Enter height: "))

print(f"A rectangle {width} by {height} has an area of {width * height}")
print(f"The perimeter is {2 * (width + height)}")
```

**Teacher:** F-strings can do math right inside the curly braces!

---

## Major Activity: Mad Libs Generator (18 minutes)

**Teacher:** Now for our main project - a Mad Libs generator! Mad Libs are stories with blanks that get filled in with random words to create funny stories.

**Teacher:** We'll create a program that asks for different types of words, then plugs them into a story template using everything we've learned about strings.

**Teacher:** Start a new file called "mad_libs_generator":

```python
# Mad Libs Story Generator
print("=" * 50)
print("          WELCOME TO MAD LIBS!")
print("=" * 50)
print("I'll ask you for some words, then create a funny story!")
print()

# Collect words from user
print("Please provide the following words:")
adjective1 = input("An adjective (like funny, big, scary): ").strip().lower()
noun1 = input("A noun (like cat, car, pizza): ").strip().lower()
verb1 = input("A verb ending in -ing (like running, singing): ").strip().lower()
adjective2 = input("Another adjective: ").strip().lower()
noun2 = input("Another noun: ").strip().lower()
color = input("A color: ").strip().lower()
number = int(input("A number: "))
noun3 = input("A plural noun (like dogs, books): ").strip().lower()
verb2 = input("A verb (like jump, eat, dance): ").strip().lower()

# Create the story using f-strings
print()
print("=" * 50)
print("           YOUR MAD LIBS STORY")
print("=" * 50)

story = f"""
Once upon a time, there was a {adjective1} {noun1} who loved {verb1}.
Every day, this {adjective2} {noun1} would {verb2} around the {color} {noun2}.

One day, {number} {noun3} appeared and challenged the {noun1} to a contest.
"Let's see who can {verb2} the fastest!" they said.

The {adjective1} {noun1} accepted the challenge and began {verb1} like never before.
In the end, everyone learned that {verb1} is the most {adjective2} activity in the world!

The End.
"""

print(story)

# Add some statistics
print("=" * 50)
print("STORY STATISTICS:")
print(f"Your story has {len(story)} characters")
print(f"You used the word '{noun1}' {story.count(noun1)} times")
print(f"The story contains {story.count('.')} sentences")
print("=" * 50)
```

**Teacher:** This is a big program! Type it carefully. Notice several important things:

1. **Triple quotes** (`"""`) let us write multi-line strings
2. We're using **f-strings** to insert variables into the story
3. We're **chaining methods** like `.strip().lower()`
4. We're using **string methods** to analyze the completed story

*[Give students 12-15 minutes to type and test this. Circulate and help with typing/debugging]*

**Teacher:** Test your program! Try it multiple times with different words and see how funny the stories get.

---

## Advanced String Tricks (3 minutes)

**Teacher:** For those who finish early, here are some advanced string tricks to try:

```python
# Advanced string operations
text = "Hello World"

print(f"Reversed: {text[::-1]}")  # Slicing backwards
print(f"Every other letter: {text[::2]}")  # Every 2nd character
print(f"Is all letters: {text.replace(' ', '').isalpha()}")
print(f"Word count: {len(text.split())}")  # Split into words and count
print(f"Centered: '{text.center(20, '*')}'")  # Center with padding
```

**Teacher:** Don't worry if these seem complex - we'll learn more about slicing and advanced operations in future classes. For now, just experiment and see what happens!

---

## Wrap-up and Showcase (2 minutes)

**Teacher:** Let's see some of your Mad Libs stories! Who got a particularly funny result?

*[Have 2-3 students read their generated stories aloud]*

**Teacher:** Hilarious! Look at how sophisticated your programs have become. You're now cleaning user input, formatting text beautifully, and creating complex interactive stories.

**Teacher:** Let's review what we learned today:

*[Write on board as we review]:*

1. **String methods:** `.upper()`, `.lower()`, `.title()`, `.strip()`, `.replace()`
2. **F-strings:** `f"Hello {name}!"` - cleaner formatting
3. **Method chaining:** `.strip().title()` - multiple operations in one line
4. **Multi-line strings:** `"""` for longer text
5. **Text analysis:** Using string methods to analyze content

**Teacher:** For homework, create a story generator using string methods and f-strings. Choose your own theme - it could be:
- A superhero adventure generator
- A school day story creator
- A sports story builder
- A mystery story generator

Use at least 5 different user inputs and make sure to clean/format them properly!

**Teacher:** Next class, we'll have a **Unit 1 Review** and work on a mini-project that combines everything we've learned: variables, input, and string manipulation.

**Teacher:** Any questions about string methods or f-strings?

*[Address final questions]*

**Teacher:** Excellent work today! You're mastering text manipulation like professional developers!

---

## Teacher Notes for Session 4

### **Common Student Questions & Answers:**
- **"Why use f-strings instead of commas?"** F-strings give you more control over formatting and are easier to read when combining lots of variables
- **"Do string methods change the original string?"** No! They return a new string. If you want to keep changes, assign to a variable
- **"What's the difference between .title() and .capitalize()?"** `.title()` capitalizes every word, `.capitalize()` only the first letter
- **"Can I use multiple methods together?"** Yes! That's called method chaining: `name.strip().title()`

### **Extension Activities for Fast Finishers:**
- Create a text-based username generator that formats names into usernames
- Build a program that analyzes text for readability (word count, sentence count)
- Make a simple encryption program that replaces letters with numbers
- Create a program that generates email addresses from names

### **Assessment Checkpoints:**
- [ ] Student can use basic string methods (.upper(), .lower(), .strip())
- [ ] Student understands f-string syntax and can use variables in them
- [ ] Student can chain multiple string methods together
- [ ] Student can create multi-line strings with triple quotes
- [ ] Student can combine string methods with user input for practical applications

### **Common Errors to Watch For:**
- Forgetting the `f` in f-strings: `"Hello {name}"` instead of `f"Hello {name}"`
- Trying to use methods on numbers: `age.upper()` when age is an integer
- Forgetting parentheses in methods: `name.upper` instead of `name.upper()`
- Confusing assignment with method calls: thinking methods permanently change strings
- Syntax errors in multi-line strings (mismatched quotes)

### **Differentiation Strategies:**
- **For struggling students:** Provide a reference sheet of common string methods, use simpler Mad Libs templates
- **For advanced students:** Introduce string slicing, challenge them to create more complex story generators
- **For kinesthetic learners:** Act out what different string methods do (standing up for .upper(), whispering for .lower())

### **Preparation for Next Session (Unit Review):**
- Prepare review activities covering variables, input, and string operations
- Create a comprehensive mini-project that combines all Unit 1 concepts
- Have debugging exercises ready for common mistakes from all three topics
- Prepare peer review guidelines for student projects

### **Materials to Prepare for Next Session:**
- Unit 1 concept review sheet
- Mini-project requirements and rubric
- Sample projects demonstrating best practices
- Troubleshooting guide for common errors across all Unit 1 topics

### **Real-World Connections to Highlight:**
- Form validation in websites (cleaning user input)
- Username generation in social media platforms
- Text formatting in word processors
- Data cleaning in spreadsheets and databases
- Chatbot response formatting

### **Troubleshooting Tips for Teachers:**
- If students struggle with f-string syntax, show side-by-side comparisons with comma formatting
- Watch for students trying to call methods on non-string variables
- Be ready to explain the difference between methods that return new strings vs. modify in place
- Have extra Mad Libs templates ready for students who finish the main one quickly