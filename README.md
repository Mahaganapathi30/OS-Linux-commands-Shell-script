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

<img width="640" height="155" alt="Screenshot 2026-07-28 190159" src="https://github.com/user-attachments/assets/6e828414-5354-4e7b-b729-e138e15e4ebc" />

cat < file2
## OUTPUT

<img width="638" height="177" alt="image" src="https://github.com/user-attachments/assets/fe68eef8-e9a1-4f04-b0bb-0aaf01c827bc" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="636" height="75" alt="image" src="https://github.com/user-attachments/assets/e8350c7a-9cc1-4f6d-a201-cc413f7b939c" />

comm file1 file2
 ## OUTPUT

<img width="638" height="227" alt="image" src="https://github.com/user-attachments/assets/bd457ff2-0cf3-4e9c-b590-d2838a2ef5d3" />
 
diff file1 file2
## OUTPUT

<img width="638" height="276" alt="image" src="https://github.com/user-attachments/assets/a992577e-5ae4-4195-ae12-0fc44f058cc2" />

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

<img width="637" height="229" alt="image" src="https://github.com/user-attachments/assets/e49e8bee-27ad-450a-a8a2-a30a2fb6ae1c" />

cut -c1-3 file11
## OUTPUT

<img width="637" height="103" alt="image" src="https://github.com/user-attachments/assets/13e57ca0-457d-4451-be1f-8011db1299cc" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="638" height="127" alt="image" src="https://github.com/user-attachments/assets/78bf8f93-6ab8-4683-a617-b7d6f82c8b9e" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="641" height="126" alt="image" src="https://github.com/user-attachments/assets/f8504d31-9336-4227-ad69-9b033ffdecef" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world

<img width="644" height="200" alt="image" src="https://github.com/user-attachments/assets/76d7fab4-5f9e-4c8a-b9c9-d91beb7864f5" />

grep Hello newfile 
## OUTPUT

<img width="638" height="76" alt="image" src="https://github.com/user-attachments/assets/57d4102d-912d-427d-8959-f6888c814cdc" />

grep hello newfile 
## OUTPUT

<img width="637" height="73" alt="image" src="https://github.com/user-attachments/assets/01a3322d-b093-40c5-bf79-777abc13d38e" />

grep -v hello newfile 
## OUTPUT

<img width="634" height="72" alt="image" src="https://github.com/user-attachments/assets/ffd27121-71f0-42f3-a271-45f3b8c90b61" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="638" height="102" alt="image" src="https://github.com/user-attachments/assets/42d0f10f-bf98-4e33-900a-27c17cae435d" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="639" height="78" alt="image" src="https://github.com/user-attachments/assets/c2193b33-12cf-4d6d-b3ed-2781b9616445" />


grep -R ubuntu /etc
## OUTPUT

<img width="685" height="576" alt="image" src="https://github.com/user-attachments/assets/8577256c-27e5-480b-b263-fd5cbc79dd7b" />


grep -w -n world newfile   
## OUTPUT

<img width="683" height="100" alt="image" src="https://github.com/user-attachments/assets/b6900d0e-6b1d-4142-8162-2edcdac989b1" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

<img width="686" height="174" alt="image" src="https://github.com/user-attachments/assets/ad945320-8193-4c55-a485-069cdcc8fe6c" />


cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```

<img width="688" height="176" alt="Screenshot 2026-07-28 195541" src="https://github.com/user-attachments/assets/e65fceed-dc95-488f-9c8e-09a8647b4abd" />


egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="686" height="99" alt="image" src="https://github.com/user-attachments/assets/af71b41f-e236-4709-bc11-892dd48f3612" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="684" height="103" alt="image" src="https://github.com/user-attachments/assets/4b876346-19a3-45e0-a422-80fcba5a3495" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="685" height="98" alt="image" src="https://github.com/user-attachments/assets/273302e3-e5d7-423b-a7da-1d0179c136c0" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="686" height="73" alt="image" src="https://github.com/user-attachments/assets/3cec118e-8e3a-41ea-b0ea-ca4f3ee13f4d" />


egrep '(world$)' newfile 
## OUTPUT

<img width="687" height="100" alt="image" src="https://github.com/user-attachments/assets/cf6ca3ca-9183-4ecd-995b-931d4ce49bb5" />


egrep '(World$)' newfile 
## OUTPUT

<img width="677" height="77" alt="image" src="https://github.com/user-attachments/assets/de38c371-0304-4f0e-a73d-fd092cbb24cb" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="692" height="123" alt="image" src="https://github.com/user-attachments/assets/c9c2d94d-0077-4609-9d4d-dab2d8e15444" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="683" height="73" alt="image" src="https://github.com/user-attachments/assets/699cbc30-e5c2-4112-9079-ca45158619bc" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="687" height="74" alt="image" src="https://github.com/user-attachments/assets/9bb0d795-6cd1-46bf-b77d-0b95b17b4eef" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="682" height="75" alt="image" src="https://github.com/user-attachments/assets/b7bc684b-9e0c-45e4-a94c-dd85c4fba37d" />

egrep l{2} newfile
## OUTPUT

<img width="603" height="96" alt="image" src="https://github.com/user-attachments/assets/c5b48abf-0c79-4243-a0ed-69c1a7a1f4b6" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="661" height="125" alt="image" src="https://github.com/user-attachments/assets/09ec28b7-097a-4bfc-a31e-6e245f9388b3" />


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

<img width="688" height="250" alt="image" src="https://github.com/user-attachments/assets/c3c38369-c2b5-4e97-9f0c-cd2f022489bd" />


sed -n -e '3p' file23
## OUTPUT

<img width="350" height="75" alt="image" src="https://github.com/user-attachments/assets/4281112d-4cff-4579-b540-c2f0473c8979" />


sed -n -e '$p' file23
## OUTPUT

<img width="306" height="73" alt="image" src="https://github.com/user-attachments/assets/893e6efa-8ce4-4eab-8de2-e2e39d43b4dc" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="350" height="246" alt="image" src="https://github.com/user-attachments/assets/851c4e86-f9a5-46c7-8543-d22414deb14d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="354" height="249" alt="image" src="https://github.com/user-attachments/assets/8a13a05b-63c1-4671-ada9-afcf8be49b14" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="382" height="250" alt="image" src="https://github.com/user-attachments/assets/36d23031-3290-4124-b3ed-fbf0e3828962" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="328" height="175" alt="image" src="https://github.com/user-attachments/assets/c971e564-9aca-4548-97bf-a096512c2e56" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="361" height="129" alt="image" src="https://github.com/user-attachments/assets/0a763c3a-26b6-476e-8f46-f41eac2b19ac" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="393" height="103" alt="image" src="https://github.com/user-attachments/assets/ebb9b16d-1cd2-49f0-bd5b-2776f97b3930" />


seq 10 
## OUTPUT

<img width="288" height="297" alt="image" src="https://github.com/user-attachments/assets/3eb53d45-ec78-4cbb-838b-1620b0dd6280" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="291" height="126" alt="image" src="https://github.com/user-attachments/assets/488c7810-cfc8-458e-a4b9-6809d602bfdc" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="306" height="122" alt="image" src="https://github.com/user-attachments/assets/ca47d23c-0220-4b4f-aae1-c5da27dbc97e" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="299" height="152" alt="image" src="https://github.com/user-attachments/assets/965bf28d-ed70-4b2b-81ae-f6bc187f0fd4" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="295" height="125" alt="image" src="https://github.com/user-attachments/assets/5267c85e-1ef5-45f4-b57c-88e75e79943d" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="334" height="129" alt="image" src="https://github.com/user-attachments/assets/b33400e6-30ce-4050-b27b-39f8e54ee6b0" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="357" height="126" alt="image" src="https://github.com/user-attachments/assets/4d6cfcfc-0e1d-4fdf-892d-7df946480c92" />


sed -n '2,4{s/$/*/;p}' file23

## OUTPUT
<img width="362" height="121" alt="image" src="https://github.com/user-attachments/assets/c179ea69-937f-4a01-b15d-a5f1a52f1a7d" />



#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

<img width="319" height="173" alt="image" src="https://github.com/user-attachments/assets/66f07d5e-59cc-42c1-8d89-eb7cedffbcc1" />


sort file21
## OUTPUT

<img width="313" height="173" alt="image" src="https://github.com/user-attachments/assets/e3b7c868-1019-496a-af59-1f30573b3d60" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

<img width="311" height="198" alt="image" src="https://github.com/user-attachments/assets/f79ae869-0812-4cd1-880b-43852f55948e" />


uniq file22
## OUTPUT

<img width="317" height="174" alt="image" src="https://github.com/user-attachments/assets/77e20429-b411-447b-a3ed-71ea11e01ddd" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="439" height="253" alt="image" src="https://github.com/user-attachments/assets/ec0a8a16-c112-46a5-b897-0f9f2bfb1536" />


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

<img width="305" height="249" alt="image" src="https://github.com/user-attachments/assets/e35892df-44a2-4365-ab18-a80b4c8d8ff2" />

cat urllist.txt | tr -d ' '
 ## OUTPUT


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="470" height="124" alt="image" src="https://github.com/user-attachments/assets/8537c14f-7a32-4813-8092-a0fb2529bd9f" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="458" height="601" alt="image" src="https://github.com/user-attachments/assets/03d81c1b-8762-4d95-914f-32e0a3a57149" />


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
