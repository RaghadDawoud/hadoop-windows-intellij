# Resolving java.lang.NullPointerException while running hadoop locally on windows 11
---
With Intellij, you don't need to use a cluster or configure the Hadoop and/or Spark environments on your own computer in order to build and test your programs using Maven.

If you tried to run your Hadoop code locally on intellij on Windows you might get the java.lang.NullPointerException error:
 




 


 




 


 
Next go to Path -> double click on Path -> create a new path %HADOOP_HOME%\bin as shown below then click on ok on all windows:
 

Finally: go to intellij and test your code the problem should be solved, and you can run the code successfully!
 

Note: if the error still the same the version of winutils.exe might be incompatible with your system, try to download another version.
