# Hands-on Lab : CREATE, ALTER, TRUNCATE, DROP

In this lab, you will learn how to create tables and load data using the phpMyAdmin graphical user interface (GUI) tool in the MySQL database service.
Instructions: source https://www.phpmyadmin.net/
![image](https://github.com/user-attachments/assets/904e3604-76d9-4cba-9c3b-b21ecc965e08)
Then, you can create a new database
![image](https://github.com/user-attachments/assets/8dedccad-1256-44b4-9554-d491dfdc99de)

Add a name and create
![image](https://github.com/user-attachments/assets/f717dc75-9eb2-441e-bc87-f8188626bd27)

Click on SQL to run the code:
![image](https://github.com/user-attachments/assets/9bcc6985-ac83-4c2e-9864-7e050f70e4e6)

Paste the code and run it:
![image](https://github.com/user-attachments/assets/8ed7e345-a409-4989-808b-df23d93c9fc9)

Click again in sql and run some code to populate the table:
![image](https://github.com/user-attachments/assets/4d591ffd-b22d-42ae-a12f-c08d39eeff58)


## QUIZ


![image](https://github.com/user-attachments/assets/b5520d02-1204-4bd1-8b5a-2ff24f52a9ab)


![image](https://github.com/user-attachments/assets/c5db66e5-e3e7-4d3c-a124-b965e2deb556)



- Q1) Solution 
```
CREATE TABLE Toys (
        ID INTEGER NOT NULL,
        Variety VARCHAR(20),
        Quantity INTEGER
        );
```
- Q2) Solution
```
  INSERT INTO TOYS VALUES
        (1,'Chew toy',20),
        (2,'Balls',50),
        (3,'Bowls',30),
        (4,'Foldable bed',40);
 
SELECT * FROM TOYS
```

- Q3) Solution
```
ALTER TABLE TOYS
MODIFY Variety VARCHAR(30);
```

- Q4) Solution
```
 TRUNCATE TABLE TOYS;
```

- Q5) Solution
  ```
  DROP TABLE TOYS;
  ```
