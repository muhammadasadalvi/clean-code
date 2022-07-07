# clean-code
1. C++ Author: Code Should be Elegant and efficient. 
2. Author of OO analysis: Clean code is simple and direct. should have straightforward lines of control. 
3. Clean Code can be read, and enhanced by developer. It has unit and acceptance tests. It has meaningful names. It provides one way rather to provide many methods to do one thing. 
4. Clean code is written by someone who cares.

Simple Code:
* runs all the test
* contains no duplication
* express all the design ideas that are in the system
* minimize the number of entities such as classes, methods, functions and the like. 

You can call it beautiful code when the code makes it look like the language was made for the problem. 

# Meaningful Name
Choosing good names takes time but saves more than it takes.

**int d; // gives no meaning**
**e.g. int elapsedTimeInDays;**
**e.g. int deysSinceCreation;**

**Example 1: With Bad Naming Conventions** 
public List<int[]> getThem() {<br/>
List<int[]> list1 = new ArrayList<int[]>();<br/>
for (int[] x : theList)<br/>
if (x[0] == 4)<br/>
list1.add(x);<br/>
return list1;<br/>
}

**Example 1: With Good Naming Conventions**
public List<int[]> getFlaggedCells() {<br/>
List<int[]> flaggedCells = new ArrayList<int[]>();<br/>
for (int[] cell : gameBoard)<br/>
if (cell[STATUS_VALUE] == FLAGGED)<br/>
flaggedCells.add(cell);<br/>
return flaggedCells;<br/>
}

**Example 1: Modified Version**
public List<Cell> getFlaggedCells() {<br/>
List<Cell> flaggedCells = new ArrayList<Cell>();<br/>
for (Cell cell : gameBoard)<br/>
if (cell.isFlagged())<br/>
flaggedCells.add(cell);<br/>
return flaggedCells;<br/>
}

1. Use Pronounceable Name
2. Use Searchable name instead of number etc. like 7, 5 use const int NUMBER_OF_WEEK_DAYS = 7;
3. Avoid encoding
4. Class Names - Classes and Object should have noun and noun phrase names like **Customer**, **WikiPage**
5. Method Name - method names are verb and verb phrase postPayment, deletePage, save
6. Don't be cute, names should be clever and easy to remember i.e. **Say what you mean. Mean what you say**
7. Pick one Word Per Concept.
8. Add meaningful context, like state if it is part of form then we can understand it is part of address but if use in another function then we cannot undersatnd, addrState is giving context.

---

# Functions
1. The First Rule is: Function should be small 20-30 lines max
2. if, else, while blocks should be one line long and indent level not more than one to two indent level. 
**FUNCTIONS SHOULD DO ONE THING . T HEY SHOULD DO IT WELL .THEY SHOULD DO IT ONLY .**

