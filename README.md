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
> ![Screenshot 2024-09-18 221016](https://github.com/user-attachments/assets/31c301be-7f33-4fa3-82f7-a9758a5b4062)
>
> Download winutils.exe in “bin” folder as shown below:
>
> ![Screenshot 2024-09-18 221706](https://github.com/user-attachments/assets/c585baca-5ff5-4d0e-9857-b91842f44f8c)
>
> ![Screenshot 2024-09-18 222117](https://github.com/user-attachments/assets/8792db98-4647-4ca6-a267-c5970a3277b4)
>
> Next download the hadoop.dll file the same way you downloaded winutils.exe in “bin” folder as shown:
>>
>> ![Screenshot 2024-09-18 222543](https://github.com/user-attachments/assets/b3d6a175-7a97-4375-beef-5595d5d4436a)
>>
>> ![Screenshot 2024-09-18 220516](https://github.com/user-attachments/assets/40029c4e-adcd-40a6-9c23-6e3ef1b698b4)
>>
>> Note: the version of winutils.exe and Hadoop.dll should be the same
>>
>>


#### 3.	Step 3: go to system environment variables

> Create a new environment variable: HADOOP_HOME then enter the path to the folder where the winutils.exe file is located:
HADOOP_HOME=C:\hadoop\bin
>
> ![Screenshot 2024-09-18 223054](https://github.com/user-attachments/assets/c828c0c2-3364-4afc-babd-9af395a09741)
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

#### 4. Finally:
>
> Go to intellij and test your code the problem should be solved, and you can run the code successfully!
>
>![Screenshot 2024-09-17 194037](https://github.com/user-attachments/assets/66423ef7-7f32-41bf-aa9b-18ad3388e654)
>
>
Note: if the error still the same the version of winutils.exe might be incompatible with your system, try to download another version.


























