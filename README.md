# RDBMS Normalizer

Team members: Madhusudhan Byru(12611642) and Guru Sai Prasad Sunkara(12608151)
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
• The parserFile method is used to convert the given input files into the string characters. 
• bcnfDecomposition function is defined to decompose the relation into BCNF normal form. 
• check1NF method is defined to check whether the dataset is in 1NF or not. 
• check2NF method is defined to check whether the dataset is in 2NF or not. 
• check3NF method is defined to check whether the dataset is in 3NF or not. 
• checkBCNF method is defined to check whether the dataset is in BCNF or not. 
• check4NF method is defined to check whether the dataset is in 4NF or not. 
• check5NF method is defined to check whether the dataset is in 5NF or not. 
• normalizeTo1NF function is defined to decompose the given dataset into the 1NF. 
• normalizeTo2NF function is defined to decompose the given dataset into the 2NF. 
• normalizeTo3NF function is defined to decompose the given dataset into the 3NF. 
• normalizeToBCNF function is defined to decompose the given dataset into the BCNF. 
• normalizeTo4NF function is defined to decompose the given dataset into 4NF. 
• checkLosslessFor5NF function is defined to check for the lossless decomposition of 5NF. 
• normalizeTo5NF function is defined to decompose the given dataset into 5NF. 
• outputTypeMethod function is defined to generate the user required output results. 
• get1NF(primary_keys, df) function is defined to print the 1NF sql query as an output. 
• sql_query(twonf_tables) and sql_query(threenf_tables) calls are used to print the 2NF, 3NF sql queries as output. 
• sql_query(bcnf_tables), sql_query(fournf_tables), and sql_query(fivenf_tables) function is defined to print the BCNF, 4NF, 5NF sql queries as output. 
• Checking for the normal form of the given dataset whether it is in any type of normal form or not. 
• The highest normal form of the given dataset can be found by using the functions in_1nf, in_2nf, in_3nf, in_4nf, in_bcnf and in_5nf from the variable high_normalform.

Code Execution and Flow:

• Following code execution, the console will display the information shown below. • To normalize the provided table, enter the highest normal form by pressing 1 for 1NF, 2 for 2NF, 3 for 3NF, B for BCNF, 4 for 4NF, and 5 for 5NF. • Next, press 1 to obtain the supplied relation's highest normal form, and press 2 if the highest normal form is not needed. The primary key for this relation should be StudentID,Course. Then, insert the values for the primary key, separated by commas. 

• It offers the query of the decomposed tables after decomposing the given table till it satisfies the specified normal form if it is not in the provided normal form. • Otherwise, it returns the original table's query if the supplied table satisfies the given normal form. • The candidate keys for every table in the 5NF are supplied. The candidate key for the student table is StudentID; for the course table, it is Course; and for the professor table, it is Professor. • The highest normal form that the provided table can satisfy is shown at the end. Only 1NF is satisfied by the provided table.


Challenges faced:
1. Implementing Algorithms:
  The normalization methods required careful attention to detail as they were being coded. A thorough grasp of functional   connections was necessary because each normal form has unique needs and guidelines for spotting infractions. The implementation of checks for different forms, including 1NF, 2NF, and BCNF, required a thorough relational design approach. It was also difficult to make sure the algorithms could correctly decompose relations without introducing redundancy or missing important information. It was essential to test the algorithms on a variety of datasets in order to find potential flaws and edge situations. To make sure the algorithms operated properly in a variety of situations, this process of improvement and debugging was crucial.

2. Data Types and SQL Compatibility
   During the project, there were many difficulties in mapping Python data types to SQL data types. Because each programming language has a unique set of data types, it was necessary to have a solid understanding of both systems in order to ensure compatibility when creating SQL queries. Complexity was increased by the requirement to translate different Python kinds—such as dates, strings, floats, and integers—into their corresponding SQL types. The mapping procedure was further complicated by taking into account database restrictions such as primary keys, foreign keys, and unique constraints. The significance of accuracy in database architecture was highlighted by the extensive testing required to guarantee that the generated SQL queries ran correctly without type-related errors or mismatches.



