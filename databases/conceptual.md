### Conceptual Exercise

Answer the following questions below:

- What is PostgreSQL?
  - PostgreSQL, also known as Postgres, is a powerful open-source relational database management system (RDBMS). It is widely used for storing and managing structured data in various applications and industries. PostgreSQL offers robust features, scalability, and reliability, making it a popular choice for both small and large-scale projects.

- What is the difference between SQL and PostgreSQL?
  - SQL and PostgreSQL are related but distinct concepts:
  - SQL (Structured Query Language): SQL is a standardized programming language used for managing and manipulating relational databases. It provides a set of commands (queries) to create, retrieve, update, and delete data stored in a relational database. SQL is a language specification and not a specific database system
  - PostgreSQL: PostgreSQL, on the other hand, is an open-source relational database management system (RDBMS) that implements the SQL language. It is one of many database systems that support SQL. PostgreSQL extends the SQL standard by adding its own additional features, functions, and data types.
  - In summary, SQL is the language used to interact with databases, while PostgreSQL is a specific database management system that uses SQL as its querying language. SQL can be used with different database systems, such as PostgreSQL, MySQL, Oracle, SQL Server, etc. Each database system, including PostgreSQL, may have its own unique features and capabilities in addition to supporting the SQL language.

- In `psql`, how do you connect to a database?
  - To connect to a PostgreSQL database using the psql command-line tool, you can follow these steps:
  - Open a terminal or command prompt on your system.
  - Type the following command to connect to a PostgreSQL database: 
    - psql -h <host> -p <port> -U <username> -d <database_name>
  - Replace <host>, <port>, <username>, and <database_name> with the appropriate values for your PostgreSQL setup.

  - Press Enter to execute the command. If the connection is successful, you will be prompted to enter the password for the specified username. Enter the password and press Enter.
  - If the provided information is correct, psql will establish a connection to the specified PostgreSQL database, and you will see a command prompt indicating that you are connected.

  - If any of the connection parameters are omitted, psql will assume default values. For example, if you don't specify a host, it will default to connecting to the local machine; if you don't specify a port, it will default to using port 5432.


- What is the difference between `HAVING` and `WHERE`?
  - WHERE is used to filter rows based on conditions before any grouping or aggregation
  - HAVING is used to filter groups of rows after grouping and aggregation based on aggregate conditions.

- What is the difference between an `INNER` and `OUTER` join?
  - An INNER join returns only the matching rows between tables
  -  OUTER join includes both matching and non-matching rows.

- What is the difference between a `LEFT OUTER` and `RIGHT OUTER` join?
  - A LEFT OUTER join includes all rows from the left table and matching rows from the right table
  - RIGHT OUTER join includes all rows from the right table and matching rows from the left table.

- What is an ORM? What do they do?
  - An ORM (Object-Relational Mapping) is a programming technique that allows developers to interact with a relational database using object-oriented models. It automates tasks such as data mapping, querying, and managing relationships between objects and database tables, providing a higher-level abstraction for database operations. ORMs simplify database access, enhance code maintainability, and promote faster development by leveraging object-oriented principles.

- What are some differences between making HTTP requests using AJAX 
  and from the server side using a library like `requests`?
- AJAX requests are made from the client-side using JavaScript, while server-side requests using requests library are executed on the server. AJAX requests are asynchronous and subject to same-origin policy, while requests requests are synchronous and not subject to same-origin restrictions. AJAX requests are often triggered by user actions, while requests requests can be initiated programmatically on the server. AJAX requests are primarily used for frontend interactivity, while requests is used for backend operations and server-to-server communication.
  

- What is CSRF? What is the purpose of the CSRF token?
  - CSRF stands for Cross-Site Request Forgery, which is a type of web security vulnerability. It occurs when an attacker tricks a user's web browser into making unintended and potentially malicious requests to a target website where the user is authenticated.
  - The purpose of a CSRF token is to mitigate CSRF attacks. It is a unique token generated by the server and included in each HTML form or request. The token acts as a security measure to validate that the request originates from a trusted source and not from a malicious attacker.
  - When a user submits a form or performs an action that requires a server request, the CSRF token is included in the request. The server then checks the received token against the expected value stored on the server. If the tokens match, the request is considered legitimate, and the server processes it. If the tokens don't match or the token is missing, the server can reject the request as a potential CSRF attack.
  - By requiring and validating CSRF tokens, websites can ensure that the requests made by users originate from their own sessions and not from forged or malicious sources. This helps protect against unauthorized actions performed on behalf of the user.
  - In summary, a CSRF token is a security mechanism used to protect against Cross-Site Request Forgery attacks. It verifies that requests come from legitimate sources and prevents unauthorized actions on behalf of users.

- What is the purpose of `form.hidden_tag()`?
  - In the context of Flask, form.hidden_tag() is a function provided by the Flask-WTF extension, which is used in conjunction with Flask-WTF forms.
  - The purpose of form.hidden_tag() is to generate HTML code for rendering hidden input fields in a form. Hidden input fields are not visible to users but can be submitted along with the form data. They are often used to include additional information or tokens that need to be passed to the server but are not meant to be seen or modified by users.
  - The primary use case for form.hidden_tag() is to include the CSRF (Cross-Site Request Forgery) token as a hidden field in the form. By rendering the CSRF token as a hidden input field, it ensures that the token is submitted with the form data, allowing the server to validate the authenticity of the request and protect against CSRF attacks.
  - To use form.hidden_tag(), you typically include it in the form template using {{ form.hidden_tag() }}. This will generate the HTML code for the hidden fields, including the CSRF token if CSRF protection is enabled.
  - In summary, form.hidden_tag() is used to generate HTML code for rendering hidden input fields, primarily to include the CSRF token in a form for protection against CSRF attacks.
