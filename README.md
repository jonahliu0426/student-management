# student-management
1. Download files
2. Open terminal and direct to the location of the files then run command: './mvnw spring-boot:run'. (or you can just open it in IDE and run the program)
3. Open your browser and go to: localhost:8080/api/student.
4. You will see simple student information in JSON format.

In order to perform post method, you can use Postman, 
before sending, you should click the Authentication bar,
and type in the username and password

 username: root
 
 password: 11111

GET:

1. localhost:8080/api/student -> return all students info

2. localhost:8080/api/student/name?name={param1}&age={param2} -> return all students whose name equals to the name specified in param1, and whose age equals to specified in param2

3. localhost:8080/api/class   -> return all classes info

4. localhost:8080/api/student/contain_name?name={parameter} -> return all students whose name contains the character specified in the parameter
          

POST:

1. localhost:8080/api/class/add, 
In the body bar, select row button, and chenge the format to JSON, next type in  the param key and value in JSON format.

for example:
{
  "year":2022,
  "number":1
}

then click SEND, you should see the class is added to the database, and you can check it by performing a GET method via localhost:8080/api/class.

2. localhost:8080/api/student/register

   {
     "name": "Dave"
   }
   
   If successful, Postman console will display a returned string as following: "Registered student, Primary ID: {student id} Name: {student name}".
   

3. localhost:8080/api/student/assignclass/{sid}/{cid}
   
   for example: localhost:8080/api/student/assignclass/7/2, will assign the student with student id 7 to class with class id 2
   
   if success, Postman console will display a returned string as following: "Assigned class. Primary ID {class id} to {student name}"

   
