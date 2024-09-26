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
// git add-h
// git commit
// git origin

### Display the content of the files
cat < file1


## OUTPUT
![image](https://github.com/user-attachments/assets/7d9a63bb-3319-4190-b13c-de1803e3d22f)


cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/1573e84d-a1ce-456c-bab0-f7cd8e88c336)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/8afbae35-1672-42cc-b2bd-a81eb39842d9)

 
comm file1 file2
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/5ff2bdd7-898c-4645-b3fa-b305e828bf1c)


 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/21a1b84e-79d7-43d3-a953-b379f1b87514)


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
![image](https://github.com/user-attachments/assets/91b657c4-ce8d-4839-95f1-d90066cfd307)



cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/18df53c8-6b79-4af2-9c41-27724d776dc8)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/49e98219-597d-4b35-ba66-30e9989215e5)


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
![image](https://github.com/user-attachments/assets/e0c9ef13-c952-4fa7-aa26-cdc330c296a7)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f8159d1a-7065-4a8f-b89d-8fc0f763019a)



grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6c366906-2350-44a4-af3b-a2835863c2e2)


cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/86944f70-9da8-4926-8c3c-15df3277c8f4)


cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/773db096-54fa-4183-8b54-f262f4194341)



grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/4ca73659-9600-46bc-b318-7b3a67d6b6f8)


grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/db7251d2-bf2f-4db5-888e-4e8754498626)

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
![image](https://github.com/user-attachments/assets/0c42f4ca-675b-46b2-8ee8-f98720db447c)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ace406f5-da4f-4b85-bac7-347892281994)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/37ee6988-9a97-49f2-8faa-2411c3e2e1d2)



egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/1c73dc65-52bc-43b1-a6fc-72c9254f3c65)


egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/debcb546-a0e2-4424-9fdf-0320e0a93498)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f57ad60a-3adb-479d-a05c-066bd29d47c4)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b0ead521-15c7-48b7-bbc5-793f0050722c)


egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ffcddc36-ff59-40ba-9a81-c4401ccca137)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/940f6676-5339-4976-b58f-5168f1bf8016)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4ac20c4b-7319-46e5-9deb-20131fa18d9e)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/8c2af884-062c-4c33-ade5-978bdf268138)

egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/ce24bfdf-ac08-48e4-8241-84c20a96a162)

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
![image](https://github.com/user-attachments/assets/1c60b1f2-abee-41aa-8be5-9463b5980881)


sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/2b11ee45-1b19-46eb-ad63-1c10f22828d0)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f295500d-d882-4f7d-91be-256d6512dda9)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/55b7110e-ecc3-4253-9ca1-f2b0161145c6)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/199bd33b-1a9c-405f-9760-183a0761eda0)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/e678edcc-0a89-4867-940f-ac09f86ece65)

sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/062c919a-2c4e-4656-8a42-51432989a938)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/5fcdd30c-b077-4bf9-9bb4-14f6c3acb459)


seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/af88c582-0580-485a-9ccd-7a1460eb2d4a)


seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/d99c0230-522e-4292-8986-357efe281097)


seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/5730a87d-0e0f-4761-9e72-21d0be26e283)


seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/d87e1e89-dd32-4679-a7d5-75abf3a64c54)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/f95aa282-e712-4d0e-b897-b350fdf1bc79)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/9782a9c3-3ea3-4d8f-933e-0581b6894d51)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ea16b4e6-f71a-4721-892f-66149649c6d7)


sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/c05af4f0-3431-45be-8bef-6ac08b4d95ca)

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
![image](https://github.com/user-attachments/assets/1af3717f-b0df-4aa7-bb87-1e75dee39e98)

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
![image](https://github.com/user-attachments/assets/ce35b2bd-95eb-4089-b488-1fb3ab75d432)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/7bc39d86-c4af-4ab2-85ac-9e59084efe5e)

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
![image](https://github.com/user-attachments/assets/be98968a-ae3c-4141-a50b-7e748f2c038b)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/01de9d0b-ea7d-41b1-b726-53de315d9bce)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/ddaae369-5e87-4138-b6af-23b9d92dc9e4)

mkdir backupdir
 
mv backup.tar backupdir
 
## OUTPUT
![image](https://github.com/user-attachments/assets/f9fbc90b-4834-41c7-9dd6-aead28a7de29)

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/62df892d-bf76-4df6-8110-26b63714af14)

gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/user-attachments/assets/7a7c3663-aa95-4e61-91cb-292fc61ea6c1)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/4ec90cf0-1825-4328-a45d-83af2dc6ed26)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World'; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/f1f8390c-bf19-4f31-8edc-4ade6fc0bfc3)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/dbe7b9ab-a41f-46fc-a7dd-4b3bbb1fcb0f)

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
![image](https://github.com/user-attachments/assets/56b40729-faca-45d6-96ba-df935d1f3bf3)

ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/238eb527-a4b1-44aa-90cf-d68003fd6f56)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/91a6cb55-b257-48ba-a500-773aaf349ab0)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/01d596bc-f1c9-4af1-8cba-6b34e64f4867)

abcd
 
echo $?
## OUTPUT
![image](https://github.com/user-attachments/assets/3118c253-3adb-444c-8b93-87ee67eed99d)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/063046ee-f75f-4152-983f-c612249804c6)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/37f4a961-c747-4fb2-82a6-3d1c8699fcdc)

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
![image](https://github.com/user-attachments/assets/24dc6c95-6432-407c-bf08-fe8eb27d9f83)

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
![image](https://github.com/user-attachments/assets/76f1430e-22c9-4868-be6e-a89572f4eb66)


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
![image](https://github.com/user-attachments/assets/1148ea68-0f09-45fd-9e3a-2f4624145609)

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
![image](https://github.com/user-attachments/assets/5ad2bb22-0700-4f01-b3e4-2458906f4349)

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
![image](https://github.com/user-attachments/assets/d089d425-9b17-43f6-8bbf-235b921335c6)

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
![image](https://github.com/user-attachments/assets/8ce226f2-d861-48b1-96f2-ae4812d3c06b)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/ffff6d09-e819-4048-ad37-d89bc07ab56d)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/4da0f011-f8e7-4f01-b890-26807705a49e)

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
$ ./untiltest.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/1b8bb571-6805-4d99-a5f7-e24e71bf3ce7)

 
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
$ ./forin1.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/44348f3a-2278-4737-94c5-275ef5705586)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/83fc6bb5-3825-46fa-a586-232105265197)

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```

$ chmod 755 forin3.sh
$ ./forin3.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/a0f1ebbc-44d8-4df3-b9ff-2cc7f8acdc03)

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

cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

$ chmod 777 forinfile.sh
$./forinfile.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/06154d77-7c30-4a07-8e37-bad79225869d)

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
![image](https://github.com/user-attachments/assets/e73b98fd-61cb-483f-b23c-b99030fc09a1)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/af4050f9-c7fa-4568-a12e-e5781ebd3f02)

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
![image](https://github.com/user-attachments/assets/044cfc01-081d-415c-a1c1-db8c3657a7f3)

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


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/f52b3d06-b9e5-45e9-b91f-6dbced2240e6)

cat forcontinue.sh 
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
echo "The for loop is completed"
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/02b6d33e-b106-4fe5-ae85-8dffcfbfa79f)

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
![image](https://github.com/user-attachments/assets/f21e5ae1-7d46-4f8e-a99f-ddea38b9301e)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. "
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/19bef20d-a78d-4922-af9f-9560682e915c)



 
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
![image](https://github.com/user-attachments/assets/721b3440-fc60-41f3-bbae-7c5d9ae9e1ce)

 ./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/c3626633-09d6-494c-bb78-4089f1765a15)

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
![image](https://github.com/user-attachments/assets/e08494e2-0765-4dfa-bcd2-ee5ebef3fe4b)

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
$ chmod 777 argshift1.sh
## OUTPUT
$ ./argshift1.sh 1 2 3
![image](https://github.com/user-attachments/assets/ad494e30-347c-4e0c-a7ee-b9caf57e2170)

cat argshift3.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +xch
```
## OUTPUT
 ./argshift3.sh 1 2 3
![image](https://github.com/user-attachments/assets/32b02523-c0af-4989-918a-9e80aa508fd9)

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
![image](https://github.com/user-attachments/assets/f74337be-6115-4eba-8e0c-8e685decbc6d)

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
![image](https://github.com/user-attachments/assets/a8e8ff68-ae35-40c3-a383-af474842080e)

# RESULT:
The Commands are executed successfully.
