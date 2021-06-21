## Basic work with files

- Create directory test1  
mkdir test1
- Create file test1.txt inside the test1 directory.
'''console
touch test1.txt
'''
-   Create copy of folder test1 with name test2.  
cp -r  /home/vladstr/Desktop/test1 /home/vladstr/Desktop/test2
-    Delete file test1.txt inside test2 directory.
rm -f test1.txt
-    Rename test2 folder into directory_without_file
mv test2 directory_without_file
-    Insert 'test1' text into test1/test1.txt file.
echo 'test1'>>test1.txt
-    print the text from the test1/test1.txt file.
cat test1.txt
-    Insert 'test2' into the end of test1/test1.txt file.
echo test2 >> test1.txt
-    print the text from the test1/test1.txt file.
cat test1.txt
- check the size of test1 directory
ls -sh; du -sh
## Permissions

-   Create test directory and block access for all to it.
mkdir noaccess | chmod 000 noaccess
-   Try to remove that directory.
rm -r noaccess // tells that you are trying to remove write-protected directory
/ rm -rf noaccess // deletes the directory 
-    Create simple script which prints current date. Try to execute it.
#!/bin/bash date // to execute ./date.sh

## Log checking

-  Count lines in the file test.txt.
wc -l // 200 lines

- Show last 3 lines from the test.txt file. 
tail -n 3

-  Hom many uniq IP addresses accessed the website ? 
94 ips

-  IP address with most requests.


-  Top 3 IP addresses by amount of POST requests.


-  Which IP addresses received 403 error ? 


- Task with * . Write script to show which pages Google checked from the website 

## Replace

Replace IP address with most requests on 127.0.0.1 in test.txt file 
