# DB

Team members: Madhusudhan Byru(12611642) and Guru Sai Prasad Sunkara(12..)
Dataset: The sample data contains attributes like StudenetID, FirstName, Lastname, Course, Professor, ProfessorEmail, CourseStart, CourseEnd. The dataset is taken as .csv file(comma separated values).

Functional Dependencies: The functional dependencies used for the dataset are:
StudentID -> FirstName, LastName Course, 
Professor -> classroom
Course -> CourseStart, CourseEnd 
Professor -> ProfessorEmail 

Multi-valued dependencies: 
Course ->> Professor 
Course ->> classRoom 
StudentID ->> Course 
StudentID ->> Professor 

The functional dependencies and multi-valued dependencies are taken as .txt files(functional_dependencies.txt,multivalued_dependencies.txt). 
User Input:
 • Choice of the highest normal form to read(1NF,2NF,3NF,BCNF,4NF,5NF).
 • Primary key used(StudentID, Course) Core Components:

Input Parser: The csv file and the txt file containing the functional dependencies are read by the parser function. It deconstructs the text into identifiable character strings.

Normalizer: Using the specified functional relationships, the Normalizer breaks down the input dataset into the necessary normal form. The provided dataset is broken down into the user-required normal form using the normalizing techniques.

SQL Query Generator: It refers to a tool or functionality that helps to generate the SQL queries.

Deliverables: Source Code: Here, we have used the Python programming language to normalize the given dataset.
Code Description:  
• The open method is used to open and read the functional dependencies txt file. 
• The Parser method is used to convert the given input files into the string characters. 
• bcnf_decomosition function is defined to decompose the relation into BCNF normal form. 
• in_1nf method is defined to check whether the dataset is in 1NF or not. 
• in_2nf method is defined to check whether the dataset is in 2NF or not. 
• in_3nf method is defined to check whether the dataset is in 3NF or not. 
• in_bcnf method is defined to check whether the dataset is in BCNF or not. 
• in_4nf method is defined to check whether the dataset is in 4NF or not. 
• in_5nf method is defined to check whether the dataset is in 5NF or not. 
• first_normal_form function is defined to decompose the given dataset into the 1NF. 
• second_normal_form function is defined to decompose the given dataset into the 2NF. 
• third_normal_form function is defined to decompose the given dataset into the 3NF. 
• bc_normal_form function is defined to decompose the given dataset into the BCNF. 
• fourth_normal_form function is defined to decompose the given dataset into 4NF. 
• decomposing_to_5nf function is defined to check for the lossless decomposition of 5NF. 
• fifth_normal_form function is defined to decompose the given dataset into 5NF. 
• output function is defined to generate the user required output results. 
• sql_query_1NF function is defined to print the 1NF sql query as an output. 
• sql_query_2_3 function is defined to print the 2NF, 3NF sql queries as output. 
• sql_query_BCNF_4_5 function is defined to print the BCNF, 4NF, 5NF sql queries as output. 
• Checking for the normal form of the given dataset whether it is in any type of normal form or not. 
• The highest normal form of the given dataset can be found by using the functions in_1nf, in_2nf, in_3nf, in_4nf, in_bcnf and in_5nf from the variable high_normalform.

Code Execution and Flow:

• Following code execution, the console will display the information shown below. • To normalize the provided table, enter the highest normal form by pressing 1 for 1NF, 2 for 2NF, 3 for 3NF, B for BCNF, 4 for 4NF, and 5 for 5NF. • Next, press 1 to obtain the supplied relation's highest normal form, and press 2 if the highest normal form is not needed. The primary key for this relation should be StudentID,Course. Then, insert the values for the primary key, separated by commas. 

• It offers the query of the decomposed tables after decomposing the given table till it satisfies the specified normal form if it is not in the provided normal form. • Otherwise, it returns the original table's query if the supplied table satisfies the given normal form. • The candidate keys for every table in the 5NF are supplied. The candidate key for the student table is StudentID; for the course table, it is Course; and for the professor table, it is Professor. • The highest normal form that the provided table can satisfy is shown at the end. Only 1NF is satisfied by the provided table.
