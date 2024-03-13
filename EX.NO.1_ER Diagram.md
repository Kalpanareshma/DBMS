# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 
![image (2)](https://github.com/Kalpanareshma/DBMS/assets/122040453/a272272d-7aa3-4d6c-8353-8c9cd5a00c46)



### Relational model
![image (3)](https://github.com/Kalpanareshma/DBMS/assets/122040453/bf56970b-6598-469d-bf3f-37db091eda82)



### SQL DDL Schema 
```
CREATE TABLE BANK
(
  Code INT NOT NULL,
  Name INT NOT NULL,
  Addr INT NOT NULL,
  PRIMARY KEY (Code)
);

CREATE TABLE BANK_BRANCH
(
  Branch_no INT NOT NULL,
  Addr INT NOT NULL,
  PRIMARY KEY (Branch_no)
);

CREATE TABLE LOAN
(
  Loan_no INT NOT NULL,
  Amount INT NOT NULL,
  Type INT NOT NULL,
  PRIMARY KEY (Loan_no)
);

CREATE TABLE CUSTOMER
(
  Phone INT NOT NULL,
  Ssn INT NOT NULL,
  Name INT NOT NULL,
  Addr INT NOT NULL,
  PRIMARY KEY (Ssn)
);

CREATE TABLE ACCOUNT
(
  Acct_no INT NOT NULL,
  Balance INT NOT NULL,
  Type INT NOT NULL,
  PRIMARY KEY (Acct_no)
);

```


## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
