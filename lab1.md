**Commands to add,remove,copy,merge files from HDFS and view hdfs files**

---------

# Steps


1. View the hdfs dfs command

* hdfs dfs (**Enter the following command to view the usage of hdfs dfs**)

![1](https://user-images.githubusercontent.com/63799117/85553516-a7a59e80-b641-11ea-832c-7a973772c251.PNG)

2. Create a Directory in HDFs

* hdfs dfs -ls (**To view content**)

![3](https://user-images.githubusercontent.com/63799117/85553847-fd7a4680-b641-11ea-917e-dad5df019aea.PNG)

*  hdfs dfs -mkdir test(**To create a directory named**)

* hdfs dfs -mkdir test/test1

* hdfs dfs -mkdir -p test/test2/test3 (**Subdirectories for test**)

* hdfs dfs -ls -R (**Recursively view the contents of a folder**)

![4](https://user-images.githubusercontent.com/63799117/85553857-ff440a00-b641-11ea-9443-b30a3c9506b1.PNG)


3. Delete a Directory

*  hdfs dfs -rm -R test/test2(**Delete the test2 folder**)

* hdfs dfs -ls -R 

![5](https://user-images.githubusercontent.com/63799117/85553861-010dcd80-b642-11ea-813a-f7bbf1a82e18.PNG)

4. Upload a file to Hdfs

* cd /Destop/root/labs/Lab2.1/

*  tail data.txt

* hdfs dfs -put data.txt test/ (**Command to copy**)

![1](https://user-images.githubusercontent.com/63799117/85555766-df154a80-b643-11ea-90bd-d6bd37b5244a.PNG)

* hdfs dfs -ls test 

![2](https://user-images.githubusercontent.com/63799117/85556021-1552ca00-b644-11ea-99f2-d3bc0f7c3748.PNG)

5. Copy a File in HDFS

* hdfs dfs -cp test/data.txt test/test1/data2.txt

* hdfs dfs -ls -R test

* hdfs dfs -rm test/test1/data2.txt 

![8 1](https://user-images.githubusercontent.com/63799117/85556345-61057380-b644-11ea-81db-39e288c09b08.PNG)

6. View the Contents of a File in HDFS

* hdfs dfs -cat test/data.txt (To view full data)

* hdfs dfs -tail test/data.txt (To view last 20 rows)

7. Getting a File from HDFS

* hdfs dfs -get test/data.txt /tmp/
* cd /tmp
* ls data*

8. The getmerge Command

*  hdfs dfs -put /root/devph/labs/demos/small_blocks.txt test/ 

* hdfs dfs -getmerge test /tmp/merged.txt 

9. Specify the Block Size and Replication Factor

*  hdfs dfs -D dfs.blocksize=1048576 -put data.txt data.txt 

* hdfs fsck /user/root/data.txt 

















