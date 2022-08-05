# Django

### 1. What is Django?
Django is an open-source, back-end serverside web framework which makes it easier to build 
web pages using Python. It is one of the most popular web server frameworks because it
enables rapid development of secure and maintainable websites.  


### 2. What are the benefits?
* can be used to build almost any type of website (e.g. cms, wikis, social networks, news sites etc.)
* everything needed is part of the one "product"
* provides a secure way to manage user accounts and passwords
* enables protection against many vulnerabilities by default (incl. SQL injection, cross-site scripting, cross-site request forgery)
* each part of the architecture is independent of the others, and can hence be replaced or changed if needed
* is written in Python (so it runs on many platforms)


### 3. What are the drawbacks?
* There are no conventions (the framework doesn’t have a set of principles that developers can follow for web development)
* is not suitable for smaller projects (too high-end, requires a lot of coding)
* The framework is considered as a single package, which is not a good thing. The lower dependencies Django have, the more code, developers will have to write.
* steep learning curve


### 4. What is an ORM?
Object-Relational Mapping is a technique that allows to query and manipulate data from 
a database using an object-oriented paradigm. An ORM library encapsulates the code needed 
to manipulate the data, so there is no need to use SQL anymore; we can interact directly with 
an object in the same language we're using.

Retrieving a dataset from the database example:  

Without ORM:

    book_list = new List();
    sql = "SELECT book FROM library WHERE author = 'Linus'";
    data = query(sql); // I over simplify ...
    while (row = data.next())
    {
    book = new Book();
    book.setAuthor(row.get('author');
    book_list.add(book);
    }

With ORM:

    book_list = BookTable.query(author="Linus");



### 5. Explain the Django architecture?


### 6. What is a Django Model?


### 7. What are "static files"?


### 8. What are middlewares?

