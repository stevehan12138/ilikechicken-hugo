---
title: "How to connect to your Pythonanywhere database remotely"
draft: false
---

Pythonanywhere is an excellent place to run your python code and your website, it offers multiple consoles and database.  
When you are debugging your code, and it uses a database, such as a website, it can be quite tedious to set up another mysql server when you don’t have another cloud service such as Azure or AWS. In that case, you can just use the database from Pythonanywhere.  

The database can’t be directly connected, so that you would need SSH tunneling. Open up a terminal, type:

```
ssh -L 3306:username.mysql.pythonanywhere-services.com:3306 username@yoursshhostname
```

Replace username with your username, and your ssh host name is either ssh.pythonanywhere.com or ssh.eu.pythonanywhere.com depending on where you live.
After that, you should be connected to the server. Now, just open another console and proceed to use the database as normal.
You can find other ways to set up in the official document:  

https://help.pythonanywhere.com/pages/AccessingMySQLFromOutsidePythonAnywhere/