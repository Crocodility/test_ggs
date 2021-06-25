## Basic work with files

- Create directory test1
~~~console
mkdir test1
~~~
- Create file test1.txt inside the test1 directory.
~~~console
touch test1.txt
~~~
-   Create copy of folder test1 with name test2.  
~~~console
cp -r  /home/vladstr/Desktop/test1 /home/vladstr/Desktop/test2
~~~
-    Delete file test1.txt inside test2 directory.
~~~console
rm -f test1.txt
~~~
-    Rename test2 folder into directory_without_file
~~~console
mv test2 directory_without_file
~~~
-    Insert 'test1' text into test1/test1.txt file.
~~~console
echo 'test1'>>test1.txt
~~~
-    print the text from the test1/test1.txt file.
~~~console
cat test1.txt
~~~
-    Insert 'test2' into the end of test1/test1.txt file.
~~~console
echo test2 >> test1.txt
~~~
-    print the text from the test1/test1.txt file.
~~~console
cat test1.txt
~~~
- check the size of test1 directory
~~~console
ls -sh; du -sh
~~~
## Permissions

-   Create test directory and block access for all to it.
~~~console
mkdir noaccess | chmod 000 noaccess
~~~
-   Try to remove that directory.
~~~console
rm -r noaccess // tells that you are trying to remove write-protected directory
/ rm -rf noaccess // deletes the directory 
~~~
-    Create simple script which prints current date. Try to execute it.
~~~console
#!/bin/bash date // to execute ./date.sh
~~~

## Log checking

-  Count lines in the file test.txt.
~~~console
wc -l // 200 lines
~~~

- Show last 3 lines from the test.txt file. 
~~~console
tail -n 3
~~~

-  Hom many uniq IP addresses accessed the website ? 
~~~console
cat test.txt | grep -o "[0-9]\+\.[0-9]\+\.[0-9]\+\.[0-9]\+" | sort | uniq > ips.txt  
output is in file ips.txt file
~~~


-  IP address with most requests.
~~~console
cat test.txt | awk '{print $1}' | sort -n | uniq -c | sort -rn >topips.txt
output is in topips.txt file
~~~

-  Top 3 IP addresses by amount of POST requests.
~~~console
There is no ips with POST requests
~~~

-  Which IP addresses received 403 error ? 
~~~console
searching with grep '403'/'forbidden'/'error' test.txt did not give any results
~~~

- Task with * . Write script to show which pages Google checked from the website 
~~~console
cat test.txt | grep 'Google' | awk '{print $7}'
~~~

## Replace

Replace IP address with most requests on 127.0.0.1 in test.txt file 
~~~console
vladstr@shared-MS-7B33:~/Desktop/test_ggs$ sed 's/114.119.140.234/127.0.0.1/' test.txt
~~~
