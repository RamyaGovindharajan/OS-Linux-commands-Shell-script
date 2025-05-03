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

![image](https://github.com/user-attachments/assets/b3db2b73-1975-4fe0-8d03-ae8759f7e20b)


cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/9236d5ca-97c1-489b-9c18-3898eb1c14bd)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/3ebe3974-56dd-4f63-aac7-9a97a43c3926)
 
comm file1 file2
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/26226eea-3910-49be-9f23-00cb012e5f5d)
 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/e30eacad-9e3b-4ad5-87e0-79176a4afb80)

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


![image](https://github.com/user-attachments/assets/e05ab576-b979-4c2d-addb-ee679069fcf7)

cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/cf8837c0-7e39-479b-86cc-f28e349e9e45)

cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/016455ad-5b8b-45fa-be11-cf766815aae0)

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

![image](https://github.com/user-attachments/assets/ee270fc1-5ea6-41fd-92ab-1d75034a419e)



grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/92960f34-6f44-4738-ae47-12be64556e0f)


grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d26fede0-a5bc-499c-9387-15afdbac6de7)

cat newfile | grep -i "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/29f1b961-493c-4527-a39d-81697db11f2c)

cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/7dd49588-6170-4e81-a376-6f37d4c054ee)


grep -R ubuntu /etc
## OUTPUT

grep![Screenshot from 2025-04-18 18-32-53](https://github.com/user-attachments/assets/d9bb1cc3-e10a-42de-981c-c8fc9d673e4d)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/94d75f84-db24-463e-9042-dd579fcf35e0)


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

![image](https://github.com/user-attachments/assets/aec74743-0d3b-4253-ae95-783fe5b55b85)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/99232cac-8a27-4a59-9e10-5ef9b5dcd097)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/d9cb25d7-2992-4ccd-949e-eaa7fa5dab30)

egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/50ebb049-cd48-4c15-9d35-2f9d386877bd)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d2f59f84-7bd3-423a-88c9-07837668aaf6)

egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/78004cf6-a59a-4e60-b7bb-bd77ca8428b7)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/297a5a5b-8c1e-4354-9c8e-7feb0ad9a57d)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b7e22f73-bc78-452e-9b2a-a010bb273b71)

egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/31462f65-4b1b-410c-a574-2600fd56c10d)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/05f8a7a9-e5a8-40dd-884a-14bb6ad12bf9)


egrep l{2} newfile
## OUTPUT

egrep![Screenshot from 2025-04-18 18-34-31](https://github.com/user-attachments/assets/5b5b5b51-6f63-49e6-ae35-b9e858ee7e29)


egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-04-18 18-35-20](https://github.com/user-attachments/assets/bd5a2144-e6e9-4264-be87-291becdaa05e)


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

![image](https://github.com/user-attachments/assets/937f29af-b87a-4d5f-832c-f49239fdb684)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/f1b97470-dd89-44d4-a1a4-93d8eb5ecdd1)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/2e7ec78a-58ae-48fd-815b-954064fb503c)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/51b20d2d-fa27-42d5-b5e2-7cd309596a33)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/b0a18462-94f3-4114-9c26-0e8bea37b537)



sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/69d4f4a3-9ef2-4dfd-b55f-5c252b43bed6)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/bc67a5da-183f-4ed3-98f5-60081da7a746)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/26d0dddb-bd86-4717-ab41-33794970b0fd)


seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/21592950-c8c2-434d-9117-041a962be6db)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/96673e0e-e0cb-4e1a-8473-124984a62293)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/43e77fcd-4702-4995-bf14-c0d25a4a8654)



seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/92f99976-6df9-4721-b6c8-e6786381bd9f)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/df1e8962-7fdb-4b18-8d5c-3df841b440a2)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/e13328f8-f33e-4c39-b8d5-69576fe3df77)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/08821d66-0b51-404c-bd70-2ab3927199a4)




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
![image](https://github.com/user-attachments/assets/b6b7314b-7034-449a-ae22-627f7de810f0)


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
![image](https://github.com/user-attachments/assets/303bce5e-d9ca-4cba-94ae-200cb3c2c09d)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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

![image](https://github.com/user-attachments/assets/746e75e5-fccb-44f0-88d9-123fe68c6cf4)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/e4ef5666-8daa-4f06-81a3-e9c4f1e192db)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2025-04-18 18-37-27](https://github.com/user-attachments/assets/67a5923d-828a-4b74-bf15-75c0b391cf36)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2025-04-18 18-37-27](https://github.com/user-attachments/assets/838094d6-16ca-4ad5-9873-69fc9ea7048c)


tar -xvf backup.tar
## OUTPUT
![Screenshot from 2025-04-18 18-37-27](https://github.com/user-attachments/assets/112f73f8-4d18-4118-881f-252608110ae9)

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
![Screenshot from 2025-04-18 18-37-27](https://github.com/user-attachments/assets/04311ef4-fd2e-478e-affe-eae1d1711571)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2025-04-18 18-39-29](https://github.com/user-attachments/assets/18256c31-eb39-4a42-9c20-771d8f76bf8c)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/e1653584-eae8-47d8-adc1-1546d99451ee)


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

 ![image](https://github.com/user-attachments/assets/d0776c2f-630a-4e07-9ad6-2878b11e3868)

ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/80e3be46-51b5-4666-8c97-055ced94ff45)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/bc610602-d0fd-43b2-a444-5f6eb57688e2)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/e1ba3f77-72f9-455f-a884-6ed25a7e00c2)

abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/3fb15207-e035-470c-a414-3bd550feec86)

 
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
![image](https://github.com/user-attachments/assets/ef94d6b2-93ce-4f95-be48-1c6ccb863eea)



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
![image](https://github.com/user-attachments/assets/ec0421c2-ecd4-44cd-853c-4d09f3254c38)


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
![image](https://github.com/user-attachments/assets/627af4bc-7157-4cef-9cb8-907c1bd5b40f)



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
![image](https://github.com/user-attachments/assets/9047bfe9-6e37-499e-bf4b-411fca7b160c)


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
![image](https://github.com/user-attachments/assets/c86ce2a2-b441-4778-bac2-99c6da45b12a)

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
![image](https://github.com/user-attachments/assets/7bd72773-198e-4998-b419-390966cb473f)


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
![image](https://github.com/user-attachments/assets/4ec86a81-a899-4902-8ed5-475071270ff1)

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
![image](https://github.com/user-attachments/assets/ac94d747-068a-4c63-a8b9-d0089406a666)

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
![image](https://github.com/user-attachments/assets/ed350261-2b38-4c00-b555-facdb101cf18)



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
![image](https://github.com/user-attachments/assets/363015ac-7c35-424a-abd1-cfa37e1edc07)


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
![image](https://github.com/user-attachments/assets/c1cc8ef1-93bd-44f4-a4e7-d4f0110963c8)


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
 
![image](https://github.com/user-attachments/assets/70184d64-45cc-4ff5-993a-94df1b8d4a75)

 
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
![image](https://github.com/user-attachments/assets/bf8eefcf-f558-4488-b264-bce50eb94b71)


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

 ![image](https://github.com/user-attachments/assets/8de69f97-d734-46e0-b9e0-3559e01f7def)

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

![image](https://github.com/user-attachments/assets/d3435a5f-0597-4f27-838c-40233646f140)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image](https://github.com/user-attachments/assets/29537ff5-e46b-4293-a833-dc52f530833c)



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
![image](https://github.com/user-attachments/assets/c9ad827e-0317-457a-b1d7-c9e4ed4c5603)

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
![image](https://github.com/user-attachments/assets/c17808f5-b4eb-4bb7-b458-5fe94ea6dc1a)

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
 ![image](https://github.com/user-attachments/assets/3704fab1-db17-4351-bd6e-ee2cfabb7d2b)

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
 ![image](https://github.com/user-attachments/assets/74e3d547-a0ce-43be-bbcd-473cba484c1f)

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
![image](https://github.com/user-attachments/assets/7d775189-e3bd-460c-97c2-19cba1525fd1)

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
![image](https://github.com/user-attachments/assets/8ed9fe5e-b64c-43f0-8954-57f48a5a9139)


# RESULT:
The Commands are executed successfully.


