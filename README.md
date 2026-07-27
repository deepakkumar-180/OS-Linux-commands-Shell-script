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
<img width="627" height="762" alt="exp1-1" src="https://github.com/user-attachments/assets/564eed62-24e5-4668-a6b4-9c5bbe6d7272" />



cat < file2
## OUTPUT
<img width="627" height="762" alt="exp1-1" src="https://github.com/user-attachments/assets/564eed62-24e5-4668-a6b4-9c5bbe6d7272" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="505" height="185" alt="exp1-2" src="https://github.com/user-attachments/assets/8dbe6195-c86c-4c6f-af01-57c8e9e8c045" />

 

comm file1 file2

 ## OUTPUT
<img width="465" height="526" alt="exp1-comm" src="https://github.com/user-attachments/assets/cf07647c-3f28-4680-b32a-c8542ab7d722" />

 
diff file1 file2
## OUTPUT
<img width="442" height="411" alt="exp1-diff" src="https://github.com/user-attachments/assets/0ab20b93-0e65-4ce9-b4b9-8bcd72b0b1f6" />


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
<img width="407" height="127" alt="exp1-cut" src="https://github.com/user-attachments/assets/a29aad19-3972-41bf-ac7f-04b3b71dcf56" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="370" height="117" alt="exp1-cut(1)" src="https://github.com/user-attachments/assets/ec3cfcaf-19f0-4296-8c3c-679731d2f91c" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="452" height="132" alt="exp1-cut(2)" src="https://github.com/user-attachments/assets/b2b01562-8ca1-4f8c-8fce-93e2b6e9cb80" />


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

<img width="372" height="125" alt="exp1-grep" src="https://github.com/user-attachments/assets/0c15dbd5-bdfc-45bb-bf3f-f7665cc8427b" />


grep hello newfile 
## OUTPUT

<img width="372" height="150" alt="exp1-grep(1)" src="https://github.com/user-attachments/assets/e4b2d467-245f-451b-9745-51a837cdbc29" />



grep -v hello newfile 
## OUTPUT

<img width="367" height="86" alt="exp1-grep(2)" src="https://github.com/user-attachments/assets/0192f5fa-0712-4581-aeab-d8abca602238" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="362" height="97" alt="exp1-grep(3)" src="https://github.com/user-attachments/assets/8e64123b-5ff0-4fc6-8401-dd48d0869952" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="457" height="76" alt="exp1-grep(4)" src="https://github.com/user-attachments/assets/1427356a-8874-436f-baf6-9cd8c045c0b7" />


grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

<img width="445" height="102" alt="exp1-grep(6)" src="https://github.com/user-attachments/assets/61e5d801-1f98-4db6-af50-1a13e5f11cb3" />

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

<img width="452" height="102" alt="exp1-egrep" src="https://github.com/user-attachments/assets/0640097e-3622-4d9d-bac7-25ff13c5afab" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="535" height="107" alt="exp1-egrep(1)" src="https://github.com/user-attachments/assets/69d324c6-be8c-4e4a-a753-3afadff5ad05" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="497" height="101" alt="exp1-egrep(2)" src="https://github.com/user-attachments/assets/ef4fb8db-6504-4d5d-9078-7712c870980e" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="496" height="80" alt="exp1-egrep(3)" src="https://github.com/user-attachments/assets/a7e79b4a-ab24-4eed-80b1-c26636166d98" />


egrep '(world$)' newfile 
## OUTPUT

<img width="467" height="102" alt="exp1-egrep(4)" src="https://github.com/user-attachments/assets/ae11c933-51ea-4c6e-b54c-39c10121fcc4" />


egrep '(World$)' newfile 
## OUTPUT
<img width="416" height="101" alt="exp1-egrep(5)" src="https://github.com/user-attachments/assets/4dda3925-a625-4aab-a9ee-4af591383e37" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="561" height="120" alt="exp1-egrep(6)" src="https://github.com/user-attachments/assets/4dde206b-23da-45bb-8fd1-a9c694649f04" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="492" height="77" alt="exp1-egrep(7)" src="https://github.com/user-attachments/assets/b3d9138d-fbb9-41ee-959b-36aa32802881" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="487" height="82" alt="exp1-egrep(8(2))" src="https://github.com/user-attachments/assets/3c9c8c7e-f1fe-45ad-bfbd-addfd09682a9" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="442" height="80" alt="exp1-egrep(8)" src="https://github.com/user-attachments/assets/a57e6dab-1033-45ca-9a06-25820209187f" />


egrep l{2} newfile
## OUTPUT

<img width="407" height="107" alt="exp1-egrep(9)" src="https://github.com/user-attachments/assets/c1eecca9-f935-4a96-a327-1d7113660ab1" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="476" height="160" alt="exp1-egrep(10)" src="https://github.com/user-attachments/assets/a0e18812-3aa5-4f19-ad74-75fb6ef7bb4b" />

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

<img width="412" height="77" alt="exp1-sed" src="https://github.com/user-attachments/assets/b9d8bf23-4ba3-4929-b80a-5a56a71b879c" />


sed -n -e '$p' file23
## OUTPUT

<img width="387" height="85" alt="exp1-sed(1)" src="https://github.com/user-attachments/assets/f18936bc-88f3-4136-8f94-41b9bfd286da" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="411" height="257" alt="exp1-sed(2)" src="https://github.com/user-attachments/assets/c0cabdde-da59-4079-bc7f-febc87341636" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="456" height="252" alt="exp1-sed(3)" src="https://github.com/user-attachments/assets/d8ff36d1-6539-4abb-8561-b2b14787dc2e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="492" height="245" alt="exp1-sed(4)" src="https://github.com/user-attachments/assets/377865cd-e8de-4596-94ee-1d8b84bda4f8" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="422" height="185" alt="exp1-sed(5)" src="https://github.com/user-attachments/assets/17b4022b-e569-4998-891d-0259df374f81" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="426" height="122" alt="exp1-sed(6)" src="https://github.com/user-attachments/assets/82fe5c95-e53e-4272-bb9b-7ff76b994126" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="497" height="102" alt="exp1-sed(7)" src="https://github.com/user-attachments/assets/13404c96-c48c-4fa6-a402-d6cf4d401eea" />


seq 10 
## OUTPUT

<img width="600" height="307" alt="exp1-seq" src="https://github.com/user-attachments/assets/29c58d45-20bf-41f1-b728-d0d079967de2" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="472" height="130" alt="exp1-seq(1)" src="https://github.com/user-attachments/assets/8fef83fd-397f-4950-8b4b-6f5b3f4f6008" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="531" height="132" alt="exp1-seq(2)" src="https://github.com/user-attachments/assets/abb9440d-33d2-4792-9c78-51db6ea42d77" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="482" height="132" alt="exp1-seq(3)" src="https://github.com/user-attachments/assets/b8e5f460-4637-4d26-95d2-2ea75353cd42" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="482" height="132" alt="exp1-seq(4)" src="https://github.com/user-attachments/assets/5248044c-1d30-442a-984b-2e309319de20" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="440" height="125" alt="exp1-seq(5)" src="https://github.com/user-attachments/assets/712575f1-77fb-4de7-a38b-4c1662e1c9a9" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="510" height="127" alt="exp1-seq(6)" src="https://github.com/user-attachments/assets/82421616-53f5-494b-b13f-6eaa790ff1ba" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="472" height="122" alt="exp1-seq(7)" src="https://github.com/user-attachments/assets/0114ca24-a76b-4b6a-af4e-924fbfd70ffa" />


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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



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
