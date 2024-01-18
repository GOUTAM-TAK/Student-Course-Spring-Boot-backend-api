. Develop a backend using Spring Boot , REST API , Spring Data JPA for student admission.

End points to develop
1. Launch new course
JSON request payload : course details (except course id)
eg : course title(unique) , start date , end date , fees , min score
This should add a record in the courses table.
Return suitable response.
(Hint : ApiRespone with string mesg is desirable. But even if you return a string mesg , it's also acceptable)
eg URL : http://host:port/courses, method=POST

2. Add student details
Json request payload : student details + course id
eg : first name , last name , email , course id,score obtained.
This should add a record in students table if the admission is granted(score based)  , with the foreign key of course_id set.
If the score is less , do not add a record.
Return suitable response.
(Hint : ApiRespone with string mesg is desirable. But even if you return a string mesg , it's also acceptable)
eg URL : http://host:port/students, method=POST

3. View all students , for a specific course
i/p : course title
Send the i/p using a path variable
eg URL for a course title , Mastering_Java
 : http://host:port/students/course_title/Mastering_Java 
method=GET

4. Update course fees
i/p : course id n updated fees.
eg URL : for a course id=10 n updated fees =25000
 http://host:port/courses/10/fees/25000
method=PUT

5. Cancel Student admission
i/p : course id n student id
eg URL : for a course id=10 n student id=20
 http://host:port/courses/10/students/20
method=DELETE

Develop this app in a layered manner
Rest Controller --Service --DAO --Entities --DB
