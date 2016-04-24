# StripperProject

Write a partial preprocessor program that removes blank lines and Java-style comments 
from a text file.  Create test cases to check the program, and a program to verify 
test output.

/************************************************************************************/

Details – Stripper 

1.	Processing.  Take a text file (perhaps purporting to be a Java program), 
    and strip all blank lines and comments.  The stripped file will have only 
    text lines remaining (Java code, perhaps – since we aren’t processing the code, 
    it doesn’t matter what is in the text portions of each file).
    
            a.	There are two kinds of blank lines: “true” blank lines, consisting 
                of only a return character, and apparent blank lines 
                (they look blank to us), which have a return after blanks and / or tabs.
                
            b.	There are two kinds of comments, formatted as Java defines comments.  
                Line comments, delimited by ‘//’ and end of line, can cover part or 
                all of one line.  Block comments, delimited by ‘/*’ and ‘*/’, can 
                cover part of a line, one line, or more than one line.  You may 
                assume there are no unclosed block comments.
                
            c.	Do not remove any extraneous blanks or tabs in the middle or at 
                the end of a text line (for example: int total;<blank><blank><blank>
                will not be altered). 
                
/************************************************************************************/

2.	Development.  Create and exchange your test files first (see below), 
    then design, write, and test the code in for each phase.
    
            a.	Phase 1: strip both kinds of blank lines.
            b.	Phase 2: strip line comments.
            c.	Phase 3: strip block comments.
            d.	Phase 4: no additional functionality, but test 
                against files containing a combination of blank lines 
                and comments and plain text.
                
/************************************************************************************/

3.	Input.  Run your program against your own test files and against 
    swapped files from classmates (see below).  Files to be processed 
    will be read from the default folder.  Name the test files so that your 
    program can cycle through all test files in a single loop.  To do this, 
    each file name will have three parts, created by concatenation in the main 
    loop: a prefix that is the same for every file (use striptest), a number 
    for which test case it covers (see later list), and a letter for which student’s 
    case it is.  You will have, in part, the following test files:
    
            striptest-1.txt     	your input file for test case 1
            striptest-2.txt 	your input file for test case 2
            :
            striptest-10a.txt     	first input file for test case 10 (yours)
            striptest-10b.txt     	second input file for test case 10 (classmate #1)
            striptest-10c.txt     	third input file for test case 10 (classmate #2)
            striptest-10d.txt     	fourth input file for test case 10 (classmate #3)
            :
          	In this example, 10a, 10b, 10c, and 10d should be testing the same 
          	case (#10 on the list), but they will be different in that each 
          	person will (most likely) create a different specific example for that test case.  
          	
/************************************************************************************/

4.	Output.  The stripped file is written to a new file whose name is based on 
    the input name (again created with concatenation):
    
            striptest-1-out.txt     		output from your file for test case 1
            striptest-2-out.txt     		output from your file for test case 2
            striptest-10a-out.txt     	output from your file for test case 10
            striptest-10b-out.txt     	output from one classmate’s file for test case 10
            etc.

/************************************************************************************/

5.	Implementation.  Do not use any language or library features such as regular 
    expressions that reduce the complexity of the program.  You may use any language 
    for the project.

/************************************************************************************/

Details - Testing
1.	Test your program incrementally using your input files and files from classmates.  
    By changing your loop counter (which creates the files names), you can control 
    which tests you want to run at any given time.  Ultimately, your program 
    will run through every test case and all the files in one execution.
    
              a.	In class, collect emails from three other students. 
              
              b.	Create a test input file for each test case on the 
                  listing at the end of the assignment.  Send your group 
                  members your test files, named correctly, with your 
                  suffix as decided in your group (‘a’, ‘b’, etc.).  File 
                  in the attached sheet with your classmate’s names, emails, 
                  and suffixes to keep track of which files came from which classmate.  
                  See due dates for when to email files to classmates for each phase.
                  
              c.	Make sure you carefully check each output file for correctness.  
                  Since the processing is straightforward, we won’t exchange expected 
                  output except on the last case (see below); on the simpler tests, you 
                  can easily tell whether blank lines and comments have been correctly removed. 
                  Be sure you check for small errors like not dropping the ‘/’ from a ‘*/’ pair.
              
              d.	I will send several final test cases for you to run.  They will be 
              files that have various groupings of blank lines, comments, and text.  
              Check this output with your checker program.
              
