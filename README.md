# Exp 01 - OS Linux commands Shell scripting
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
![image](https://github.com/user-attachments/assets/6fccd523-1904-4548-b48c-b634a6760137)



cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/5e15f943-716c-4d13-8736-dd26cd96e5c4)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/3c00b5bd-6bf1-474e-96c2-e136feb99ced)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/b1cb74f1-7090-425e-8d28-4e8d23fb7bee)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/725a14d5-e419-4221-bfa2-97f2580ddd07)


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
![image](https://github.com/user-attachments/assets/8ed6ef0a-beba-4473-8df0-8d1687a2fe43)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/cd1005ad-c27e-4fbd-ac2e-54af177ee6b6)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/4a68ab21-b372-42f2-bd6a-d176014baea9)


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
![image](https://github.com/user-attachments/assets/17ceda92-2d8a-4bf0-90a4-d7596be63ed4)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d3c26ea6-3a5c-4cd4-ae93-42c5e80bc733)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e8df394a-05d0-4656-91fd-edc5d244d047)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/cc868b4c-3718-4d99-b743-76e442a0b066)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/61c05a75-577c-4ce6-b159-e3532397d417)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/0546c10e-5a52-4333-971a-d8e04730fd56)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/8dc7e9f0-17fc-4d61-b93a-58a0d6e819ac)


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

![image](https://github.com/user-attachments/assets/feb84853-5607-4c01-b959-42f69bdefa06)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/731431c5-079c-4ccf-8db4-021ca6089613)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/12d44307-7b36-4ace-af07-9072125006b0)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b5d7ada9-b952-4770-a459-bb304bec478e)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/41eed109-ea90-40a3-a999-bc0c04c010bd)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/57ffadc5-7e18-429e-ba6e-e12120aa1c76)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/496d2ed3-92b4-45d0-a55a-78bb1d514b38)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/5ce956c9-6405-44f8-9f92-26c7cbc398f2)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a6933d1f-57f4-465b-80ad-e62090dfbd61)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/83c2e168-7f8a-438a-aa0d-86e7ec60108d)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/7af0fc66-1e70-439e-939d-7e084130f16a)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/377117ef-9e97-4e60-854d-45996cd2847f)


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
![image](https://github.com/user-attachments/assets/c2ce5a93-5668-406c-a9c1-84bf3754db39)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8364bc33-4a9f-4159-ad02-af8b07cfa6d3)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/9228794d-8a6e-4cff-be5f-cf1039db1ed8)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ca777e2e-1a54-4005-b7b3-bd7821535088)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ce747184-bfa9-43b1-afa6-f78bfd1e8abb)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ab460fd6-0660-4086-b2cf-0ddb568f9d7a)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1060fffe-7270-4177-afd9-35174a759c83)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8e631c64-d22e-4dd4-a5aa-ad7a4b805bc4)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/039b436a-8ce8-43ce-a19a-50529d276d87)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/0446a37b-d933-4a62-b80b-0343a6bffb7d)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/966bff2f-6c65-4ddd-b8e8-ee600752b064)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/096a7214-6145-4a00-b974-88af55b560fe)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/2cefa889-0a78-4333-ac13-97f748021c3b)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/c5562130-1224-4718-9bde-1593cf9f541a)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1a4b9649-70a5-4415-adbc-3c5f555e746f)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/c47d7762-0c14-45c9-a6ed-531552035674)


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
![image](https://github.com/user-attachments/assets/1c75ce5d-8eb5-450c-8e8e-7dc22a322cc6)


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
![image](https://github.com/user-attachments/assets/cfe9c371-e39e-4eaa-baaf-d3b617c9c403)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/39621e59-7e7d-4a5f-b2b0-71d0077080e0)


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
![image](https://github.com/user-attachments/assets/6e523c66-2a83-4c16-a19c-faeb11b9b11c)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/5637df83-3650-4995-b77b-19762d604b2b)



## Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/af83ce0c-e18b-4be3-8416-8bbdee59d907)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/4f102ba9-53e9-4a0e-9ebb-0c24413fc87d)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/98ea7d57-4da9-4d24-a68c-013f91e55229)


gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/user-attachments/assets/e54af9c7-1ac4-4bed-a203-c6b780523329)



gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/079e2bbb-e95b-4761-bd61-789f1a3dd55f)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/e4af163e-b80a-40fc-bcf1-fa93109286af)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/14ac7075-3b09-4e91-add5-3456bb13fc66)


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
![image](https://github.com/user-attachments/assets/b953a2f3-5513-4a29-9de6-431e1489c581)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/e988dd15-3557-4cdc-9c5a-56afc6dc70ce)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/d39c5f62-2db3-4955-84c9-6f954d50ae18)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/a7d96713-1af4-4dcf-ab74-70411b23153f)

 
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

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/b10f44ee-7d68-4422-af94-d333b28feff2)



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
![image](https://github.com/user-attachments/assets/fdc676c2-30b4-4cb5-856a-0f8a4ad6e040)


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
![image](https://github.com/user-attachments/assets/005816e4-afad-4995-9435-ee00da64d1fd)



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
![image](https://github.com/user-attachments/assets/4ef6ef44-0b5f-48ac-a075-9ba22be5807d)


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
![image](https://github.com/user-attachments/assets/a8130528-2907-4ace-9b34-4a1d6f314c66)


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
![image](https://github.com/user-attachments/assets/ab09b9e2-280f-4fe8-8351-91a7a6c74c85)


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
![image](https://github.com/user-attachments/assets/fef988a9-668c-4c57-9390-06195de6ec87)


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
![image](https://github.com/user-attachments/assets/b67efcf5-eecc-43f2-a682-6410eeed0e41)


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
![image](https://github.com/user-attachments/assets/0a0c9627-d9fa-417b-b678-1c75ce570039)

 
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
## OUTPUT
![image](https://github.com/user-attachments/assets/11a5b76e-dc51-4cd8-be25-3eaec6999d94)

 
 
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
![image](https://github.com/user-attachments/assets/7c63c81f-e699-4029-ad04-5b32b616f33c)

 
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
## OUTPUT
![image](https://github.com/user-attachments/assets/09afc6ba-de5f-42a1-b5ef-b7b9d71e0e3b)


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
## OUTPUT
![image](https://github.com/user-attachments/assets/2ba66689-930f-4f5e-a005-1d18c1402ec0)


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
$ cat>cities
```
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```
## OUTPUT
![image](https://github.com/user-attachments/assets/a137aaa7-9661-49c3-b4a6-eb739bd0e876)



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
![image](https://github.com/user-attachments/assets/3072743a-9691-40b4-99ab-5d9189afd9ea)


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
![image](https://github.com/user-attachments/assets/17775c12-db30-4953-8c3e-1c80482a0cd3)


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
![image](https://github.com/user-attachments/assets/88560eb0-ff33-47e4-81bb-88d413240e20)

 
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
![image](https://github.com/user-attachments/assets/170e8101-2eaa-49c5-9389-b98ec10467be)


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
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/295e60f5-4274-4953-a0df-f0881c625371)

 
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
![image](https://github.com/user-attachments/assets/482c630c-3b9b-42d1-8f95-dcdb431ce8bd)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/a307d5a2-dcea-4379-8a73-4d19df5e70a6)



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
./funcex.sh 
 ./funcex.sh 1 2
## OUTPUT
![image](https://github.com/user-attachments/assets/4c206ec8-5809-40bb-8a55-3f72201ffb24)

![image](https://github.com/user-attachments/assets/5355b55a-8615-41eb-b2d6-1291bd114e7a)

 


 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/user-attachments/assets/dd025c0c-d7c2-4882-840e-4070d5e4644b)


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
$ ./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/user-attachments/assets/e4709e9d-080d-4670-b104-e6616064ce80)

 
cat argshift2.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
 ./argshift2.sh 1 2 3
## OUTPUT

![image](https://github.com/user-attachments/assets/77fa2545-28db-4def-a70f-2e4d1dae8f1a)

 
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
![image](https://github.com/user-attachments/assets/209171aa-f009-4f76-b623-c8b364c8f21a)

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
![image](https://github.com/user-attachments/assets/c67d9c34-9a34-4dba-a619-589ee9ceca73)


# RESULT:
The Commands are executed successfully.
