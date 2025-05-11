# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![os 1](https://github.com/user-attachments/assets/d915cd79-c7b3-45dd-93ea-151ec840ffe4)




cat < file2
## OUTPUT
![os 2](https://github.com/user-attachments/assets/24214eec-bf48-489e-825d-d58cb09c223c)




# Comparing Files
cmp file1 file2
## OUTPUT
![os 3](https://github.com/user-attachments/assets/a0b0bcfb-c003-476b-a6bc-db2fcfed6e15)



comm file1 file2
 ## OUTPUT
![os 4](https://github.com/user-attachments/assets/96e3eaee-01cc-43c2-95e5-9f0a184f576a)


 
diff file1 file2
## OUTPUT
![os 5](https://github.com/user-attachments/assets/1377acf6-3f05-40c1-a72f-e3ae23ae2b48)




#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![108](https://github.com/user-attachments/assets/d682446e-7982-4a34-b6ce-602311b293d0)




cut -d "|" -f 1 file22
## OUTPUT
![109](https://github.com/user-attachments/assets/43b30e8e-413b-4169-97cf-2f726d2beb72)



cut -d "|" -f 2 file22
## OUTPUT
![110](https://github.com/user-attachments/assets/6cccc2c1-3fde-4cb3-9850-40b02b52b01b)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![os 10](https://github.com/user-attachments/assets/109c3f5f-9784-4790-9ada-1c018db098cd)




grep hello newfile 
## OUTPUT
![new10](https://github.com/user-attachments/assets/5b9e6cad-f5fd-4f0d-9a7c-16f6089c864e)




grep -v hello newfile 
## OUTPUT
![os 11](https://github.com/user-attachments/assets/df8dfa11-71fd-4843-9801-417fa3053cf9)




cat newfile | grep -i "hello"
## OUTPUT
![os 12](https://github.com/user-attachments/assets/d189bf1b-2bf9-4ae7-a47d-6597ed3dde23)





cat newfile | grep -i -c "hello"
## OUTPUT
![os 13](https://github.com/user-attachments/assets/bdc3a2d4-e2e6-46cf-a6fc-382672f88afe)




grep -R ubuntu /etc
## OUTPUT
![os 15](https://github.com/user-attachments/assets/707bc1df-2886-466e-9887-b02abdbb9447)




grep -w -n world newfile   
## OUTPUT
![os 16](https://github.com/user-attachments/assets/f44ebc1b-af9c-4e46-942b-78a6dbce4687)




cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![111](https://github.com/user-attachments/assets/cc34ddde-ba68-4f5d-9b19-deb1322bcf61)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![112](https://github.com/user-attachments/assets/9b43a23c-8f0c-42c9-80f6-a4dd99e58c03)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![os 19](https://github.com/user-attachments/assets/b0da715e-1948-4310-9910-69798fd7a2b0)





egrep '(^hello)' newfile 
## OUTPUT
![os 20](https://github.com/user-attachments/assets/3a3315cd-7fe1-4201-b1f4-2480060eb73e)



egrep '(world$)' newfile 
## OUTPUT
![os 21](https://github.com/user-attachments/assets/8ba1a273-62a3-4d35-b53f-bde038517203)



egrep '(World$)' newfile 
## OUTPUT
![os 21](https://github.com/user-attachments/assets/f324ea4b-7d34-4ddc-a6d6-3bd88ec44383)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![os 22](https://github.com/user-attachments/assets/176c9ec8-5774-4e87-ab4e-5a59e85c690e)



egrep '[1-9]' newfile 
## OUTPUT
![os 23](https://github.com/user-attachments/assets/af5dc9d9-0a9c-4a24-bd3a-31a77767c00a)


egrep 'Linux.*world' newfile 
## OUTPUT
![os 24](https://github.com/user-attachments/assets/27b55aac-df93-403e-8f88-5123d250e319)


egrep 'Linux.*World' newfile 
## OUTPUT
![os 25](https://github.com/user-attachments/assets/e2635d30-21c6-473f-b149-f8abb31012d2)


egrep l{2} newfile
## OUTPUT
![os 26](https://github.com/user-attachments/assets/e7673983-1eb2-4fb2-b197-0626e510dd39)



egrep 's{1,2}' newfile
## OUTPUT 
![os 28](https://github.com/user-attachments/assets/c770c44a-5d42-4b9b-b73d-1c8f1821cc00)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![os 32](https://github.com/user-attachments/assets/96d5454e-8b03-4c9c-999b-f852692b1ec0)



sed -n -e '$p' file23
## OUTPUT
![os 33](https://github.com/user-attachments/assets/28429b87-280c-416c-8a10-f10586070c22)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![os 34](https://github.com/user-attachments/assets/e89448cc-7890-42d8-8633-6ce2305fe224)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![os 35](https://github.com/user-attachments/assets/373be957-07f4-40b6-b60f-5ddb2fcf4281)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![os 36](https://github.com/user-attachments/assets/a2de9862-3e4e-476d-b354-947f2d0aac3f)



sed -n -e '1,5p' file23
## OUTPUT
![os 37](https://github.com/user-attachments/assets/3b17ba31-83a3-4918-984d-0954c1834f94)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![os 38](https://github.com/user-attachments/assets/7d89cf36-2cec-4cbd-bfdf-78156edb7fdf)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![os 39](https://github.com/user-attachments/assets/387c4fb1-20e6-4eae-89e0-82dfe7f435ab)



seq 10 
## OUTPUT
![os 40](https://github.com/user-attachments/assets/e793557f-80cd-4bca-ad69-88459ac85ca2)



seq 10 | sed -n '4,6p'
## OUTPUT
![os 41](https://github.com/user-attachments/assets/0c39e32a-c4a0-4421-8bd7-989e0704e406)




seq 10 | sed -n '2,~4p'
## OUTPUT
![os 42](https://github.com/user-attachments/assets/8c20d0cb-8dbc-46a6-9f4f-e28b66a2e65a)



seq 3 | sed '2a hello'
## OUTPUT
![os 43](https://github.com/user-attachments/assets/7f398235-8e52-4f67-b607-f8fe4eb9cd9d)



seq 2 | sed '2i hello'
## OUTPUT
![os 44](https://github.com/user-attachments/assets/82402f7e-50cb-4ed4-8499-66cc86007b66)


seq 10 | sed '2,9c hello'
## OUTPUT
![os 45](https://github.com/user-attachments/assets/b34c8c37-0cd4-4639-b415-9153a0345804)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![os 46](https://github.com/user-attachments/assets/d6ce805e-66f5-4c36-85f7-b9bc712d8e64)



sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![os 49](https://github.com/user-attachments/assets/834f7848-4fd9-4ced-8f4b-a29ddca050f8)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![113](https://github.com/user-attachments/assets/731c4a9e-8531-4b00-8589-a2b99c67f6cc)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![os 51](https://github.com/user-attachments/assets/76ca8280-d30e-41dd-8ec6-e4eb0d5be2b1)


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![os 53](https://github.com/user-attachments/assets/3945b452-1231-42be-947d-8cbe54018aa8)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![os 54](https://github.com/user-attachments/assets/641e9f16-5d0d-4a18-8cfc-1c5a5a4617cd)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![100](https://github.com/user-attachments/assets/e1fd3332-8b2d-4abd-bfb7-b31e80d3d3ae)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![101](https://github.com/user-attachments/assets/f858403a-1390-45a9-9395-eaaef4b9e736)


tar -xvf backup.tar
## OUTPUT
![103](https://github.com/user-attachments/assets/9ea7ee1c-10b9-4f25-b5d9-77d9f32ee4a2)


gzip backup.tar

ls .gz
## OUTPUTS
![114](https://github.com/user-attachments/assets/bee91416-43d0-4ecb-99f3-ea5e0adad6dd)


gunzip backup.tar.gz
## OUTPUT
![115](https://github.com/user-attachments/assets/7f7ff73b-5d02-4bb7-9287-128df336f2d5)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![117](https://github.com/user-attachments/assets/3b3b4216-f518-4997-86fc-6faa2472007c)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![os 60](https://github.com/user-attachments/assets/6dc9e146-e9dc-4d1f-8db0-71b28503fe75)

 
ls file1
## OUTPUT
![os 61](https://github.com/user-attachments/assets/5b89ef19-6f5a-4051-a25e-5d280258d5c7)


echo $?
## OUTPUT 
![119](https://github.com/user-attachments/assets/497f765f-0502-4a39-8fb5-84752ddba2ff)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![119](https://github.com/user-attachments/assets/21af425b-8c18-4838-8d94-8ccd2fcba122)

 
abcd
 
echo $?
 ## OUTPUT
![120](https://github.com/user-attachments/assets/01a458cb-ce86-4cf0-9cf1-56e1b43eaba9)


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
![70](https://github.com/user-attachments/assets/078e272f-3b56-418e-91c6-d7a3cfce2f6c)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![71](https://github.com/user-attachments/assets/8c904667-1e1a-4668-8475-3ea9ed9a187f)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![74](https://github.com/user-attachments/assets/c0ac01bf-15a0-45c3-9eb6-1ce701c3a3e6)


# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT!




# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
![76](https://github.com/user-attachments/assets/7ba767be-6480-41d2-90bd-a83ae4056c1e)


# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![77](https://github.com/user-attachments/assets/872301dd-d7a0-4651-b88f-e218bc7326b8)


# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![78](https://github.com/user-attachments/assets/635ad882-f55c-4f31-91c0-f6e2e309d977)



# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![79](https://github.com/user-attachments/assets/420bde13-9213-4e70-ad25-452be937f514)


# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 

![80](https://github.com/user-attachments/assets/3363e1b5-fff9-40b7-9e21-4ed5814baed7)


 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
![81](https://github.com/user-attachments/assets/ddbb18c1-a70c-4dc9-b4ba-d5fa61481597)


 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
![82](https://github.com/user-attachments/assets/71f45015-3907-4238-96b5-c80cf0e87ab5)


 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
![83](https://github.com/user-attachments/assets/79afe787-121e-42a4-bb8e-17155090c33e)


 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 


```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh


 
$ ./forin2.sh 
![85](https://github.com/user-attachments/assets/ceb08798-6fe3-4f28-90c2-654c33689c27)

 

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

 
## OUTPUT
![107](https://github.com/user-attachments/assets/40601fcb-4abf-45d4-9c13-dc3b5b1b93c0)



cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![86](https://github.com/user-attachments/assets/e62089fe-b43f-4038-afee-47340f8c659f)



cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![87](https://github.com/user-attachments/assets/c1658df8-cb0a-41e9-8e27-db7ef3b6a680)



cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![88](https://github.com/user-attachments/assets/5e92fd13-a5eb-4f17-89ab-5317270a0cbc)




cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![89](https://github.com/user-attachments/assets/2764a025-df20-4a97-ab60-23318e35c444)



 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![92](https://github.com/user-attachments/assets/59083f5f-27ff-4e9a-8d37-321bfcb7d83a)



$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![93](https://github.com/user-attachments/assets/f36e24a7-51a2-4ef6-9dc4-8bb1773645e0)


 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![94](https://github.com/user-attachments/assets/ca539a50-379d-4f8b-9ae0-eb87f1dfc95b)




 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![94](https://github.com/user-attachments/assets/8f6015c3-f00b-46e5-a6ce-5ec896290cc5)




$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

![96](https://github.com/user-attachments/assets/796648f3-74b7-4f06-8881-a958f075c512)
 
 ./funcex.sh 1 2

![97](https://github.com/user-attachments/assets/c2147873-346a-45df-8549-f82533461e5a)
 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT

![98](https://github.com/user-attachments/assets/ba9fba49-04ec-49d0-83fe-4e5ce945a48d)

$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT

![98](https://github.com/user-attachments/assets/4aa33d01-2b56-49b8-b7c4-457a5da22e37)

$ ./argshift.sh 1 2 3

 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT

![99](https://github.com/user-attachments/assets/96cead2f-4e2f-4b8c-8ed5-7d1462b2a3f1)

 ./argshift.sh 1 2 3 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT
![105](https://github.com/user-attachments/assets/a1fac2f3-0012-40fb-ae89-f0951e71316f)

 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![106](https://github.com/user-attachments/assets/75f03aac-3548-49c7-a2a7-fb0adc6b1403)


# RESULT:
The Commands are executed successfully.
