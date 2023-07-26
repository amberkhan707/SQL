# SQL
Here, you will learn SQL from basic to Advance


# What is SQL(Structured Query Language)?  
It is a Language that is used to Interact with Database. It is used to create table from an ER Model.
  
# Difference between SQL and MYSQL:
| SQL                           | MYSQL                                                     |    
| ----------------------------- | -------------                                             |   
| it is a query language        | itself a RDBMS(Relational Data Base Mangement System      |   
| way to access data            | server where data is accesed                              |   


# Install it in your PC   
u can watch the process of installation above in installation file  

# Datatypes  
No need to learn all the Data types:

# Data Types for Database Columns  
you can refer notes from notessql file.

  # LEARN CODE:
Let's take an example of bulding Banking RDBMS,  

*create table of entity and table column will be its attributes*  


Customer Table:  
customer_id: Unique identifier for each customer.  
first_name: Customer's first name.  
last_name: Customer's last name.  
email: Customer's email address.  
phone: Customer's phone number.  
   
  CREATE TABLE customer (  
    customer_id INT PRIMARY KEY AUTO_INCREMENT,  
    first_name VARCHAR(50) NOT NULL,  
    last_name VARCHAR(50) NOT NULL,  
    email VARCHAR(100) NOT NULL,  
    phone VARCHAR(20)  
);  
  
  
Designing a whole banking system involves a complex and comprehensive database schema. Below, I'll provide a high-level overview of the database schema for a basic banking system. Keep in mind that a real-world banking system would require much more detailed and sophisticated implementation, including security features, transaction handling, and compliance with banking regulations.

Let's design the basic database schema for a banking system:

Customer Table:
customer_id: Unique identifier for each customer.
first_name: Customer's first name.
last_name: Customer's last name.
email: Customer's email address.
phone: Customer's phone number.
sql
Copy code
CREATE TABLE customer (  
    customer_id INT PRIMARY KEY AUTO_INCREMENT,  
    first_name VARCHAR(50) NOT NULL,  
    last_name VARCHAR(50) NOT NULL,   
    email VARCHAR(100) NOT NULL,  
    phone VARCHAR(20)  
);    
   
Account Table:  
account_id: Unique identifier for each account.  
customer_id: Foreign key referencing the customer_id in the customer table to associate accounts with a specific customer.  
account_number: Unique account number.  
balance: Current balance in the account.  
  
  CREATE TABLE account (
    account_id INT PRIMARY KEY AUTO_INCREMENT,
    customer_id INT NOT NULL,
    account_number VARCHAR(20) NOT NULL UNIQUE,
    balance DECIMAL(15, 2) DEFAULT 0.00,
    FOREIGN KEY (customer_id) REFERENCES customer(customer_id)
);  

Transaction Table:  
transaction_id: Unique identifier for each transaction.  
account_id: Foreign key referencing the account_id in the account table to associate transactions with a specific account.  
transaction_type: Type of transaction (e.g., deposit, withdrawal, transfer).  
amount: Transaction amount (positive for deposits, negative for withdrawals).  
transaction_date: Timestamp for when the transaction occurred.  
  
 CREATE TABLE transaction (  
    transaction_id INT PRIMARY KEY AUTO_INCREMENT,  
    account_id INT NOT NULL,  
    transaction_type VARCHAR(20) NOT NULL,  
    amount DECIMAL(15, 2) NOT NULL,  
    transaction_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,  
    FOREIGN KEY (account_id) REFERENCES account(account_id)  
);  

  Loan Table:  
loan_id: Unique identifier for each loan.  
customer_id: Foreign key referencing the customer_id in the customer table to associate loans with a specific customer.   
loan_amount: The initial loan amount.  
interest_rate: The interest rate for the loan.  
start_date: The start date of the loan.  
end_date: The end date of the loan.  
status: The status of the loan (e.g., active, paid off).  
  
 CREATE TABLE loan (  
    loan_id INT PRIMARY KEY AUTO_INCREMENT,  
    customer_id INT NOT NULL,  
    loan_amount DECIMAL(15, 2) NOT NULL,  
    interest_rate DECIMAL(5, 2) NOT NULL,  
    start_date DATE NOT NULL,  
    end_date DATE NOT NULL,  
    status VARCHAR(20) NOT NULL,  
    FOREIGN KEY (customer_id) REFERENCES customer(customer_id)  
);  
   
  Loan Payment Table:  
payment_id: Unique identifier for each loan payment.   
loan_id: Foreign key referencing the loan_id in the loan table to associate payments with a specific loan.  
payment_amount: The amount of the loan payment.  
payment_date: Timestamp for when the payment was made.  
    
  CREATE TABLE loan_payment (  
    payment_id INT PRIMARY KEY AUTO_INCREMENT,  
    loan_id INT NOT NULL,  
    payment_amount DECIMAL(15, 2) NOT NULL ,  
    payment_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,  
    FOREIGN KEY (loan_id) REFERENCES loan(loan_id)  
);  
  

*Go through sql cheat sheet to memorize code*


                                                       *practice practice practice*   
  
