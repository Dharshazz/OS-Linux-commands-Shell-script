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
<img width="389" height="149" alt="Screenshot 2025-08-12 112321" src="https://github.com/user-attachments/assets/308d4751-d0c8-4af8-9b75-9b349fd16ca9" />



cat < file2
## OUTPUT
<img width="427" height="171" alt="Screenshot 2025-08-12 112246" src="https://github.com/user-attachments/assets/6d9de269-8efd-4b6d-aa9e-d0fe3d8a2eb4" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="400" height="78" alt="image" src="https://github.com/user-attachments/assets/40ba9a17-5451-429e-a511-45024f9431d3" />

 
comm file1 file2
 ## OUTPUT
<img width="393" height="224" alt="image" src="https://github.com/user-attachments/assets/c0b49393-8727-49f7-80f1-ab4e9f07bc58" />

 
diff file1 file2
## OUTPUT
<img width="430" height="276" alt="image" src="https://github.com/user-attachments/assets/01bba462-b1e3-4396-ae3e-2517c4da5d98" />


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
<img width="412" height="101" alt="image" src="https://github.com/user-attachments/assets/5141ebfc-45fe-4070-ac8f-059f8a0fc5bd" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="391" height="130" alt="image" src="https://github.com/user-attachments/assets/86bce095-1e07-4492-9727-e2a69ff69600" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="399" height="121" alt="image" src="https://github.com/user-attachments/assets/b4184f69-cb10-4e66-87f5-4e93fc9a865b" />



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
<img width="400" height="71" alt="image" src="https://github.com/user-attachments/assets/4c7f434f-a784-49d5-9c59-6c20c6281ea5" />




grep hello newfile 
## OUTPUT
<img width="400" height="71" alt="image" src="https://github.com/user-attachments/assets/051421d0-8779-4826-807f-eddac37f51d2" />




grep -v hello newfile 
## OUTPUT
<img width="402" height="75" alt="image" src="https://github.com/user-attachments/assets/a59dd033-86f8-47a5-b5ca-7ab46a01c592" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="447" height="76" alt="image" src="https://github.com/user-attachments/assets/e9199b29-43d8-4872-88b1-bfd1c82d28ed" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="440" height="75" alt="image" src="https://github.com/user-attachments/assets/e0ed8377-4850-4fcf-8b41-38355ac1caf0" />





grep -R ubuntu /etc
## OUTPUT
<img width="1184" height="655" alt="image" src="https://github.com/user-attachments/assets/4f52da1e-58ac-4c8f-b661-8a848c164bc4" />



grep -w -n world newfile   
## OUTPUT
<img width="459" height="78" alt="image" src="https://github.com/user-attachments/assets/0b18254e-68fb-469e-a193-849dc9c4df5f" />


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
<img width="446" height="77" alt="image" src="https://github.com/user-attachments/assets/41d4fee9-68cf-40c1-85ed-c3fa380d9e20" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="488" height="74" alt="image" src="https://github.com/user-attachments/assets/13803e92-37c2-4a50-984a-f1d6ac39b19e" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="439" height="79" alt="image" src="https://github.com/user-attachments/assets/af834136-a230-4505-ae9c-6711e9e73d28" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="327" height="47" alt="image" src="https://github.com/user-attachments/assets/3c3e6f2b-3d90-4dcf-9a18-4e618ada1a1c" />



egrep '(world$)' newfile 
## OUTPUT

<img width="409" height="83" alt="image" src="https://github.com/user-attachments/assets/f3e4fa81-0486-417c-888e-4ee0c4cb6f0f" />


egrep '(World$)' newfile 
## OUTPUT
<img width="349" height="53" alt="image" src="https://github.com/user-attachments/assets/32e58357-6ca3-496c-9170-0a8238631166" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="369" height="78" alt="image" src="https://github.com/user-attachments/assets/04e221d7-8dd3-4e0b-9fb2-1b68a12c8656" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="367" height="50" alt="image" src="https://github.com/user-attachments/assets/c4b8a1cf-4e46-4563-a20b-fe567e277949" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="398" height="73" alt="image" src="https://github.com/user-attachments/assets/537606cb-5ad9-4dc4-b0d4-35cfbe64889f" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="398" height="73" alt="image" src="https://github.com/user-attachments/assets/537606cb-5ad9-4dc4-b0d4-35cfbe64889f" />

egrep l{2} newfile
## OUTPUT
<img width="400" height="101" alt="image" src="https://github.com/user-attachments/assets/1bb11606-5c4a-4a78-a73e-184dda680c47" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="318" height="103" alt="image" src="https://github.com/user-attachments/assets/b0e904f9-c747-4afa-95a7-770dc9e57a3e" />


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
<img width="375" height="79" alt="image" src="https://github.com/user-attachments/assets/4c7391be-bfea-461a-8f95-428d2b8627d7" />



sed -n -e '$p' file23
## OUTPUT
<img width="350" height="82" alt="image" src="https://github.com/user-attachments/assets/a0a13765-0637-42c4-9a2f-37d659f7b911" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="453" height="251" alt="image" src="https://github.com/user-attachments/assets/59889936-b50d-4bc1-b1db-95769514d76f" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="468" height="249" alt="image" src="https://github.com/user-attachments/assets/ba6cfb6b-c992-4cca-8f4b-0d1c11b85eec" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="467" height="251" alt="image" src="https://github.com/user-attachments/assets/09610d3a-f561-4024-9ed6-755f788a4864" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="379" height="179" alt="image" src="https://github.com/user-attachments/assets/e0edc467-60a5-40d1-bcdb-69416acc2bbc" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="435" height="127" alt="image" src="https://github.com/user-attachments/assets/f3275dc6-8227-4558-a3d7-2b1f68132911" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="435" height="104" alt="image" src="https://github.com/user-attachments/assets/612e7572-49f8-4d65-87c5-b7c6161d0dee" />



seq 10 
## OUTPUT
<img width="316" height="302" alt="image" src="https://github.com/user-attachments/assets/133243a6-5493-4721-bafd-06240908b9a9" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="383" height="128" alt="image" src="https://github.com/user-attachments/assets/6f363fa5-24ed-432f-a8aa-4e02ef4e87d8" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="343" height="123" alt="image" src="https://github.com/user-attachments/assets/a9bd5b3f-d727-4344-a3a2-84163a77db7e" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="357" height="152" alt="image" src="https://github.com/user-attachments/assets/43acee58-cce7-4422-94e0-4b14c0841069" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="352" height="126" alt="image" src="https://github.com/user-attachments/assets/1b198e36-61d0-4579-82c1-64df5a88c4b7" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="370" height="118" alt="image" src="https://github.com/user-attachments/assets/1e00b8ae-d012-437f-91b9-02645c134fef" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="480" height="131" alt="image" src="https://github.com/user-attachments/assets/e174b9af-f6ed-47df-a828-4abcd3903b38" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="435" height="131" alt="image" src="https://github.com/user-attachments/assets/503f2bd3-6d40-4edc-a25b-d8e8cfeea725" />




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
<img width="428" height="176" alt="image" src="https://github.com/user-attachments/assets/89598f2e-367a-46f9-82af-51a948188ced" />


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
<img width="394" height="184" alt="image" src="https://github.com/user-attachments/assets/f25fb450-826f-4513-a2b3-51e0478f2a35" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="482" height="253" alt="image" src="https://github.com/user-attachments/assets/47001c29-921f-4815-aeef-7d8f6ced5241" />




cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="364" height="128" alt="image" src="https://github.com/user-attachments/assets/7d2d12f1-db4c-45dd-acfe-6bc0f79523cd" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="514" height="123" alt="image" src="https://github.com/user-attachments/assets/2b9b6deb-c4aa-4883-8e6a-372974dbdc22" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="663" height="556" alt="image" src="https://github.com/user-attachments/assets/bef67f7c-d6e7-43b5-8863-92b1b546f8f5" />
<img width="473" height="571" alt="image" src="https://github.com/user-attachments/assets/5332a844-de0e-40cd-9e9d-e9b5b2004195" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="781" height="466" alt="image" src="https://github.com/user-attachments/assets/b85beeb9-c1a8-48ba-88b6-378b09ef739b" />


tar -xvf backup.tar
## OUTPUT
<img width="519" height="549" alt="image" src="https://github.com/user-attachments/assets/ddc04876-9647-4a6d-ba91-bf165b988ddd" />

<img width="549" height="487" alt="image" src="https://github.com/user-attachments/assets/115fc3dc-ab46-497a-abee-9950e03ab6da" />

gzip backup.tar

ls .gz
## OUTPUT
 
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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="486" height="380" alt="image" src="https://github.com/user-attachments/assets/d92732f4-d6de-4934-9917-fdf0f9cb79db" />


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
<img width="721" height="411" alt="image" src="https://github.com/user-attachments/assets/32c65bb6-2942-4e44-afaf-a33122b7d32e" />

 
ls file1
## OUTPUT
<img width="406" height="82" alt="image" src="https://github.com/user-attachments/assets/c2741679-493c-401f-bd7c-4a8ca97ca774" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="364" height="75" alt="image" src="https://github.com/user-attachments/assets/043e19c8-68d9-4229-8dc8-4a2bb80bc429" />

abcd
 
echo $?
 ## OUTPUT
<img width="394" height="78" alt="image" src="https://github.com/user-attachments/assets/508778be-c646-4782-96c2-57cc9db25320" />


 
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
<img width="452" height="313" alt="image" src="https://github.com/user-attachments/assets/ff153584-801c-484d-96dd-2923e1255d98" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="442" height="142" alt="image" src="https://github.com/user-attachments/assets/48d832b7-d301-45ef-be2e-233def05581f" />


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
<img width="648" height="260" alt="image" src="https://github.com/user-attachments/assets/cecb86bd-a901-46f9-8f93-0e658dda2cb0" />

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
<img width="520" height="479" alt="image" src="https://github.com/user-attachments/assets/2fb90494-4ba9-43a6-8924-61d205b04a58" />



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
<img width="509" height="548" alt="image" src="https://github.com/user-attachments/assets/93161f11-eb28-4cfc-8400-3fc85e1fed98" />

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
<img width="661" height="589" alt="image" src="https://github.com/user-attachments/assets/79dd6ea3-e73f-483e-acc4-aaeb1095477e" />

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
<img width="575" height="485" alt="image" src="https://github.com/user-attachments/assets/1374f14b-ed8b-4f72-9a99-49b1ab2beb06" />


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
<img width="518" height="254" alt="image" src="https://github.com/user-attachments/assets/7c2d5048-c678-443a-a1ee-6467901d30db" />

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
 # output
 <img width="613" height="231" alt="image" src="https://github.com/user-attachments/assets/b69e8f7d-8d58-4958-9c14-a96d2bf3a039" />

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
 # Output
 <img width="613" height="231" alt="image" src="https://github.com/user-attachments/assets/9142f9b8-d7c7-4525-a6f1-6d0d77477038" />

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
 # Output
 <img width="577" height="250" alt="image" src="https://github.com/user-attachments/assets/d7f1b45d-0d46-4810-a350-2a8e6f8000f1" />

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
<img width="654" height="223" alt="image" src="https://github.com/user-attachments/assets/13f04ddf-aa37-4124-b4bd-c4715d150548" />

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
<img width="422" height="237" alt="image" src="https://github.com/user-attachments/assets/17f8deb0-f206-4bc9-ba09-57e6fb153f49" />


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
<img width="467" height="230" alt="image" src="https://github.com/user-attachments/assets/fbaf564d-fffe-49fa-a5f0-479a7ed4f930" />

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
<img width="394" height="218" alt="image" src="https://github.com/user-attachments/assets/132b9440-611e-4d27-936f-9a0249a4e4f8" />

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
<img width="394" height="218" alt="image" src="https://github.com/user-attachments/assets/c4568cfb-2d96-4c8e-8dc1-019fa6daf5ba" />

 
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
<img width="522" height="382" alt="image" src="https://github.com/user-attachments/assets/3337a756-8774-4a6b-abcc-48401269bf38" />

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
 <img width="522" height="382" alt="image" src="https://github.com/user-attachments/assets/a8140b3e-29e5-46a8-8340-bf08fe33288e" />

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
<img width="529" height="213" alt="image" src="https://github.com/user-attachments/assets/754c71ad-91b9-4c14-a99b-217f525d55cb" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="471" height="222" alt="image" src="https://github.com/user-attachments/assets/054c0c76-2852-4f77-8eed-6d55b9fc90a8" />



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
<img width="617" height="382" alt="image" src="https://github.com/user-attachments/assets/7f623e51-8287-47d1-92f4-bb94526504d1" />

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
<img width="370" height="188" alt="image" src="https://github.com/user-attachments/assets/502e4da6-7376-4207-ad38-85d8e1af6f6a" />

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
## 
<img width="491" height="342" alt="image" src="https://github.com/user-attachments/assets/2245237a-87e7-4a1d-80e1-b58c2499e8c2" />

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
