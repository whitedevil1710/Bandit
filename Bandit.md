### **LEVEL-0:**

I used the following command to connect the bandit

ssh bandit.labs.overthewire.org -l bandit0 -p 2220

The password to connect the bandit0 is &quot;bandit0&quot;.

When I connected to the bandit0 I found a readme file in home directory I used the &quot;ls&quot; command to see the files in the specific directory and &quot;cat&quot; filename to find the content in the file

As it is specified in the description that the password for the next level is stored in the readme file.

        The password for the next level is &quot;boJ9jbbUNNfktd78OOpsqOltutMc3MY1&quot;.

### **LEVEL-1:**

I logged into the bandit I used &quot;ls&quot; command to find any files stored in it then I found an dashed file I used &quot;cat ./-filename&quot; to see the content in the file and I found the password.

        The password for the next level is &quot;CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9&quot;

### **LEVEL-2:**

In the description it is mentioned that the password is saved in the file named &quot;spaces in this filename&quot;. So I used the command cat &quot;file name&quot; to display the file content if we are giving the space in this filename linux terminal identifies this as 4 different file so to understand the linux terminal that it is a single file name we have enclose it in double quotes.

        The password is displayed as &quot;UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK&quot;

### **LEVEL-3:**

        In this level the &quot;ls&quot; command displays a directory named inhere. To open the file inhere I used the &quot;cd filename&quot;.

As mentioned in the question that password is hidden in a file So I used &quot;ls -a&quot; ls is used to display all the directories except some directories starting with &quot;.&quot; Which means that it is hidden by using -a it will not ignore such type of entries it will display every file present in the current folder. So as the password is stored in hidden file I used the mentioned command. Then I used the &quot;cat .filename&quot; to display the content in the hidden file

        The password  is &quot;pIwrPrtPN36QITSp3EQaw936yaFoFgAB&quot;.

### **LEVEL-4:**

        In this level there is a folder inhere in home directory which I found by using &quot;ls&quot; command. When I moved into the in here using &quot;cd filename&quot; command I found so many files there. In these only one file contains the password so I used the command &quot;file ./\*&quot; to find the file type of all the dashed file stored in that folder I found one of the file is ascii and all others are in the format  data so I used the command &quot;cat ./-filename&quot; to display the content in the ascii file then I found the password in it.

        The password for next level is &quot;koReBOKuIDDepwhWk7jZC0RTdopnAYKh&quot;.

### **LEVEL-5:**

        In the description it is mentioned that the password is stored in a file which is human readable;1033 bytes in size and not executable

In the terminal  I opened the inhere folder by command cd and type this command to find the file with specified &quot;find -type f -size 1033c ! -executable&quot;. In this find is used to find any file or keyword from the whole system so I used &#39;-size&#39; to specify size and &#39;!=executable&#39; to specify file is not executable and &quot;type -f&quot; to specify it is a regular file and  found out the particular file and It contains password.

The Password for next level &quot;DXjZPULLxYr17uwoI01bNLQbtFemEgo7&quot;.

### **LEVEL-6:**

        In the description provided it is said that the file is somewhere in the server and has the following properties :

\*owned by user bandit7

\*owned by group bandit6

\*33 bytes in size

To find the file I used the linux command :

&quot;find / -user bandit7 -group bandit6 -size 33c&quot;.

 &quot;find &quot; is used to search for the files in the directory ,  / is used to search the whole directory, &quot;-user&quot; is used to specify the name of the user who owns the file, &quot;-group&quot; is used to specify the group that owns the file , the the &quot;-size&quot; is used to specify the size of the file. After execution of the command we will get a lot of directories . We can find a directory with  the file bandit7.password.  Then I used &quot;cat&quot; to see the content in the file  and I found the password.

The Password for next level &quot;HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs&quot;

### **LEVEL-7:**

In the description it is said  that the password is stored in a file named data.txt and it is stored near the name  &quot;millionth&quot; , then I used the command &quot;cat data.txt | grep millionth&quot; to find the password. In it the &quot;cat&quot; command is used to see the content in the file and &quot;grep&quot;  is used to find the matching pattern specified. In it the word &quot;millionth&quot; is specified .So after running the command it extracted the text &quot;millionth&quot; from the text file which then shows the content .

The Password for the next level &quot;cvX2JJa4CFALtqS87jk27qwqGhBM9plV&quot;.

### **LEVEL-8:**

In the description it is mentioned that the password is stored in a file named data.txt  and is the only line of text that occurs only once . Then I used the command &quot; cat data.txt|sort| uniq -c&quot;. In thi command &quot;cat data.txt&quot; is used to see the content of the file, &quot; sort &quot; sorts the file data in an alphabetic order, and &quot;uniq –c &quot; will display the text in unique order and counts the number of times it  is repeated . In it only once a text is repeated so that is password as per the description provided.

The Password for next level &quot;UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR&quot;.

### **LEVEL-9:**

        As per the description , the password is stored in a data.txt file in one of the few human readable strings proceeded by several &quot;=&quot;characters. So I used the command &quot;strings data.txt | grep =&quot; In the  data.txt&quot; file there are both human-readable and unreadable files  , To extract human readable file I used the command &quot;strings filename&quot; ,&quot; grep&quot; to match the pattern &quot;=&quot; . From this I found the password.

 The Password for next level &quot;truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk&quot;

### **LEVEL-10:**

        As per the description, the password is stored  in a file data.txt which contains base64 encoded data. So I used the command &quot;cat data.txt | base64 --decode&quot; . In this the command &quot;cat data.txt&quot; will display the contents in the text file and &quot;base64 --decode&quot; will decode the displayed content and gives the output which is the password.

The Password for next level &quot;IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR&quot;.
