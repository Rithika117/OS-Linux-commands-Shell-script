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
<img width="760" height="240" alt="Screenshot from 2026-01-29 16-42-27" src="https://github.com/user-attachments/assets/8b7bb268-542f-4647-84e9-9324721bb377" />



cat < file2
## OUTPUT
<img width="760" height="240" alt="Screenshot from 2026-01-29 16-42-55" src="https://github.com/user-attachments/assets/b4bb1997-cc9e-4e57-a62b-b8a645c0d762" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="754" height="106" alt="Screenshot from 2026-01-29 16-44-03" src="https://github.com/user-attachments/assets/63b90c4c-f28c-463c-938e-8db6211622d9" />

comm file1 file2
 ## OUTPUT
<img width="778" height="183" alt="Screenshot from 2026-01-29 16-44-59" src="https://github.com/user-attachments/assets/72b8bd0a-9325-4f16-afb4-f18923902b22" />

 
diff file1 file2
## OUTPUT
<img width="721" height="227" alt="Screenshot from 2026-01-29 16-45-39" src="https://github.com/user-attachments/assets/61aa4310-1c9f-4d3b-8837-423dd69980fa" />


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
<img width="727" height="60" alt="Screenshot from 2026-01-29 16-52-52" src="https://github.com/user-attachments/assets/b5e2c5c0-1904-4c2d-8217-7fba7c603cb6" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="724" height="143" alt="Screenshot from 2026-01-29 17-03-01" src="https://github.com/user-attachments/assets/69ab0abd-e625-4132-a11a-8d81434d715f" />


cut -d "|" -f 2 file22
## OUTPUT


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
<img width="671" height="254" alt="Screenshot from 2026-01-29 17-06-09" src="https://github.com/user-attachments/assets/76d11250-ab46-49cb-b6a9-8c9221c4295f" />



grep hello newfile 
## OUTPUT
<img width="671" height="254" alt="Screenshot from 2026-01-29 17-06-36" src="https://github.com/user-attachments/assets/3a208cfc-72a3-4a0e-b9e9-b726e5b9c302" />




grep -v hello newfile 
## OUTPUT
<img width="671" height="254" alt="Screenshot from 2026-01-29 17-06-36" src="https://github.com/user-attachments/assets/b842ff6a-32ee-44ec-bd98-f929d0e3bd89" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="671" height="254" alt="Screenshot from 2026-01-29 17-07-21" src="https://github.com/user-attachments/assets/f7d580c3-1596-4c44-bc20-8813bb2d2d2c" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="671" height="67" alt="Screenshot from 2026-01-29 17-09-04" src="https://github.com/user-attachments/assets/0c1730a2-faa1-4dab-8c57-1ca3ff7cb8df" />



grep -R ubuntu /etc
## OUTPUT
<img width="828" height="668" alt="Screenshot from 2026-01-29 17-18-24" src="https://github.com/user-attachments/assets/7912d7f8-47d2-4795-a870-a1e0a742e96a" />



grep -w -n world newfile   
## OUTPUT
<img width="671" height="67" alt="Screenshot from 2026-01-29 17-16-59" src="https://github.com/user-attachments/assets/939df5c8-8d13-4fa5-b024-b8920d9fa9d7" />


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
<img width="846" height="96" alt="Screenshot from 2026-01-29 17-22-00" src="https://github.com/user-attachments/assets/e7ed1d1b-aa2f-498d-b9b2-b1842b9eb4c9" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="743" height="104" alt="Screenshot from 2026-01-29 17-29-15" src="https://github.com/user-attachments/assets/68e41f40-d831-4be3-ac6c-99bc244fc384" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="743" height="104" alt="Screenshot from 2026-01-29 17-25-36" src="https://github.com/user-attachments/assets/00bf1411-1c12-479e-8532-51094ea79422" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="743" height="104" alt="Screenshot from 2026-01-29 17-29-15" src="https://github.com/user-attachments/assets/82c6136c-acfe-4cfd-a2f0-a27da8d78745" />



egrep '(world$)' newfile 
## OUTPUT
<img width="743" height="104" alt="Screenshot from 2026-01-29 17-43-50" src="https://github.com/user-attachments/assets/158067ed-379b-48b0-92f8-17737897b134" />



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="743" height="104" alt="Screenshot from 2026-01-29 17-44-33" src="https://github.com/user-attachments/assets/8f76befa-2df4-4c52-82e2-8fb6f5a5981e" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="743" height="104" alt="Screenshot from 2026-01-29 17-45-50" src="https://github.com/user-attachments/assets/898f7ab1-31f6-4aab-8088-89be4d5e9cdd" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="743" height="104" alt="Screenshot from 2026-01-29 17-46-53" src="https://github.com/user-attachments/assets/45cd4928-35c7-4f17-a9c2-d309d1575379" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="743" height="104" alt="Screenshot from 2026-01-29 17-46-53" src="https://github.com/user-attachments/assets/53ee38ee-1c70-4b17-b0ea-d225bc8275cb" />


egrep l{2} newfile
## OUTPUT

<img width="744" height="104" alt="Screenshot from 2026-01-29 17-52-10" src="https://github.com/user-attachments/assets/2c8080e1-abf6-4982-8391-9b40629e0aeb" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="742" height="127" alt="Screenshot from 2026-01-29 17-51-45" src="https://github.com/user-attachments/assets/d4c4ce29-83c1-46e1-9cb3-d0832eee3570" />


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
<img width="744" height="104" alt="Screenshot from 2026-01-29 17-53-09" src="https://github.com/user-attachments/assets/980c1aa1-1ab4-4238-bb8a-5375cf7f6198" />



sed -n -e '$p' file23
## OUTPUT
<img width="730" height="270" alt="Screenshot from 2026-01-29 17-55-21" src="https://github.com/user-attachments/assets/c2c7ec42-0777-4878-acb7-4ab32dfefa8c" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="730" height="270" alt="Screenshot from 2026-01-29 17-55-21" src="https://github.com/user-attachments/assets/f600978a-db9f-4014-8d11-961ac874c282" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="730" height="270" alt="Screenshot from 2026-01-29 17-56-06" src="https://github.com/user-attachments/assets/6768b4f4-b0ce-4f88-841c-1eb75385ec46" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="735" height="181" alt="Screenshot from 2026-01-29 17-56-24" src="https://github.com/user-attachments/assets/a415ecb1-a96c-41db-9ad6-5c2dcc709e3b" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="735" height="120" alt="Screenshot from 2026-01-29 17-57-02" src="https://github.com/user-attachments/assets/627c5b50-e0f9-45c0-bf6e-16b841ce6d05" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="740" height="100" alt="Screenshot from 2026-01-29 17-57-51" src="https://github.com/user-attachments/assets/4a0a4182-4527-4216-b49d-e419c72b5030" />



seq 10 
## OUTPUT
<img width="727" height="245" alt="Screenshot from 2026-01-29 17-58-10" src="https://github.com/user-attachments/assets/af324c1a-7353-43dd-9316-39d4aec0678e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="751" height="96" alt="Screenshot from 2026-01-29 17-58-31" src="https://github.com/user-attachments/assets/3008543c-9c6c-47d0-b46b-230868839c72" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="751" height="96" alt="Screenshot from 2026-01-29 17-58-46" src="https://github.com/user-attachments/assets/bce2bb0d-900a-41c6-aba3-3ed66009dd13" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="752" height="125" alt="Screenshot from 2026-01-29 17-59-03" src="https://github.com/user-attachments/assets/01f33da9-a3a3-406b-bfbb-d56d8c3c0056" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="752" height="125" alt="Screenshot from 2026-01-29 17-59-25" src="https://github.com/user-attachments/assets/ba250d86-316c-48d5-b02f-68ca0bf850a6" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="752" height="125" alt="Screenshot from 2026-01-29 17-59-46" src="https://github.com/user-attachments/assets/fda92b42-5c58-41f7-b374-79b2f1ec3113" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="752" height="125" alt="Screenshot from 2026-01-29 17-59-59" src="https://github.com/user-attachments/assets/2ddbd6cf-a6f1-404a-b771-ff5e5b572e00" />



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
<img width="750" height="175" alt="Screenshot from 2026-01-29 18-01-59" src="https://github.com/user-attachments/assets/511815d1-a3ad-49e5-be90-08390a7589e5" />


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
<img width="750" height="175" alt="Screenshot from 2026-01-29 18-02-52" src="https://github.com/user-attachments/assets/90592e68-c4cc-4fc0-b8d3-a1748cb541b5" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="752" height="257" alt="Screenshot from 2026-01-29 18-03-22" src="https://github.com/user-attachments/assets/6d9fe863-343a-4bc6-81ae-96e818668c13" />

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
<img width="777" height="125" alt="Screenshot from 2026-01-29 18-05-51" src="https://github.com/user-attachments/assets/7b43a845-1cc9-4ae3-847b-803aeb1e4d38" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="777" height="125" alt="Screenshot from 2026-01-29 18-06-06" src="https://github.com/user-attachments/assets/95421c88-0693-46f4-9bb1-f34c3e19c48f" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT 
<img width="747" height="91" alt="Screenshot from 2026-01-29 22-05-52" src="https://github.com/user-attachments/assets/6bcb37b3-529a-4a40-baea-2aff4ad5f2e6" />

 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="681" height="707" alt="Screenshot from 2026-01-29 22-05-29" src="https://github.com/user-attachments/assets/f8eec190-1b16-4098-8963-6e11597f98f0" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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
<img width="681" height="707" alt="Screenshot from 2026-01-29 22-05-29" src="https://github.com/user-attachments/assets/a8ad0e45-ef36-48e9-bb83-825f07a319e3" />

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="747" height="91" alt="Screenshot from 2026-01-29 22-06-09" src="https://github.com/user-attachments/assets/4f2a4ec5-ac3c-4197-9756-332864e2cfcd" />

abcd
 
echo $?
 ## OUTPUT
<img width="747" height="91" alt="Screenshot from 2026-01-29 22-06-09" src="https://github.com/user-attachments/assets/388fc988-f6aa-4477-be0f-d9f09ac153d5" />


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="747" height="381" alt="Screenshot from 2026-01-29 22-07-49" src="https://github.com/user-attachments/assets/d6737e1e-fc33-487c-b2d6-9b718a23e7d6" />


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
<img width="786" height="89" alt="Screenshot from 2026-01-29 22-15-35" src="https://github.com/user-attachments/assets/1427602e-6162-443f-8b18-ea88e9947bad" />

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
## OUTPUT
<img width="786" height="89" alt="Screenshot from 2026-01-29 22-20-40" src="https://github.com/user-attachments/assets/ca25ebc9-a7ad-448a-b3f0-5f204069e800" />



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
<img width="953" height="109" alt="Screenshot from 2026-01-29 23-02-20" src="https://github.com/user-attachments/assets/45b3c6c6-f362-4add-b35c-96e153da7f5c" />


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
<img width="953" height="109" alt="Screenshot from 2026-01-29 23-04-14" src="https://github.com/user-attachments/assets/f3320de9-e0f5-4415-b538-9ac5b344365e" />

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
<img width="935" height="184" alt="Screenshot from 2026-01-29 23-14-26" src="https://github.com/user-attachments/assets/264637eb-32e4-4341-b8d1-476a038b9e17" />

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
<img width="932" height="217" alt="Screenshot from 2026-01-29 23-26-56" src="https://github.com/user-attachments/assets/244a5e60-bd2c-4cc0-a104-970c5b6b5471" />


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
<img width="932" height="217" alt="Screenshot from 2026-01-29 23-28-26" src="https://github.com/user-attachments/assets/63f14044-e121-4c22-89e3-be48285f7be3" />

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
<img width="932" height="217" alt="Screenshot from 2026-01-29 23-31-01" src="https://github.com/user-attachments/assets/3f6f4d39-256a-4448-8a83-553a84efe7be" />

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
<img width="912" height="311" alt="Screenshot from 2026-01-29 23-33-50" src="https://github.com/user-attachments/assets/606a3d80-6534-4288-948b-c47ae4e5194c" />

 
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
<img width="921" height="120" alt="Screenshot from 2026-01-29 23-35-55" src="https://github.com/user-attachments/assets/c99f59ef-cfed-4d27-97d1-92ce0706961f" />

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
 <img width="932" height="169" alt="Screenshot from 2026-01-29 23-40-00" src="https://github.com/user-attachments/assets/d7f90f35-658b-4b33-9815-57dc09481ec0" />

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
<img width="932" height="169" alt="Screenshot from 2026-01-29 23-41-39" src="https://github.com/user-attachments/assets/48defe5a-f0c7-4ac8-9e1e-3b520de820a1" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="932" height="169" alt="Screenshot from 2026-01-29 23-45-40" src="https://github.com/user-attachments/assets/a12c2a10-154b-4df6-90fd-2dea9676e5b0" />



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

 
 ./funcex.sh 1 2

 
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


# RESULT:
The Commands are executed successfully.
