![image](https://github.com/LimiaSadinaSathi/Prison_Management_System/assets/77088710/6acb7785-80fb-4b91-8485-3257f747602e)# Prison_Management_System
Entity Relationship (ER) Diagram:
![image](https://github.com/LimiaSadinaSathi/Prison_Management_System/assets/77088710/c2b97115-9b89-483e-aaa8-1a86e6834b00)


Normalization:
Superintend (Prison code, name, capacity, officer’s id, name, age, contact no, batch, rank, shift).
1NF: Contact no is a multivalued attribute.
2NF:
Prison code, name, capacity.
Officers id, name, age, contact no, batch, rank, shift.
3NF:
Prison code, name, capacity.
Officers id, name, age, batch, rank, shift.
Officers id, contact no.

TABLES FROM SUPERINTED:
1. Prison code, name, capacity
2. Officers id, name, age, batch, rank, shift, prison code
3. Officers id, contact no - composite pk.
Register (Officers id, name, age, contact no, batch, rank, shift, case id, case type, issue date).
1NF: Contact no is a multivalued attribute.
2NF:
Officers id, name, age, contact no, batch, rank, shift.
Case id, case type, issue date.
3NF:
Officers id, name, age, batch, rank, shift.
Officers id, contact no.
Case id, case type, issue date.

Tables from Register:
1. Officers id, name, age, batch, rank, shift, case id.
2. Officers id, contact no.
3. Case id, case type, issue date.
Distributed by (Officers id, name, age, contact no, batch, rank, shift, Id, name, contact no).
1NF: Contact no is a multivalued attribute’s.
2NF:
Officers id, name, age, contact no, batch, rank, shift.
Id, name, contact no.
3NF:
Officers id, name, age, batch, rank, shift.
Officers id, contact no.
Id, name, contact no.
Id, contact no.

Tables from Distributed by:
1. Officers id, name, age, batch, rank, shift, id.
2. Officers id, contact no.
3. Id, name, contact no.
4. Id, contact no.
Guard (Id, name, contact no, number, capacity).
1NF: Contact no is a multivalued attribute’s.
2NF:
Id, name, contact no.
Number, capacity.
3NF:
Id, name.
Id, contact no.
Number, capacity.

Tables from guard:
1. Id, name, contact no, number.
2. Id, contact no.
3. Number, capacity.
Stay in (Number, capacity, prisoner id, name, date of in, age, gender, blood group, work type, eat).
1NF: There is no multivalued attributes.
2NF:
Number, capacity.
Prisoner id, name, date of in, age, gender, blood group, work type, eat.
3NF:
Number, capacity.
Prisoner id, name, date of in, age, gender, blood group, work type, eat.

Tables from Stay in:
1. Number, capacity.
2. Prisoner id, name, date of in, age, gender, blood group, work type, Number.
Visit (Prisoner id, name, date of in, age, gender, blood group, work type, eat, visitor’s id, name, phone number, relation with prisoner).
1NF: Phone number is a multivalued attribute.
2NF:
Prisoner id, name, date of in, age, gender, blood group, work type, eat.
Visitors id, name, phone number, relation with prisoner.
3NF:
Prisoner id, name, date of in, age, gender, blood group, work type, eat.
Visitors id, name, relation with prisoner.
Visitors id, phone number.

Tables from Visit:
1. Prisoner id, name, date of in, age, gender, blood group, work type, visitors id.
2. Visitors id, name, relation with prisoner.
3. Visitors id, phone number.
   
Final Table:
Prison code, name, capacity, - prison.
Officers id, contact no - composite pk- officer contact (one- many).
Officers id, name, age, batch, rank, shift, case id, constable id, Prison code - officer’s.
Case id, case type, issue date- prisoners case.
Constable Id, mobile no –constable contact (one –many).
Constable Id, name, contact no, number- constable.
Number, capacity - prison cell- (one-many).
Prisoner id, name, date of in, age, gender, blood group, work type, Number, case id, Visitor’s id- Prisoners.
Visitor’s id, name, relation with prisoner- Visitors.
Visitor’s id, phone number - visitor contact (one-many).

Table creation: 
Prison Table: 
![image](https://github.com/LimiaSadinaSathi/Prison_Management_System/assets/77088710/8d951e58-1275-4b82-b173-0a5b99ff801c)
  
Officer’s Table: 
![image](https://github.com/LimiaSadinaSathi/Prison_Management_System/assets/77088710/746d0c18-478e-471e-af32-49d6e1ffa66d)

Prisoner’s case Table: 
  
Constable Table:
 
 	 
 
Prisoner’s Table: 
  
Visitor’s Table: 
 
 
Prison Cell Table: 
  
Officer’s Contact Table: 
 
 
Constable Contact Table: 
  
Constable Contact Table: 
 
 
Insertion: 
Prison Table: 
  
Officer’s Table: 
  
 
Constable Table: 
  
Visitor’s Table: 
 
Prisoner’s Case Table: 
  
Prisoner Table: 
 
Prison Cell Table: 
  
Officer Contact Table: 
 
Constable Contact Table: 
  
Visitor Contact Table: 
 

