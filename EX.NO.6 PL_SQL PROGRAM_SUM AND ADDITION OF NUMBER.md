# Ex. No: 6 PL/SQL program to perform addition and subtraction of two number 
### DATE: 
### AIM: To create PL/SQL program to perform addition and subtraction of two number.

### Steps:
1. Declare the variable a, b and necessary variables in Declare section.
2. Perform addition of two numbers
3. Perform subtraction of two numbers 
4. Display the result 
5. End the begin section.

### Program:
```
DECLARE
 a NUMBER := 550;
 b NUMBER := 450;
 c NUMBER;
BEGIN
 c:=a+b;
 dbms_output.Put_line('addition of two numbers is '||c);
 c:=a-b;
 dbms_output.Put_line('subtraction of two numbers is '||c);
END;
```

### Output:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/5351d328-dc16-4840-869b-8866b7339a37)


### Result:
Thust the program was performed sucessfully.
