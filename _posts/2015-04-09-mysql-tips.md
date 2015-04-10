---
layout: post
title: MySQL Tips
---

I haven't posted in a while, but I have gotten a lot of homework done. Which is a really good thing. One of the classes I have gotten a lot done in is my Database Design class. It is a pretty simple laidback class for being an upper division course. I mean its course number is CS4307, which is pretty far up there. Anyways, what I want to share today is how to do some basic MySQL and then transition into some more difficult ones. First, [here](https://github.com/ZachCustomBit/School/tree/master/cs-2420) is a link to my Github Repo that has all my MySQL scripts for the class if anyone is interested.

One of the very first things I learned when I was learning MySQl was how to insert into a table. It is rather simple, you just need to know the name of your table, the column names, and the values you want to insert into your table. An example would be like this

`INSERT INTO table_name (column1, column2, column3) VALUES (value1, value2, value3);`

MySQL isn't case sensitive, but it is good form to capitalize all the statements. This makes it much easier to read. I recently learned that if you are going to be filling every column, and you know the order you can simplify the above query to

`INSERT INTO table_name VALUES (value1, value2, value3);`

This is rather nice when you are creating a new record from an online form in PHP because you will usually be filling every column so you can just leave out the column names and save yourself a good amount of time and headache. Because I don't know about you but, I do know that for me MySQL queries can get long and confusing very fast.

Let's go into something more difficult UNION SELECTS! These things are pretty tricky. I will be showing an example I did in class. My teacher had one suggestion for the class, and it was "Good luck everyone. When I do UNION SELECTS I just fool around until I get the answer I want and don't touch it ever again!" Let's just say I was less than pleased with that sage advice. Anyways this is my example on how to do a `UNION SELECT` with the widely known spj database. Which can be downloaded at the bottom of the page [here](http://cit.dixie.edu/it/4300/). What we are trying to get returned in this example is every city that has either a supplier or a job. A supplier can be found in the `s` table, and a job can be found in the `j` table. Thus we need to perform a `UNION SELECT` to get the cities that have a supplier or a job.

`SELECT DISTINCT city FROM s UNION SELECT city FROM j;`

Which will return us the statement of

```
--------------

+--------+
| city   |
+--------+
| London |
| Paris  |
| Athens |
| Rome   |
| Oslo   |
+--------+
5 rows in set (0.00 sec)

--------------
```

I am going to end this post here, but I'll post again about MySQL because there is a lot more to go into. If you have any requests, such as Sub Selects, or Joins just comment below, and I'll focus more on them.

Thanks for reading!
