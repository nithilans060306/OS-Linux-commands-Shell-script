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

![image](https://github.com/user-attachments/assets/62e21401-d8eb-48bf-bb41-18555c311d81)


cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/d7adae03-f296-42db-b6eb-ef53e76952de)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/1c2dff85-9559-4245-a5cf-80f5ee2925d0)

comm file1 file2
 ## OUTPUT

 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/590f1e25-a31a-4c96-a30d-3412369a4d96)

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

![image](https://github.com/user-attachments/assets/383e0b6f-8002-4ac2-8603-381b798657ea)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot 2024-09-16 205549](https://github.com/user-attachments/assets/6ec70330-b950-433d-b431-1e6a2841ea6e)


cut -d "|" -f 2 file22
## OUTPUT

![Screenshot 2024-09-16 205604](https://github.com/user-attachments/assets/9ec7bdc1-d0db-45cb-80cb-81d8d9978960)

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

![Screenshot 2024-09-16 210058](https://github.com/user-attachments/assets/ddbe56c9-43f4-4c3a-bba3-a8919c38cb53)


grep hello newfile 
## OUTPUT

![Screenshot 2024-09-16 210613](https://github.com/user-attachments/assets/3d3e7edc-0fc0-4b7c-aa84-f24e0c67bf5d)



grep -v hello newfile 
## OUTPUT

![Screenshot 2024-09-16 210841](https://github.com/user-attachments/assets/29ba281a-51f4-44fc-a294-8a9866b72658)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot 2024-09-16 211058](https://github.com/user-attachments/assets/662f2787-9e8a-45a8-a9dc-357bf32c6a23)



cat newfile | grep -i -c "hello"
## OUTPUT


![Screenshot 2024-09-16 211141](https://github.com/user-attachments/assets/4193d629-9b79-4066-b5ad-645146866914)


grep -R ubuntu /etc
## OUTPUT

![Screenshot 2024-09-16 212038](https://github.com/user-attachments/assets/052850f1-9d1a-4c24-bc48-b5d0b9c100c6)


grep -w -n world newfile   
## OUTPUT

![Screenshot 2024-09-16 213812](https://github.com/user-attachments/assets/24f266e3-ca55-4ba1-b138-a6edbf82251f)

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

![Screenshot 2024-09-16 214353](https://github.com/user-attachments/assets/8300144e-06f8-49c8-b91d-063d25f36b0f)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2024-09-16 214554](https://github.com/user-attachments/assets/1c74d201-58a3-44f8-ba5d-b3b3ae55f541)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![Screenshot 2024-09-16 214635](https://github.com/user-attachments/assets/3fac97f4-43be-4aa3-af93-119fce5516a7)


egrep '(^hello)' newfile 
## OUTPUT

![Screenshot 2024-09-16 215145](https://github.com/user-attachments/assets/fb67ad53-ce79-415e-b051-3f1fc07bf272)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot 2024-09-16 215110](https://github.com/user-attachments/assets/d32cd64c-b2c0-408c-9aa4-9c7e5510aa55)


egrep '(World$)' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/9359179d-1e02-458a-8983-ab036881419d)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot 2024-09-16 215241](https://github.com/user-attachments/assets/823cf508-d45e-4ef0-bb1e-a5c677f95efe)


egrep '[1-9]' newfile 
## OUTPUT


![Screenshot 2024-09-16 215344](https://github.com/user-attachments/assets/339ca14f-6879-47d6-b347-db1c2e6cfa21)


egrep 'Linux.*world' newfile 
## OUTPUT


![Screenshot 2024-09-16 215504](https://github.com/user-attachments/assets/bfb85956-cf1a-472b-a18c-fc3f487c7af7)

egrep 'Linux.*World' newfile 
## OUTPUT


![Screenshot 2024-09-16 215537](https://github.com/user-attachments/assets/020e07bd-01be-4be3-bc05-e4c826729186)

egrep l{2} newfile
## OUTPUT


![Screenshot 2024-09-16 215636](https://github.com/user-attachments/assets/b5277ee9-9691-4fc7-8d57-8cacc5be6367)


egrep 's{1,2}' newfile
## OUTPUT 


![Screenshot 2024-09-16 215720](https://github.com/user-attachments/assets/c0aa127c-c530-453d-b916-7af273bfc484)


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


![Screenshot 2024-09-16 225536](https://github.com/user-attachments/assets/f9906097-d8d5-4c87-80c5-3a60719e8056)


sed -n -e '$p' file23
## OUTPUT


![Screenshot 2024-09-16 231247](https://github.com/user-attachments/assets/dd5339c2-6d00-4a2e-84d7-35c2a25be57b)


sed  -e 's/Ram/Sita/' file23
## OUTPUT


![Screenshot 2024-09-16 231405](https://github.com/user-attachments/assets/d510d6e2-4239-4b06-9c13-09ca44558458)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


![Screenshot 2024-09-16 231451](https://github.com/user-attachments/assets/34ac90e3-4244-403a-9179-e7acf42ac36c)


sed  '/tom/s/5000/6000/' file23
## OUTPUT


![Screenshot 2024-09-16 231649](https://github.com/user-attachments/assets/eee72091-bd0b-4807-81e8-cc56b8305fb7)


sed -n -e '1,5p' file23
## OUTPUT


![Screenshot 2024-09-16 231907](https://github.com/user-attachments/assets/c3f70318-3bff-4f48-9e0a-a8ac4547cc51)


sed -n -e '2,/Joe/p' file23
## OUTPUT



![Screenshot 2024-09-16 231738](https://github.com/user-attachments/assets/95647b0d-13f5-4db8-b747-014e133d1880)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![Screenshot 2024-09-16 232023](https://github.com/user-attachments/assets/cf9b0c62-da52-42c4-9aca-709af8ff0f96)


seq 10 
## OUTPUT


![Screenshot 2024-09-16 232056](https://github.com/user-attachments/assets/d6fb65b4-df40-4bf6-8b5c-4ba00ea5422d)


seq 10 | sed -n '4,6p'
## OUTPUT


![Screenshot 2024-09-16 232244](https://github.com/user-attachments/assets/91f8304e-7f0c-4544-a4ba-feac2338da54)


seq 10 | sed -n '2,~4p'
## OUTPUT


![Screenshot 2024-09-16 232200](https://github.com/user-attachments/assets/ca2dbf25-c8a0-4cd7-9106-d7f6ecb97ec1)


seq 3 | sed '2a hello'
## OUTPUT


![Screenshot 2024-09-16 232601](https://github.com/user-attachments/assets/05c2b182-abe1-494e-b0e9-207deb6c805c)


seq 2 | sed '2i hello'
## OUTPUT


![Screenshot 2024-09-16 232526](https://github.com/user-attachments/assets/e39c77e9-5974-4d6b-9424-0fa63a1bb14e)

seq 10 | sed '2,9c hello'
## OUTPUT


![Screenshot 2024-09-16 232438](https://github.com/user-attachments/assets/540911b0-bc5e-4cc1-9299-6d3bc37c8d33)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


![Screenshot 2024-09-16 232713](https://github.com/user-attachments/assets/fca54d8a-be10-4ad1-afee-de82a67e88ed)


sed -n '2,4{s/$/*/;p}' file23

![Screenshot 2024-09-16 233151](https://github.com/user-attachments/assets/f77b75de-0246-45af-89e4-08c934e033c3)


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

![Screenshot 2024-09-16 233536](https://github.com/user-attachments/assets/bc6e5cef-82e2-45d9-93a0-d8c689847dcd)


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


![Screenshot 2024-09-16 233649](https://github.com/user-attachments/assets/26edbb9c-6e07-438a-b6ff-42cc823e4f5b)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![Screenshot 2024-09-16 233756](https://github.com/user-attachments/assets/91692416-74f0-46d0-9e0d-fa7c5613497d)

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


![Screenshot 2024-09-16 234507](https://github.com/user-attachments/assets/1bb32dc1-c60e-4752-b39f-aebc3cfd222a)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


![Screenshot 2024-09-16 234225](https://github.com/user-attachments/assets/dd95d30c-efa2-426f-afe2-8dcfe4045b15)


#Backup commands
tar -cvf backup.tar *
## OUTPUT


![Screenshot 2024-09-16 234648](https://github.com/user-attachments/assets/d9937f4f-9ef2-4107-960c-a8fc6bef651a)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/d7c607da-012b-4200-a6b0-d3ad6b8afcd9)

tar -xvf backup.tar
## OUTPUT
cd ![image](https://github.com/user-attachments/assets/af6b24ba-ca30-4646-ba98-afc9f3738983)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/42143ae3-b9f6-4cf3-988a-6ab622a86cd8)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/ce75d6bb-c72c-4b31-8997-669ad8ff20a3)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/df43fccc-2ce5-4f88-840a-c88dec5e459d)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/eacd5bf8-ecbd-4da6-a174-2ee5bfb67687)

cat < scriptest.sh 
```bash
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

 ![image](https://github.com/user-attachments/assets/ee27735d-1569-4e30-ae48-2a177137a372)

ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/b9ad190c-a354-4dd6-8656-325ae0160954)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/b5bdf082-5008-4402-b6ee-e35d3d90b141)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/92ffe941-3fe1-4f10-a31d-5a094fcf4ffe)

abcd


echo $?
 ## OUTPUT
![image](https://github.com/user-attachments/assets/57e26d7b-3121-4466-933e-97c656b376ec)

 
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

![image](https://github.com/user-attachments/assets/f4e1794f-a193-4203-81eb-f7d1f9efe445)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/7bf538fc-b877-4645-ba59-c1780459f7db)


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
![image](https://github.com/user-attachments/assets/04b5a431-a997-4427-8a55-2675c6a78639)

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

![image](https://github.com/user-attachments/assets/a44406ff-9808-4b21-b629-32e0993371d4)


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
## OUTPUT
![image](https://github.com/user-attachments/assets/09eb951a-4128-44ea-a040-2332016e74b2)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/643fd8ed-ec6f-4cc4-af32-4857f3caf52c)

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
![image](https://github.com/user-attachments/assets/28112de8-32a4-4c34-a8c7-320d07dee4c5)


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
![image](https://github.com/user-attachments/assets/b5818c5e-c155-43a7-80c1-12e2dc02d787)

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
![image](https://github.com/user-attachments/assets/7c8f909f-daa0-49b4-a901-0f179cfd268e)

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
 ![image](https://github.com/user-attachments/assets/07fdf81f-1aed-439d-9ec0-e721fd3c1ebb)

 
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
 
 ![image](https://github.com/user-attachments/assets/68cd5d2a-67ed-4627-b78c-727ded08bd32)
 
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
 ## OUTPUT
![image](https://github.com/user-attachments/assets/dd748411-1cfb-430f-ab83-4e2e9e3f31b3)

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
 ![image](https://github.com/user-attachments/assets/14727090-30f1-4d9a-ae98-0a738fa2a4a1)

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
 ![image](https://github.com/user-attachments/assets/d21864fd-bf5a-4ab2-85ec-a21d0d3110c3)

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
![image](https://github.com/user-attachments/assets/7084ee73-b50d-408a-80c4-2c5ff98594c5)

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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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
