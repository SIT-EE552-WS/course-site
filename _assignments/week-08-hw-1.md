---
title: Maven Dependencies
week: 8
homework: 1
---

The directory structure of this week's assignments is a bit different than you're used to. They are now structured according 
to the conventions expected by the Maven build tool.  You will find the `.java.` files in `src/main/java` (or `src\main\java` 
if you're on Windows).  The project is configured based on the `pom.xml` at the top of the project folder.

You can run this project in the command line with this command:

```
mvn compile exec:java
```

BUT if you try that right now, you will get an error.  That's because this project has a missing dependency to Apache PDF Box.  To make it run,
add a dependency to version `2.0.21` of the library.

Once you add the dependency, running the command above again should produce an empty PDF file.  In `Main.java` there is some code commented out. 
Uncomment this code and modify it so that it prints your name in the PDF.

Submit your PDF along with your updated code.
