---
title: "How to get a procedure's definition in MSSQL"
draft: false
---

If you are new to a legacy database and want to learn more about its internals, sometimes it's good to read the definitions of stored procedures.
It can teach you what standard to follow and how exactly are the data stored. To do this, run the following query:

```
sp_helptext PROCEDURE
```

This should get you the definitions.