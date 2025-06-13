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

![Catfile1](https://github.com/user-attachments/assets/0f6dec43-36ad-41d4-814c-556563871e1e)


cat < file2
## OUTPUT
![catfile2](https://github.com/user-attachments/assets/bc6ece91-3d10-48d8-a339-229c6bdc3747)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![img3](https://github.com/user-attachments/assets/52c8617b-421b-4d95-86c2-490dac04e8cc)

comm file1 file2
 ## OUTPUT

 ![img4](https://github.com/user-attachments/assets/7210f6a5-c939-4fe4-85a1-8f2b417ce76f)


diff file1 file2
## OUTPUT
![img5](https://github.com/user-attachments/assets/cadeaa67-2fa4-4380-8998-0ae95390cbec)


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

![img6](https://github.com/user-attachments/assets/78210ed9-58c6-46f4-9086-4cce1cbe3e3f)



cut -d "|" -f 1 file22
## OUTPUT


![img7](https://github.com/user-attachments/assets/956c6e54-97a5-48c6-9bf9-3200083b0ddd)

cut -d "|" -f 2 file22
## OUTPUT

![img8](https://github.com/user-attachments/assets/4568ca07-c54d-45e5-9434-d3860d525fbe)

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

![img9](https://github.com/user-attachments/assets/ab07a543-eeab-441e-bce1-da730ec07d9e)


grep hello newfile 
## OUTPUT

![img9](https://github.com/user-attachments/assets/6d44ddeb-043d-4e42-89f1-c7fd992478e0)



grep -v hello newfile 
## OUTPUT

![img11](https://github.com/user-attachments/assets/f07b5d66-fd1d-42f2-adf3-a7998cc79119)


cat newfile | grep -i "hello"
## OUTPUT

![img12](https://github.com/user-attachments/assets/9f86f285-8ff4-4bd8-919e-ba4a607f1a82)



cat newfile | grep -i -c "hello"
## OUTPUT

![img13](https://github.com/user-attachments/assets/eabd7750-e396-44b2-8233-38fb0505fd16)



grep -R ubuntu /etc
## OUTPUT

![img14](https://github.com/user-attachments/assets/98a8c55c-23bc-4548-90d5-5e0020d85ebc)


grep -w -n world newfile   
## OUTPUT
![img15](https://github.com/user-attachments/assets/eecf4367-8c20-4d7b-937f-344700f38c4f)


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



egrep -w '(H|h)ello' newfile 
## OUTPUT

![img16](https://github.com/user-attachments/assets/aa684bce-a0f5-4107-bb5e-14c6418494b8)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![img17](https://github.com/user-attachments/assets/5761506a-cd5d-4f67-8622-51f19c287de4)



egrep '(^hello)' newfile 
## OUTPUT

![img19](https://github.com/user-attachments/assets/70317a56-1877-43fe-8cbb-b3c69fde497a)


egrep '(world$)' newfile 
## OUTPUT
![img20](https://github.com/user-attachments/assets/1c7ae2fa-3e6a-4ee2-a4b0-10a22503639b)



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT

![img21](https://github.com/user-attachments/assets/ede6089c-56b8-46f7-8fae-0f0e7a59034c)


egrep '[1-9]' newfile 
## OUTPUT

![img23](https://github.com/user-attachments/assets/39fab0e9-3dde-4ad7-9688-bedc78d85bea)


egrep 'Linux.*world' newfile 
## OUTPUT
![img24](https://github.com/user-attachments/assets/85d91e37-2199-452c-9595-951d55925b65)


egrep 'Linux.*World' newfile 
## OUTPUT


egrep l{2} newfile
## OUTPUT

![img26](https://github.com/user-attachments/assets/629e82b4-4aa9-46b2-a010-6db42c7bbc2e)


egrep 's{1,2}' newfile
## OUTPUT 

![img27](https://github.com/user-attachments/assets/0896b68c-05fa-4910-ab18-589aea0ad336)

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
![img29](https://github.com/user-attachments/assets/8d991a62-0c94-4272-9ad5-5f11d7c296a4)



sed -n -e '$p' file23
## OUTPUT

![img29](https://github.com/user-attachments/assets/e38bc9da-644e-47bd-91be-b031363949ad)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![img30](https://github.com/user-attachments/assets/96f5e8d1-5617-4a73-8d4e-35a96586cf11)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![img31](https://github.com/user-attachments/assets/26d85a9e-1b4b-4267-820d-fe542413a20d)


sed -n -e '1,5p' file23
## OUTPUT

![img32](https://github.com/user-attachments/assets/f68d27cb-2a0a-45b8-8ad6-1d4c2df3bd65)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![img34](https://github.com/user-attachments/assets/0bd70a88-7dff-4954-96b1-a29e2f9588d2)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![img35](https://github.com/user-attachments/assets/6597b055-484c-47d5-9f31-2f4cb7b176ed)


seq 10 
## OUTPUT

![img36](https://github.com/user-attachments/assets/61002d33-72f2-4d03-8499-027da5d070cd)


seq 10 | sed -n '4,6p'
## OUTPUT

![img37](https://github.com/user-attachments/assets/20d31e74-ad5f-4183-8399-ddac6529d7db)


seq 10 | sed -n '2,~4p'
## OUTPUT
![img38](https://github.com/user-attachments/assets/03b166c9-a73d-46cd-8a9f-523150852be9)



seq 3 | sed '2a hello'
## OUTPUT

![img39](https://github.com/user-attachments/assets/b144745f-92f6-4b6b-bc8d-065212208470)


seq 2 | sed '2i hello'
## OUTPUT
![img40](https://github.com/user-attachments/assets/c98c38e5-0a6d-4cae-a9e3-164f7853eb80)


seq 10 | sed '2,9c hello'
## OUTPUT

![img41](https://github.com/user-attachments/assets/389ba5e4-dcac-425f-ab78-c6f393e3f07d)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![img42](https://github.com/user-attachments/assets/88ff6393-d946-440f-bcbc-6bbb56672c5a)


sed -n '2,4{s/$/*/;p}' file23

![img43](https://github.com/user-attachments/assets/6dbdcb58-3833-44bd-a60f-0529e99d2326)

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

![img44](https://github.com/user-attachments/assets/466addb0-44fc-46bb-8bce-e05679c3aecb)

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


![img45](https://github.com/user-attachments/assets/c8ced3db-381c-4e70-82be-e97337b7f407)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![img46](https://github.com/user-attachments/assets/2d87013c-48d0-4ddd-8d78-7f20b55826c0)

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

![img47](https://github.com/user-attachments/assets/0a55849b-31cc-44ca-937b-a1e4a0a9d065)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![img48](https://github.com/user-attachments/assets/a2c20dc4-b609-484a-bc2f-afd06d6f3eca)


#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
![img49](https://github.com/user-attachments/assets/fc90f450-95bb-458a-91d5-d49260535ffd)


tar -xvf backup.tar
## OUTPUT
![img49](https://github.com/user-attachments/assets/625ccbf6-effa-4371-a9f3-0e5b0fd619eb)

gzip backup.tar

ls .gz
## OUTPUT
![img52](https://github.com/user-attachments/assets/7fd62cff-ead8-4ac8-ae1e-5489615b29dc)

gunzip backup.tar.gz
## OUTPUT
![img53](https://github.com/user-attachments/assets/abb4ba8d-8f6e-4b34-bb5a-90fbff869c37)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![img54](https://github.com/user-attachments/assets/b911ce33-3488-48ab-8049-ce1a47f5ceed)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![img55](https://github.com/user-attachments/assets/a202a56c-4c30-4bec-bb46-64b970613881)


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

 ![img56](https://github.com/user-attachments/assets/6139e3de-55cf-460f-9b0c-a0aebcfcd603)

ls file1
## OUTPUT
![img57](https://github.com/user-attachments/assets/85bb75c5-ccee-428a-8bc9-3fbbec585cbb)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?

![img58](https://github.com/user-attachments/assets/bd295b78-163c-455b-b3e6-219d24a0c00c)

## OUTPUT 
 
abcd
 
echo $?


 ## OUTPUT

![img59](https://github.com/user-attachments/assets/964505af-5322-4cd0-acf2-341f9d07f61c)

 
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

![img60](https://github.com/user-attachments/assets/13fb7728-40a8-404b-96d6-62fdf73a0b78)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![img61](https://github.com/user-attachments/assets/8348ee97-621f-410a-b347-b26adf2290d5)


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
![img62](https://github.com/user-attachments/assets/57d013a0-d2e0-4b0f-b8fa-04976d8cbd53)

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

![img63](https://github.com/user-attachments/assets/bfe07e96-5c5c-473e-8272-19fdab91ef79)


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
![img64](https://github.com/user-attachments/assets/3523b532-3f54-4497-b4f9-c864219d060c)

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
![img65](https://github.com/user-attachments/assets/9f6bc45c-1e65-4dba-a328-f461bf54feb1)

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
![img66](https://github.com/user-attachments/assets/76847f2f-78ad-4393-8188-b4f09579419c)


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
![img67](https://github.com/user-attachments/assets/dd06e5cd-f768-4668-98f9-ca16b8fae473)

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
![img69](https://github.com/user-attachments/assets/d6f35b80-d543-47aa-bc39-925cef22f499)


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
![img75](https://github.com/user-attachments/assets/59be15ee-b2b2-4785-868e-9387ad41a472)


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
![img76](https://github.com/user-attachments/assets/d6ced54b-9890-4c8d-9553-c529af2d21e3)

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
![img77](https://github.com/user-attachments/assets/249c51a0-4b8a-46c2-9182-8d77dd66ddc2)

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
![img78](https://github.com/user-attachments/assets/5bd5f899-b83b-492f-9b62-4be4aadf5185)

 
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
 ![img79](https://github.com/user-attachments/assets/a800f1b4-0ead-47f8-99ba-79ea024c4bae)

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
 ![img80](https://github.com/user-attachments/assets/6a5be4dd-d661-4a8d-9b02-c8edcfca737b)

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

![img81](https://github.com/user-attachments/assets/9c47eb05-8a2c-40b7-90e1-091c2847f813)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![img81](https://github.com/user-attachments/assets/81259ebb-276d-444b-a755-d21b88a090af)


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
![img83](https://github.com/user-attachments/assets/fa0bedd4-9bca-4fea-90d6-713e0de51ab7)

 
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
![img84](https://github.com/user-attachments/assets/702ccf15-bfd5-4a8e-9caa-a6f957553d19)

 
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

![img85](https://github.com/user-attachments/assets/47e96d87-301a-4900-9eb5-4ba3a932274d)

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

![img86](https://github.com/user-attachments/assets/6f035bff-da64-4df9-a540-43e1779026f9)

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
 ![img87](https://github.com/user-attachments/assets/f9ca5b68-6cb6-4d08-b0c9-11921a95e2cb)

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

![img88](https://github.com/user-attachments/assets/a2c9c088-0b07-4720-b544-b77a66f53085)

# RESULT:
The Commands are executed successfully
