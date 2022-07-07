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

