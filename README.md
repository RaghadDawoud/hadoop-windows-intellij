# hadoop-windows-intellij
The solution of java.lang.NullPointerException error while running Hadoop code locally on intellij on Windows

Resolving java.lang.NullPointerException while running hadoop locally on windows 11

With Intellij, you don't need to use a cluster or configure the Hadoop and/or Spark environments on your own computer in order to build and test your programs using Maven.

If you tried to run your Hadoop code locally on intellij on Windows you might get the java.lang.NullPointerException error:
 
 
You can solve this problem by following these steps:

1-	Step 1: Create a directory
Go to This PC -> Widows (C:) -> create a new folder and name it “hadoop”

 

Create a new folder inside “hadoop” folder that you created in the previous step and name it “bin”
 
	
2-	Step 2: Download the file winutils.exe from this page on GitHub (https://github.com/steveloughran/winutils/tree/master/hadoop-2.7.1/bin)

 

Download winutils.exe in “bin” folder as shown below: 

 




 
	
Next download the hadoop.dll file the same way you downloaded winutils.exe in “bin” folder as shown:

 



 

Note: the version of winutils.exe and Hadoop.dll should be the same.


3-	Step 3: go to system environment variables and create a new environment variable: HADOOP_HOME then enter the path to the folder where the winutils.exe file is located:
HADOOP_HOME=C:\hadoop\bin

 




 


 




 


 
Next go to Path -> double click on Path -> create a new path %HADOOP_HOME%\bin as shown below then click on ok on all windows:
 

Finally: go to intellij and test your code the problem should be solved, and you can run the code successfully!
 

Note: if the error still the same the version of winutils.exe might be incompatible with your system, try to download another version.
