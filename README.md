# JavaIO
 _derived from CISC191_IO_


Java Test Driven Development (TDD) project to program Java classes with unit testing ( with **JUnit** )
________

<details>
 <summary><em>source</em></summary>


 ![220px-MesaLogo](https://github.com/schougaard/SanDiegoMesaCISC191ProgrammingChallenges/assets/716243/334f6724-6afa-4198-9eff-7c49c472cd35)

# San Diego Mesa College CISC 191 Programming Challenges
Programming challenges for San Diego Community College CISC 191 Intermediate Java classes.

Created by
- Professor Dr. Tasha Frankie
- and Professor [Allan Schougaard](https://github.com/schougaard), San Diego Mesa College.

With contributions from: 
- Dom David,
- [Dan Sullivan](https://github.com/uid100)
________

</details>
<details>
 <summary>Overview</summary>

### Assignment Overview

The ability to read files is important in Java programming for a number of reasons:

- **Data persistence:** Files provide a way to store data persistently, meaning that it can be accessed and used even after the program that created it has terminated. This is essential for many applications, such as databases, web servers, and file managers.
- **Data exchange:** Files can also be used to exchange data between different programs and devices. For example, a program might read data from a file created by another program, or a program might write data to a file that will be read by a device such as a printer or a USB drive.
- **Configuration:** Files can also be used to store configuration data for programs. This type of data typically includes things like database connection strings, server addresses, and user preferences. Reading configuration data from a file allows programs to be more easily configured and maintained.

In addition to these general reasons, the ability to read files is also important for many specific Java applications. For example, web servers use files to store web pages and other static resources. Database applications use files to store database schema and data. And file managers use files to store and organize files on a computer's hard drive.

Here are some specific examples of how the ability to read files is used in Java programming:

- A web server might read a file containing a web page and send it to a user's web browser.
- A database application might read a file containing a database schema and create a new database based on that schema.
- A file manager might read a file containing a list of files and folders on a computer's hard drive and display that list to the user.
- A text editor might read a file containing a text document and display the contents of the document to the user.
- A compiler might read a file containing a Java source code file and compile it into a Java class file.

Overall, the ability to read files is an essential skill for any Java programmer. By being able to read files, you can create programs that can interact with the outside world, exchange data with other programs, and store and retrieve data persistently..
________

</details>
<details>
 <summary>Instructions</summary>

## _(Open the Project)_
1. From the **<> Code** dropdown link in the repository (above), download the Zip file to your computer.
2. Extract the files to your working folder
3. Open Eclipse and import the project. 
   - You can use File>Import menu item or right-click in the Package Manager and choose Import.
   - select General>Projects from Folder or Archive
   - navigate into the project until you see the `bin` and `src` folders, and choose *open*
4. Expand the project in the package explorer and find the .java files below the **src** folder.

## _(Complete the Assignment)_

</details>
<details>
 <summary>Code Layout</summary>
 
The setup for this programming assignment consists of two main Java files: **IO.java**, and **IOTest.java**.

#### IO.java
Where you will implement the code to pass the IOTest.java JUnit tests.

#### IOTest.java
The JUnit tests that will guide your completion of this programming assignment.
___________

</details>
<details>
 <summary>Programming Tasks</summary>

 
## Programming Task(s)
   <details>
       <summary>testReadTestResultsExists</summary>

### testReadTestResultsExists
This tester checks the logic of the readTestResults method which reads a file with a provided name (including filetype) and returns its content as a String. 
As with all your test-driven programming, the errors in the JUnit tester method should guide you in adding the missing code. 

Start by making the code compile. For example, you may need to add a missing method or class. 
Since this is from module 6, you should feel comfortable hovering over error lines and using quick fixes when appropriate. 
If you use quick fixes, double-check the return type and the parameter names for the auto-generated method headers.

You can use the File and Scanner classes in Java to help facilitate reading text files. Recall that even CSV files are text files with specific comma formatting distinguishing elements. Using these together can result in a special type of error in Java called an exception. You are given the structure to handle this in this programming assignment document, but you will revisit this later on!

Below is the main structure for reading in a file using File and Scanner. Read through the comments. Alter and add code to make it work for this method. 
//Setup the file as a File object as shown. File myFile = new File(fileName); //fileName is the name of the file

//setup scanner

Scanner scan = null;

//Add a try and catch block which looks similar to the block of an if-else-if statement! try {

  scan = new Scanner(myFile); //Create a Scanner object using the File object 
String content = ""; //Create a String to hold the content 

//Obtain content from the file as long as there is content to be obtained 
while(scan.hasNext()) 
{ 
     content += scan.next(); //Grab the content of the file through the Scanner with its next method } 
     //the loop ends once it has reach the end of the file. What do you have to do for your code? What do you do with content? 
} 
catch (FileNotFoundException e) 
{  
    // This block of code runs if the file is not found e.printStackTrace(); 
} 
finally {
   if(scan!=null)
    {
       scan.close();
    } 
}
Ensure your code above returns a String that holds the file's content!

Sidenote on finally block:
In Java, the finally block is used in conjunction with a try-catch block to ensure that certain code is executed regardless of whether an exception is thrown or not. The primary purpose of the finally block is to provide a mechanism for cleanup or resource management, such as closing files, releasing network connections, or cleaning up other resources. Here's why you might need a finally block in a try-catch construct:
Resource Cleanup: When working with external resources, such as files, database connections, or network sockets, it's important to ensure that these resources are properly released or closed, even if an exception occurs. The finally block is a good place to put code that handles resource cleanup, as it will be executed regardless of whether an exception was thrown in the try block.
Guaranteed Execution: Code in the finally block is guaranteed to run, even if an unhandled exception occurs in the try block. This ensures that you can maintain the integrity of your program by performing essential cleanup operations, regardless of how the try block terminates.
Maintaining State: finally blocks are useful for maintaining the program's state and ensuring that the program doesn't leave resources in an inconsistent or erroneous state if an exception is thrown

    
   </details>


___________

</details>

<details>
 <summary>Complete and submit the project</summary>
 
## Complete and zip the project
1. Run and add the code to the src folder until the tests are successful.
2. Uncomment each test case in the **Test** file (`TestAdvancedClasses.java`), one at a time. 
Do not modify the content in this file except to uncomment the tests. Add and modify class files
as needed for the tests to pass.
3. Review and refactor any of the code as needed:
    - be sure your code follows good coding practices and coding style and standards.
    - update the javadoc comments at the top of the file to add your name as author
    - update the comments for each method in the file.
4. Export the project as a zip file and submit your work.

___________

## Rubric

[Rubric](Rubric.md)

</details>


___________
_This repository is a subset of the CISC191 exercises. It is derived from the CISC191ProgrammingChallenges 
activity hosted by Professor Allan Schougaard, San Diego Mesa College, and not a direct fork._

_This project is to decompose that repository into git submodules_
