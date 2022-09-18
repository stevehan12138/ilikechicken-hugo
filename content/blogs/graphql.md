---
title: "What Is GraphQL"
draft: false
---

GraphQL is a new data API developed by Facebook.
It can be added directly to your existing databases and provides a clear way to request data.
For example, if you want everyone's name in the database, you can just do:

```
Query query {
    People {
        Name
        Age
    }
}
```

It is a lot easier to use compared to traditional REST APIs. 
The best thing is, you can use more than one database. 
For example, you can have your user data stored locally, and have some other information stored somewhere else and accessed through REST APIs. 
Even though you only have one REST database, GraphQL can be applied directly to your old codes, without rewriting anything.


Therefore, if you are looking for a new way to store data, GraphQL is a good one. It provides easy access to data, multiple database support, and no rewrites required.