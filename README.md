# Resolving java.lang.NullPointerException while running hadoop locally on windows 11

With Intellij, you don't need to use a cluster or configure the Hadoop and/or Spark environments on your own computer in order to build and test your programs using Maven.

If you tried to run your Hadoop code locally on intellij on Windows you might get the java.lang.NullPointerException error:

![photo_5994413562593920205_w](https://github.com/user-attachments/assets/79332b39-7c13-4a12-a653-d14044fd1744)

![photo_5994413562593920206_w](https://github.com/user-attachments/assets/a3441619-0394-4b1f-b888-deae0f4fa67f)

## You can solve this problem by following these steps:

#### 1. Step 1: Create a directory

> Go to This PC -> Widows (C:) -> create a new folder and name it “hadoop”
>
> ![first step](https://github.com/user-attachments/assets/406e7ef9-7fa2-4c99-8d2f-aa9a61578d1f)
>
> Create a new folder inside “hadoop” folder that you created in the previous step and name it “bin”
>>
>> ![2](https://github.com/user-attachments/assets/a9928295-af5d-4565-846e-d49f85bf4b90)
>>
>>


#### 2.	Step 2: Download the file winutils.exe from this page on GitHub 

> https://github.com/steveloughran/winutils/tree/master/hadoop-2.7.1/bin
>
> ![winutils github](https://github.com/user-attachments/assets/2011ac8e-2a40-46c8-a433-3febe977728d)
>
> Download winutils.exe in “bin” folder as shown below:
>
> ![download winutils](https://github.com/user-attachments/assets/4dc809cf-a64a-4735-8a9c-0472e89fbf01)
>
> ![save winutils](https://github.com/user-attachments/assets/266ec36d-c353-46c7-ba28-3e351b821a9e)
>
> Next download the hadoop.dll file the same way you downloaded winutils.exe in “bin” folder as shown:
>>
>> ![hadoopdll github](https://github.com/user-attachments/assets/3d638692-7d6c-42e3-9262-884389a52cdc)
>> ![download hadoopdll new](https://github.com/user-attachments/assets/6b0d3e59-3d06-458f-a47d-2bd8f442e5ca)
>> Note: the version of winutils.exe and Hadoop.dll should be the same
>>
>>


#### 3.	Step 3: go to system environment variables

> create a new environment variable: HADOOP_HOME then enter the path to the folder where the winutils.exe file is located:
HADOOP_HOME=C:\hadoop\bin
>
> ![Screenshot 2024-09-18 212623](https://github.com/user-attachments/assets/f8aaae75-11af-4eb3-bc7b-7ed029c8f39d)
>
> ![env](https://github.com/user-attachments/assets/f18f0b84-ea5b-426a-91a4-af33c238bc47)
>
> ![Screenshot 2024-09-18 212803](https://github.com/user-attachments/assets/78e611f5-6f0b-47b5-9342-fc5ee57fc4a0)
>
> ![Screenshot 2024-09-18 212907](https://github.com/user-attachments/assets/64bef4a6-dd69-44eb-91ea-45aadc236ac3)
>
> ![Screenshot 2024-09-18 212959](https://github.com/user-attachments/assets/fa2e575d-d244-452c-9718-0fc36b839f83)
>
> Next go to Path -> double click on Path -> create a new path %HADOOP_HOME%\bin as shown below then click on ok on all windows:
>>
>> ![path](https://github.com/user-attachments/assets/44fa687e-7459-47d2-aa4a-7b96599276da)
>>
>> 

4. Finally:
>
> Go to intellij and test your code the problem should be solved, and you can run the code successfully!
>
>![Screenshot 2024-09-17 194037](https://github.com/user-attachments/assets/66423ef7-7f32-41bf-aa9b-18ad3388e654)
>
>
Note: if the error still the same the version of winutils.exe might be incompatible with your system, try to download another version.


























