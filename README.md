java c
COSC2391 Further Programming / COSC1295 Advanced Programming 
Assignment 2 - Semester 2 2024
1. Introduction 
This assignment is designed to:
•    Evaluate your ability to develop GUI applications using JavaFX.
•    Evaluate your skills in storing persistent copy of data.
• Test your knowledge to implement advanced OO design patterns.This is an individual assignment. Your final submission is worth 42%; an in-lab milestone check in Week 10 is worth a further 3%; a final post-submission interview is worth 5%; giving a total of 50% for Assignment 2.
2. Academic Integrity (more) 
The submitted assignment must be your own work. No marks will be awarded for any work which is not created by you.Plagiarism is treated very seriously at RMIT. Plagiarism includes copying code directly from other students (or enables such copying), the internet, the output of AI systems, or other resources without proper  reference. Sometimes, students study and work on assignments together and submit similar files which may be  regarded as plagiarism. Please note that you should always create your own assignment even if you have very similar ideas. Plagiarism- detection tools will be used to check all submissions. Penalties may be applied in cases of plagiarism.
3. Background 
This assignment extends Assignment 1. You will build a GUI application for The Reading Room bookstore. The bookstore sells the following books (all are physical copies):
BOOK TITLE AUTHORS # PHYSICAL COPIES PRICE (AUD) # SOLD COPIES 
Absolute Java Savitch 10 50 142 
JAVA: How to Program Deitel and Deitel 100 70 475 
Computing Concepts with JAVA 8 Essentials Horstman 500 89 60 
Java Software Solutions Lewis and Loftus 500 99 12 
Java Program Design Cohoon and Davidson 2 29 86 
Clean Code Robert Martin 100 45 300 
Gray Hat C# Brandon Perry 300 68 178 
Python Basics David Amos 1000 49 79 
Bayesian Statistics The Fun Way Will Kurt 600 42 155
4. Task Specifications 
Basic functional requirements are listed below.
• The application can have many users.
• Each user can create a profile, with a unique username, password, and first and last name.
• Once the username and password are created, the user can log in.
•    Each user is shown a dashboard after login. The dashboard should display a personalized welcoming message that addresses the user by name. The dashboard also displays the top 5 popular books in the bookstore. The top 5 books are identified based on the number
of sold copies.
• Each user can perform. the following actions:
o Edit profile (change first name/last name/password, username is not changeable)
o Add books to shopping cart. The program can guide the user to place an order by selecting books and specifying quantity. The program should allow the user to update  the  shopping  cart  (e.g.,  removing  books,  updating  quantity)  before checking out. When there is a modification to the shopping cart, the program should verify the availability of stock and notify the user if any selected book is unavailable.
Example 1. Assume that there are 10 copies of “Absolute Java” available. A  user will get a warning message if he/she adds 11 copies of “Absolute Java” to shopping cart.
Example 2. Assume that there are 10 copies of “Absolute Java” available. User A adds 10 copies of “Absolute Java” to the shopping cart. User B also adds 2 copies of “Absolute Java” to the shopping cart. Both of them will NOT get a warning as long as they have not checked out.
Example 3. Assume that there are 10 copies of “Absolute Java” available.User A adds 10 copies of “Absolute Java” to the shopping cart. User B also adds 2 copies of “Absolute Java” to the shopping cart. User B will get a warning message once user A checks out - the book “Absolute Java” is deemed as sold-out after user A checks out.
o Check out. A user will be notified of the total price before placing the order. Once confirmed by the user, proceed to payment, where you collect (fake) credit card information (card number, expiry date, and cvv). (Do not use real credit card numbers!) You will need to perform. simple validation to check (1) if the card number has 16 digits; (2) if the expiry date is a future date; (3) if cvv has 3 digits. For simplicity, you can assume the payment will be successful. Once an order is placed, a unique order number will be generated and assigned.
o View all orders. The user can view the following details of all historical orders: order numbers, date and time the order was placed, the total price of each order, and books purchased along with their respective quantities. The orders should be displayed in reverse chronological order, with the most recent order appearing first.
o Export all orders. The user should be able to export historical orders, including the date  time of the orders, total price, and the purchased books with their quantities, to a file. The user can select specific orders for export, choose the file destination, and specify the file name. The exported file should be saved in CSV format.
o Log out.
•    The program has a special user that is the admin account. The account is initialized with the following information:
Username                Password                    First name                Last name 
admin                     reading_admin                    Admin                      Admin 
• The admin user can perform. the following actions:
o Once log in, the admin user should be displayed with an admin dashboard, showing a welcome message to the admin user.
o View the stock of all books. The program can list all the books in the bookstore. It   will display the detailed information of each book, including the title, authors, price, the number of sold copies, and the remaining stock.
o Update the stock of a book. The admin user can update (increase or decrease) the number of copies available for a selected book.
•    A non-admin user should not be permitted to perform. th代 写COSC2391 Further Programming / COSC1295 Advanced Programming Assignment 2 - Semester 2 2024Java
代做程序编程语言e functionalities of an admin user, and vice versa. For example, a normal user should not be able to update the stock of books.
5. Assessment Details 
This assignment is structured in three milestones: in-lab milestone check in week 10, full program submission in week 12, and post-submission interview in week 14. It is recommended for you to follow the stages below to incrementally build the GUI application. But you can also plan the work in your own way. 
5.1 SetupYou will use GitHub to store program code in this assignment. To get started, accept the assignment invitation by clicking this link:https://classroom.github.com/a/TTIbzQF1 . You will need to create a GitHub  account  if  don’t  have.  After  accepting  this  invitation,  create  a  git  repository  in FurtherJavaProgramming-classroom-2450. Make your repository private. Otherwise, your repository will be considered as plagiarism.Instructions to create a git repository and upload your project to GitHub can be found in Work with GitHub and GitHub Classroom.pdf from Canvas -> Assignment 2. Throughout the program development, you will need to make regular commitments to GitHub to facilitate transparency in the development process.
5.2 Part A (In-Lab milestone – Week 10)This milestone aims to assess your ability to define user interfaces for GUI application. For this milestone, you will prepare a documentation of your UI design using Scene Builder. While you don’t need to strictly follow this design as you progress to later stages, you should propose a UI design that reflects your current understanding to the best of your ability at this stage.
5.3 Part B
Following Part A, you will work on the frontend and backend part of the application. You will implement the functionalities described in the task specification.You will connect the front-end and back-end to build a functional program. You will use JDBC to store program data, so that the application can be restarted in the same state it was in the end of the previous execution. You will incorporate OO principles to design and optimize classes. You will also implement OO design pattern where applicable.
5.4 Part C (Full program submission – Week 12)
You will implement meaningful unit tests to test the functionalities of key classes in your program. See marking rubric for details.
5.5 Part D (Post-submission interview – Week 14)You will be interviewed after program submission. During the interview, you will demonstrate the functionality and GUI design of your program. In addition, it is crucial for you to demonstrate your programming skills by clearly explaining how you design the program and implement different functionalities.
6. General Requirements This section summarizes the general requirements of Assignment 2 in four aspects: (1) GUI; (2) Functionality; (3) Program Design; (4) Programming Challenge; and (5) Others. Please refer to  Canvas -> Assignment 2 -> Rubric for detailed mark allocation.Important notes: Marks for GUI, Functionality, and Programming Challenge are checked during the post-submission interview. If you do not attend the final interview, you will be awarded ZERO mark for these sections. You will also get mark deductions if you cannot EXPLAIN how you implement the functionalities.
6.1 GUI 
•    Your program should include appropriate JavaFX components to make the application easy- to-navigate.  For  example,  each  window  should  have  a  window  title;  menu  options  (if applicable) are selected from a menu bar.
•    Your program should respond clearly to every user’s action. For example, if the user types a wrong password, the login window should display a clear error message and ask the user to type again.
•    Your program should provide visual consistency. Avoid using different styles and labels for similar elements on different windows of the application.
• The UI design of your program should serve the purpose of the application.
6.2 Functionality 
All functions required by specification are implemented correctly covering different cases that might happen during the usage of the program.
6.3 Program Design 
Appropriate choice of data structures that serves the purpose of the application. Class designs that adhere to the SOLID principles.
• You are required to follow MVC pattern to connect the frontend with the backend.
•    You are required to use one of design patterns such as Singleton pattern, besides the MVC pattern.
•    You are required to implement at least one interface or abstract class to demonstrate your understanding of OO principles.
•    You  are required to apply SOLID principles when appropriate in order to enhance the maintainability and extensibility of your program, decrease coupling amongst classes, and minimize code repetition across classes.
•    You are required to choose appropriate data structures to enhance the running efficiency of the program.
6.4 Programming Challenge 
You will be asked two questions about how to extend your program to either achieve a certain new functionality or change the behaviour of an existing functionality. An example question is as follows:
•    Suppose the book "Clean Code" has become very popular recently and you need to set a limit on the maximum number of copies that can be purchased by each customer. How will you implement it?To achieve the functionality described in the question, you should clearly identify which parts of your program, both frontend and backend, require modification. Additionally, you should explain how each component will be updated and how these changes will implement the desired functionality.
6.5 Others 
•    High source code quality with adequately commented and properly indented codes and appropriate class/method/variable names.
• Regular commitments to GitHub to show the progress of program development.
• Implement at least 5 meaningful unit tests for one class that you choose.







         
加QQ：99515681  WX：codinghelp
