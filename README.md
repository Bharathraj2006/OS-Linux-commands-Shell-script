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
```
cat > file1
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
```
```
cat > file2
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
```
### Display the content of the files
```cat < file1```
## OUTPUT
![com1](<outputs/Screenshot from 2024-08-22 08-15-13.png>)

```cat < file2```
## OUTPUT
![com2](<outputs/Screenshot from 2024-08-22 08-16-35.png>)

# Comparing Files
```cmp file1 file2```
## OUTPUT
![com3](<outputs/Screenshot from 2024-08-22 08-18-16.png>)

```comm file1 file2```
## OUTPUT
![com4](<outputs/Screenshot from 2024-08-22 08-21-30.png>)

```diff file1 file2```
## OUTPUT
![com5](<outputs/Screenshot from 2024-08-29 09-27-07.png>)

# Filters

### Create the following files file11, file22 as follows:
```
cat > file11
Hello world
This is my world
```
```
cat > file22
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
```
```
cut -c1-3 file11
```
## OUTPUT
![com6](<outputs/Screenshot from 2024-08-29 09-35-38.png>)

```
cut -d "|" -f 1 file22
```
## OUTPUT

![com7](<outputs/Screenshot from 2024-08-29 09-36-57.png>)

```
cut -d "|" -f 2 file22
```
## OUTPUT
![com8](<outputs/Screenshot from 2024-08-29 09-39-02.png>)
```
cat < newfile 
Hello world
hello world
```
```
cat > newfile 
Hello world
hello world
```
```
grep Hello newfile 
```
## OUTPUT
![com9](<outputs/Screenshot from 2024-08-29 09-44-51.png>)

```
grep hello newfile 
```
## OUTPUT
![com10](<outputs/Screenshot from 2024-08-29 09-47-47.png>)

```
grep -v hello newfile 
```
## OUTPUT
![com11](<outputs/Screenshot from 2024-09-01 12-39-14.png>)

```
cat newfile | grep -i "hello"
```
## OUTPUT

![com12](<outputs/Screenshot from 2024-09-01 12-40-44.png>)

```
cat newfile | grep -i -c "hello"
```
## OUTPUT

![com13](<outputs/Screenshot from 2024-09-01 12-42-30.png>)

```
grep -R ubuntu /etc
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-04 09-27-56.png>)
![com](<outputs/Screenshot from 2024-09-04 09-28-13.png>)
![com](<outputs/Screenshot from 2024-09-04 09-28-17.png>)
![com](<outputs/Screenshot from 2024-09-04 09-28-20.png>)
![com](<outputs/Screenshot from 2024-09-04 09-28-23.png>)
![com](<outputs/Screenshot from 2024-09-04 09-28-26.png>)
```
grep -w -n world newfile  
```
## OUTPUT
![com14](<outputs/Screenshot from 2024-09-01 12-49-29.png>)

```
cat < newfile 
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
```
```
cat > newfile
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
```

```
egrep -w 'Hello|hello' newfile 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 12-54-12.png>)

```
egrep -w '(H|h)ello' newfile 
```
## OUTPUT

![com](<outputs/Screenshot from 2024-09-01 12-55-37.png>)

```
egrep -w '(H|h)ell[a-z]' newfile 
```
## OUTPUT

![com](<outputs/Screenshot from 2024-09-01 12-56-19.png>)

```
egrep '(^hello)' newfile 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 12-57-50.png>)


```
egrep '(world$)' newfile 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 12-58-38.png>)


```
egrep '(World$)' newfile 
```
## OUTPUT

![com](<outputs/Screenshot from 2024-09-01 12-59-32.png>)
```
egrep '((W|w)orld$)' newfile 
```
## OUTPUT

![com](<outputs/Screenshot from 2024-09-01 13-00-19.png>)
```
egrep '[1-9]' newfile 
```
## OUTPUT

![com](<outputs/Screenshot from 2024-09-01 13-01-50.png>)

```
egrep 'Linux.*world' newfile 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-02-53.png>)
```
egrep l{2} newfile
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-03-50.png>)

```
egrep 's{1,2}' newfile
```
## OUTPUT 
![com](<outputs/Screenshot from 2024-09-01 13-04-43.png>)

```
cat > file23
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
```

```
sed -n -e '3p' file23
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-06-31.png>)
```
sed -n -e '$p' file23
```
## OUTPUT

![com](<outputs/Screenshot from 2024-09-01 13-07-52.png>)
```
sed  -e 's/Ram/Sita/' file23
```
## OUTPUT

![com](<outputs/Screenshot from 2024-09-01 13-08-35.png>)
```
sed  -e '2s/Ram/Sita/' file23
```

## OUTPUT

![com](<outputs/Screenshot from 2024-09-01 13-09-22.png>)
```
sed  '/tom/s/5000/6000/' file23
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-10-39.png>)

```
sed -n -e '1,5p' file23
```
## OUTPUT
![com](<Screenshot from 2024-09-01 13-12-29.png>)

```
sed -n -e '2,/Joe/p' file23
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-15-55.png>)

```
sed -n -e '/tom/,/Joe/p' file23
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-16-56.png>)
```
seq 10 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-45-10.png>)


```
seq 10 | sed -n '4,6p'
```
## OUTPUT

![com](<outputs/Screenshot from 2024-09-01 13-46-36.png>)

```
seq 10 | sed -n '2,~4p'
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-47-26.png>)

```
seq 3 | sed '2a hello'
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-48-05.png>)

```
seq 2 | sed '2i hello'
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-50-23.png>)

```
seq 10 | sed '2,9c hello'
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-51-22.png>)

```
sed -n '2,4{s/^/$/;p}' file23
```
## OUTPUT

![com](<outputs/Screenshot from 2024-09-01 13-52-45.png>)

```
sed -n '2,4{s/$/*/;p}' file23
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-55-04.png>)

# Sorting File content

```
cat > file21
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
```
sort file21
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-57-16.png>)


```
cat > file22
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
```
uniq file22
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-58-09.png>)

# Using tr command
```
cat file23 | tr [:lower:] [:upper:]
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 13-59-24.png>)


```
cat < urllist.txt
www. yahoo. com
www. google. com
www. mrcet.... com
```

```
cat > urllist.txt
www. yahoo. com
www. google. com
www. mrcet.... com
```
```
cat urllist.txt | tr -d ' '
```
 ## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 14-02-09.png>)

```
cat urllist.txt | tr -d ' ' | tr -s '.'
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 14-03-13.png>)

# Backup commands
```
tar -cvf backup.tar *
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-01 14-05-17.png>)
![com](<outputs/Screenshot from 2024-09-03 08-24-16.png>)
```
mkdir backupdir
mv backup.tar backupdir 
tar -tvf backup.tar
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-03 08-33-16.png>)

```
tar -xvf backup.tar
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-03 08-35-02.png>)

```
gzip backup.tar
ls *.gz
```

## OUTPUT
 ![com](<outputs/Screenshot from 2024-09-04 09-36-07.png>)

```
gunzip backup.tar.gz
ls *.tar
```
## OUTPUT 
![com](<Screenshot from 2024-09-04 09-44-03.png>)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
```
chmod 755 my-script.sh
./my-script.sh
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 15-53-15.png>)
```
cat << stop > herecheck.txt
```
```
hello in this world
i cant stop
for this non stop movement
stop
cat herecheck.txt
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-04 17-58-20.png>)

```
cat < scriptest.sh 
```
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
```
![com](<outputs/Screenshot from 2024-09-04 18-51-59.png>)
```
cat scriptest.sh 
```
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
```
chmod 777 scriptest.sh
./scriptest.sh 1 2 3
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-04 18-52-16.png>)
 
```
ls file1
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-04 18-55-15.png>)
```
echo $?
```
## OUTPUT 
![com](<outputs/Screenshot from 2024-09-04 18-56-02.png>)
```
./one bash: ./one: Permission denied
echo $?
```
## OUTPUT 
![com](<outputs/Screenshot from 2024-09-08 15-58-11.png>)
```
abcd
echo $?
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 16-00-44.png>)

# mis-using string comparisons

```
cat > strcomp.sh 
```
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
```
cat strcomp.sh 
```
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
![com](<outputs/Screenshot from 2024-09-04 19-02-56.png>)


```
chmod 755 strcomp.sh
./strcomp.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-04 19-04-46.png>)

# check file ownership
```
cat > psswdperm.sh 
```
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
```
```
cat psswdperm.sh 
```
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
```
```
./psswdperm.sh
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 13-15-52.png>)

# check if with file location

```
cat>ifnested.sh 
```
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
```
cat ifnested.sh 
```
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
```
./ifnested.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 13-18-58.png>)

# using numeric test comparisons
```
cat > iftest.sh 
```
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
```
cat iftest.sh 
```
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
```
$ chmod 755 iftest.sh
$ ./iftest.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 13-20-49.png>)

# check if a file
```
cat > ifnested.sh
``` 
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
```
cat ifnested.sh 
```
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
```
$ chmod 755 ifnested.sh
$ ./ifnested.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 13-22-30.png>)

# looking for a possible value using elif
```
cat elifcheck.sh 
```
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
```
$ chmod 755 elifcheck.sh
$ ./elifcheck.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 13-25-24.png>)

# testing compound comparisons
```
cat> ifcompound.sh 
```
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 13-27-10.png>)

# using the case command
```
cat >casecheck.sh 
```
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
```
$ chmod 755 casecheck.sh 
$ ./casecheck.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-02-11.png>)
```
cat > whiletest
```
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
```
$ chmod 755 whiletest.sh
$ ./whiletest.sh
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-05-46.png>)
```
cat > untiltest.sh 
```
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
```
$ chmod 755 untiltest.sh
$ ./untiltest.sh
```
![com](<outputs/Screenshot from 2024-09-08 14-08-26.png>)
```
cat > forin1.sh 
```
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
```
$ chmod 755 forin1.sh
$ ./forin1.sh
```
![com](<outputs/Screenshot from 2024-09-08 14-11-19.png>)
```
cat > forin2.sh 
```
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
```
$ chmod 755 forin2.sh
$ ./forin2.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-16-36.png>)
```
cat > forin3.sh 
```
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
```
$ ./forin3.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-18-14.png>)
```
cat > forin1.sh 
```
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
```
$ chmod 755 forin1.sh
$ ./forin1.sh
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-20-37.png>)
```
cat > forinfile.sh 
```
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file"
done
```
```
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```
```
$ chmod 777 forinfile.sh
$ ./forinfile.sh
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-29-12.png>)
```
cat > forctype.sh 
```
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```
```
$ chmod 755 forctype.sh
$ ./forctype.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-33-01.png>)
```
cat > forctype1.sh 
```
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-42-01.png>)
```
cat > fornested1.sh 
```
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
```
$ chmod 755 fornested1.sh
$ ./fornested1.sh 
```
 ## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-44-55.png>)
```
cat > forbreak.sh 
```
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
echo "The for loop is completed"
```
```
$ chmod 755 forbreak.sh
$ ./forbreak.sh
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-53-05.png>)
```
cat > forcontinue.sh 
```
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
```
$ chmod 755 forcontinue.sh
$ ./forcontinue.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 14-59-12.png>)
```
cat > exread.sh 
```
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
```
```
$ chmod 755 exread.sh 
$ ./exread.sh 
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 15-04-30.png>)
```
cat > exread1.sh
```
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. "
``` 
```
$ chmod 755 exread1.sh 
$ ./exread1.sh
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 15-08-28.png>)

```
cat > funcex.sh
```
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
```
./funcex.sh 
./funcex.sh 1 2
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 15-13-59.png>)

``` 
cat > argshift.sh
```
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 15-15-31.png>)

```
cat > argshift1.sh
```
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
```
$ chmod 777 argshift1.sh
$ ./argshift1.sh 1 2 3
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 15-18-06.png>)
```
cat > argshift.sh
```
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
```
chmod 777 argshift.sh
./argshift.sh 1 2 3
```
## OUTPUT
![com](<outputs/Screenshot from 2024-09-08 15-22-33.png>)
```
cat > nc.awk
```
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
```
cat>data.dat
```
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
```
awk -f nc.awk data.dat
```
## OUTPUT 
![com](<outputs/Screenshot from 2024-09-08 15-25-30.png>)

```
cat > palindrome.sh
```
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
```
bash palindrome.sh
```
## OUTPUT 
![com](<outputs/Screenshot from 2024-09-08 15-28-57.png>)

# RESULT:
The Commands are executed successfully.
