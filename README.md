Assignment 4 --> Jacob Scheetz, Ian Iding,  Bailey Dauterman



CPS 350: Assignment 4
Two weeks, 100 pts
Due Date: March 25, 2020 at 11:55PM
This is a team project (up to four students per team). No late submissions will be accepted.
Receive 5 bonus points if turn in the complete work without errors at least one day before deadline.
Receive an F for this course if any academic dishonesty occurs
1. Purpose
The purpose of this assignment is to implement left-leaning red-black trees.
2. Description
In this assignment you will do a simple modification based on a given framework of Binary
Search Tree (BST) by changing it into a left-leaning red-black tree to maintain balance. Binary
Search Trees have a disadvantage in that the tree can grow in an unbalanced manner, depending
(primarily) on the order of data (nodes) to be inserted. Your job is to improve the existing BST
software and make it into a balanced version via the red-black principle. After you download the
provided framework and unzip the file, three files are extracted: (1) “MainGUI.java” (2)
“Node.java” (3) “Tree.java”.
2.1. Run the code
(1) Use Eclipse to create a “JavaFX project” by clicking menu “File”  “New”  “Project”.
This is the same as you did on previous JavaFX projects.
(2) Copy the three files above to the source folder of your newly created projects
“src/application/” folder. By default, after you create the project, you have “Main.java”
and “application.css” files in the folder. You can just delete the “Main.java” (leave the
“application.css” as it is) before copying the three files into it.
(3) Then refresh the “application” package in the Eclipse. You should be able to run the code
as shown in Figure 1:
 Figure 1: Binary Search Tree User Interface
The GUI allows you to add node into the tree by simply typing a number (with one or two digits
only) and hitting “ENTER” key or clicking the “add” button. Then the new node should appear
in the tree. Also, you can change the node position freely by simply “dragging” the node on
canvas to move it to any preferred position as Figure 2 shows. But it is recommended that you
not move both the left and right children to one side of the parent or above the parent, as this
makes the tree structure less meaningful with respect to a BST. Every time when a node is
inserted or selected, it is highlighted by a thin “yellow ring” around the node. You can remove
such highlight at any time by “Right Clicking” or “Left Clicking” your mouse on any blank area
of the canvas. Also, you can use the mouse to choose or highlight any node by left clicking on
the node directly.
Figure 2: Demo of dragging or moving a node to any position
As discussed earlier, the BST can easily go out of balance. Even with the same set of numbers,
different insertion orders may result in different tree appearances as Figure 3 demonstrates:

Figure 3: the same set of numbers end up with two tree structures
2.2. Implementation Requirements
You are to fix this unbalanced issue by placing incorporating left-leaning red-black tree
constraints. In addition, the tree must NOT contain any duplicate keys. So, as the warmup tasks, 
first try two simple things to start coding as described in (1) and (2) below. After finishing these
two simple tasks, you can start working on the left-leaning red-black tree implementation. Below
shows the details tasks which all involve modifying the “Tree.java” class.
(1) Modify the “insertNode()” function to make sure no repeating value nodes are inserted, e.g.
for the tree in the Figure 3, if you insert 55 again, no changes should occur on the tree, since
55 already exists.
(2) Try to change node color in the “insertNode()” function by following the example code in
the beginning of the function: “node.setColor(Node.GREEN);” This code is to set green
color. You can also try to change it to “BLACK” or “RED” color as shown in Figure 4.
(3) Now, you can start to implement the left-leaning red-black tree insertion algorithm based
on the given “insertNode()” function. Feel free to add more functions if necessary. But the
additional function should be called by the “insertNode()” function. In other words,
“insertNode()” function is the entry function when an insertion event occurs.
Figure 4: results of changing the tree to other colors. But this is not the final goal for redblack tree, which should have a combination of both red and black colors.
2.3. Add your code
Within the existing framework, you need to focus on modifying the code in the “Tree.java” file.
You do NOT need to make any changes to the “MainGUI.java”. However, you may write some
code (optional) for the “Node.java” depending on your specific left-leaning red-black tree
implementation.
For the “Node.java” and “Tree.java” files, each file has a pair of comment lines:
/******************** Implementation Here: ***************************/
/******************** End of Implementation ***************************/
You are required to write your code between these two lines. It is NOT recommended that you
write or modify any code outside this range.
 
Hints:
(1) Please follow the comments in the code, which describes the framework and the part for
your implementation in details.
(2) For the “Node.java”, the data members you may use for the assignment are separated
from the ones for the GUI part. So the data members you need to know are at the top of
the class, such as “left”, “right”, “color”, etc. In fact, for this class, you just need to use
these data members and do not need any additional coding.
(3) For the given code in the “insertNode(Node node)”, you may notice other than assigning
“left” or “right” child, the existing code also assigns other relationship such as “parent”
and “left_child_of_parent” variables. These variables are important as they allow the
nodes to be accessed easily across the tree. The GUI also needs this information to draw
the tree on the canvas. So when you modify the code, make sure set these variables
accordingly. Moreover, the existing code shows the non-recursive way to insert a new
node onto a BST. Your implementation of insertion for a left-leaning red-black BST
should be done recursively, as shown in class; the recursive method is both elegant and
precise.
(4) Make sure that the root is black. Make sure that you have a method such that it returns
true if the node’s color is red; if the node is null, return false! This is extremely
important; otherwise you will encounter null pointer errors!
2.4. Rubrics
Though there is only one major function “insertNode()” involved for the red-black tree
implementation, the function should conduct a sequence of tasks, e.g. left-rotation or rightrotation, coloring, etc. You should put these actions into separate sub-functions, which makes
your code more organized and easier for grading. Figure 5 shows an example of a successful
implementation of “insertNode()” which yields a balanced tree with correct left-leaning color
assignment.
Figure 5: Result of Left-Leaning Red-Black tree with balanced node distribution. 
3. Grading notes
If your program does not compile, you receive zero points for that program. Additional
deductions:
1. (5 points) Your code does not follow the style guide discussed in class/textbook.
2. (5 points) You turn-in items that are NOT asked for (extra files, etc.)
3. (30 points) Your code does not have author name, date, purpose of this program,
comments on the variables and methods, etc.
(1) List any difficulties you have during implementation. What is the fun part of this
assignment? (10 points)
(2) Modify the insertNode() so that the tree does NOT allow node with repeating value to be
inserted (15 points)
(3) Successfully complete the “insertNode()” function to achieve left-leaning red-black tree
insertion:
(a) Solution is recursive (15 points)
(b) Correct node color assignment (20 points)
(c) Correct left or right rotation (40 points)
4. Submission
Your project should be submitted through Isidore. Turn in your updated version of the source
codes “Node.java” and “Tree.java”, and a report for questions in Section 3 Grading notes,
which should be zipped into a single folder. 