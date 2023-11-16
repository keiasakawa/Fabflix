

- # General
    - #### Team#: 32
    
    - #### Names: Kei Asakawa, Qinyu Chen
    
    - #### Project 5 Video Demo Link:https://www.youtube.com/watch?v=U7TQmudM_qc

   



    

- # JMeter TS/TJ Time Logs
    - #### Instructions of how to use the `log_processing.*` script to process the JMeter logs.
        

- # JMeter TS/TJ Time Measurement Report

| **Scaled Version Test Plan**          | **Graph Results Screenshot** | **Average Query Time(ms)** | **Average Search Servlet Time(ms)** | **Average JDBC Time(ms)** | **Analysis** |
|------------------------------------------------|------------------------------|----------------------------|-------------------------------------|---------------------------|--------------|
| Case 1: HTTP/1 thread                          | ![Thread_1](https://github.com/uci-jherold2-teaching/cs122b-fall-team-32/blob/main/img/thread1.png)   | ??                         | ??                                  | ??                        | ??           |
| Case 2: HTTP/10 threads                        | ![Thread_10](https://github.com/uci-jherold2-teaching/cs122b-fall-team-32/blob/main/img/thread10.png)   | ??                         | ??                                  | ??                        | ??           |
| Case 3: HTTPS/10 threads                       | ![](path to image in img/)   | ??                         | ??                                  | ??                        | ??           |
| Case 4: HTTP/10 threads/No connection pooling  | ![thread8080](https://github.com/uci-jherold2-teaching/cs122b-fall-team-32/blob/main/img/thread10_8080.png)   | ??                         | ??                                  | ??                        | ??           |

| **Single Version Test Plan**                   | **Graph Results Screenshot** | **Average Query Time(ms)** | **Average Search Servlet Time(ms)** | **Average JDBC Time(ms)** | **Analysis** |
|------------------------------------------------|------------------------------|----------------------------|-------------------------------------|---------------------------|--------------|
| Case 1: HTTP/1 thread                          | ![](path to image in img/)   | ??                         | ??                                  | ??                        | ??           |
| Case 2: HTTP/10 threads                        | ![](path to image in img/)   | ??                         | ??                                  | ??                        | ??           |
| Case 3: HTTP/10 threads/No connection pooling  | ![](path to image in img/)   | ??                         | ??                                  | ??                        | ??           |

## deploy the project on Tomcat

<ol>
  <li>navigating into the root of project repo where the pom.xml is
  
   
    cd cs122b-fall-team-32
    
  </li>
<li>creating the war file: <br/>

```
mvn package
```

</li>
<li>
copying the newly created war file into the webapps folder under tomcat9:

```
cp cs122b-fall-team-32/target/*.war ./tomcat/webapps/
```

</li>
</ol>

## How to use Connection Pooling
#### Include the filename/path of all code/configuration files in GitHub of using JDBC Connection Pooling.
<ul>
<li>
AddMovieServlet
</li>
<li>
AutocompleteServlet
</li>
<li>
CartServlet
</li>
<li>
CheckOutServlet
</li>
<li>
DashboardServlet
</li>
<li>
EmployeeServlet
</li>
<li>
FirstLetterServlet
</li>
<li>
GenresServlet
</li>
<li>
GetGenresServlet
</li>
<li>
LoginServlet
</li>
<li>
MoviesServlet
</li>
<li>
SearchServlet
</li>
<li>
SingleMovieServlet
</li>
<li>
SingleStarServlet
</li>
<li>
StarsServlet
</li>
</ul>

#### Explain how Connection Pooling is utilized in the Fabflix code.
Connection Pooling is utilized by each servlet that requires connection to the backend database
 
#### Explain how Connection Pooling works with two backend SQL.
Connection Pooling works with two backend SQL by sending read/write requests to one backend while only read requests are sent to another
These read requests are then split between the two backend and balanced

# Master/Slave
#### Include the filename/path of all code/configuration files in GitHub of routing queries to Master/Slave SQL.
/etc/apache2/sites-enabled/000-default.conf

#### How read/write requests were routed to Master/Slave SQL?
Another resource was added that redirected only to the master instance and this resource was used for servlets that required write requests.

## Contributions of each team member

Kei Asakawa: Implemented task 1-3

Qinyu Chen: Implemented task4, helped with task3


