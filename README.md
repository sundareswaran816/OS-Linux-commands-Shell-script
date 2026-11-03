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

<img width="2170" height="725" alt="image1" src="./images/image1.png" />


cat < file2
## OUTPUT

<img width="2171" height="724" alt="image2" src="./images/image2.png" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="2171" height="724" alt="image3" src="./images/image3.png" />
comm file1 file2
 ## OUTPUT

<img width="2172" height="724" alt="image4" src="./images/image4.png" />


 
diff file1 file2
## OUTPUT
<img width="1537" height="1023" alt="image5" src="./images/image5.png" />
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


<img width="1859" height="846" alt="image6" src="./images/image6.png" />

cut -d "|" -f 1 file22
## OUTPUT


<img width="1859" height="846" alt="image7" src="./images/image7.png" />
cut -d "|" -f 2 file22
## OUTPUT
<img width="2170" height="725" alt="image8" src="./images/image8.png" />


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
<img width="1724" height="912" alt="image9" src="./images/image9.png" />




grep hello newfile 
## OUTPUT


<img width="1827" height="861" alt="image10" src="./images/image10.png" />



grep -v hello newfile 
## OUTPUT
<img width="1863" height="844" alt="image11" src="./images/image11.png" />

cat newfile | grep -i "hello"
## OUTPUT


<img width="1745" height="901" alt="image12" src="./images/image12.png" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1828" height="860" alt="image13" src="./images/image13.png" />


grep -R ubuntu /etc
## OUTPUT

<img width="1658" height="949" alt="image14" src="./images/image14.png" />


grep -w -n world newfile   
## OUTPUT

<img width="1692" height="930" alt="image15" src="./images/image15.png" />
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


<img width="1488" height="1057" alt="image16" src="./images/image16.png" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1559" height="1009" alt="image17" src="./images/image17.png" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1545" height="1018" alt="image18" src="./images/image18.png" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="1738" height="905" alt="image19" src="./images/image19.png" />
egrep '(world$)' newfile 
## OUTPUT

<img width="1617" height="973" alt="image20" src="./images/image20.png" />




egrep '(World$)' newfile 
## OUTPUT
<img width="1617" height="973" alt="image 26" src="./images/image21.png" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1519" height="1035" alt="image25" src="./images/image22.png" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1709" height="920" alt="image27" src="./images/image23.png" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1740" height="904" alt="image28" src="./images/image24.png" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1691" height="930" alt="image29" src="./images/image25.png" />


egrep l{2} newfile
## OUTPUT

<img width="1672" height="941" alt="image30" src="./images/image26.png" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1700" height="925" alt="image31" src="./images/image27.png" />

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
<img width="2188" height="718" alt="image32" src="./images/image28.png" />



sed -n -e '$p' file23
## OUTPUT

<img width="2172" height="724" alt="image33" src="./images/image29.png" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1899" height="828" alt="image34" src="./images/image30.png" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1997" height="787" alt="image35" src="./images/image31.png" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1959" height="803" alt="image36" src="./images/image32.png" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1615" height="974" alt="image37" src="./images/image33.png" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="1736" height="906" alt="image38" src="./images/image34.png" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1956" height="804" alt="image39" src="./images/image35.png" />



seq 10 
## OUTPUT

<img width="1407" height="1118" alt="image40" src="./images/image36.png" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1805" height="871" alt="image41" src="./images/image37.png" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1723" height="913" alt="image42" src="./images/image38.png" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="1554" height="1012" alt="image43" src="./images/image39.png" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="1606" height="979" alt="image44" src="./images/image40.png" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="1309" height="1201" alt="image45" src="./images/image41.png" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1960" height="802" alt="image46" src="./images/image42.png" />


sed -n '2,4{s/$/*/;p}' file23

<img width="1847" height="852" alt="image47" src="./images/image43.png" />

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

<img width="1220" height="390" alt="Screenshot 2026-08-01 200947" src="./images/image44.png" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1859" height="846" alt="image48" src="./images/image45.png" />

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

<img width="1961" height="802" alt="image49" src="./images/image46.png" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1797" height="875" alt="image50" src="./images/image47.png" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1860" height="845" alt="image51" src="./images/image48.png" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1812" height="868" alt="image52" src="./images/image49.png" />


tar -xvf backup.tar
## OUTPUT
<img width="1693" height="929" alt="image53" src="./images/image50.png" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1889" height="833" alt="image54" src="./images/image51.png" />

gunzip backup.tar.gz
## OUTPUT

 <img width="1719" height="915" alt="image55" src="./images/image52.png" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello Worldâ€˜; exit 0 >> my-script.sh
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

<img width="1852" height="849" alt="image56" src="./images/image53.png" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo â€œFile name is $0 â€
echo "File name is " `basename $0`
echo â€œFirst arg. is â€ $1
echo â€œSecond arg. is â€ $2
echo â€œThird arg. is â€ $3
echo â€œFourth arg. is â€ $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo â€œFile name is $0 â€
echo "File name is " `basename $0`
echo â€œFirst arg. is â€ $1
echo â€œSecond arg. is â€ $2
echo â€œThird arg. is â€ $3
echo â€œFourth arg. is â€ $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="902" height="464" alt="Screenshot 2026-08-01 210114" src="./images/image54.png" />

 
ls file1
## OUTPUT
<img width="2173" height="724" alt="image58" src="./images/image55.png" />

echo $?
## OUTPUT 
<img width="2168" height="725" alt="image59" src="./images/image56.png" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="2152" height="731" alt="image60" src="./images/image57.png" />

abcd
 
echo $?
 ## OUTPUT

<img width="2141" height="734" alt="image61" src="./images/image58.png" />

 
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


<img width="1815" height="866" alt="image62" src="./images/image59.png" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1923" height="818" alt="image63" src="./images/image60.png" />


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo â€œYou are the owner of the /etc/passwd fileâ€
else
echo â€œSorry, you are not the owner of the /etc/passwd fileâ€
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo â€œYou are the owner of the /etc/passwd fileâ€
else
echo â€œSorry, you are not the owner of the /etc/passwd fileâ€
fi
 ```
./psswdperm.sh
## OUTPUT
<img width="2014" height="781" alt="image64" src="./images/image61.png" />

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo â€œ$HOME The object exists, is it a file?â€
if [ -f $HOME ]
then
echo â€œYes,$HOME it is a file!â€
else
echo â€œNo,$HOME it is not a file!â€
if [ -f $HOME/.bash_history ]
then
echo â€œBut $HOME/.bash_history is a file!â€
fi
fi
else
echo â€œSorry, the object does not existâ€
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo â€œ$HOME The object exists, is it a file?â€
if [ -f $HOME ]
then
echo â€œYes,$HOME it is a file!â€
else
echo â€œNo,$HOME it is not a file!â€
if [ -f $HOME/.bash_history ]
then
echo â€œBut $HOME/.bash_history is a file!â€
fi
fi
else
echo â€œSorry, the object does not existâ€
fi
```

./ifnested.sh 
## OUTPUT
<img width="1823" height="863" alt="image65" src="./images/image62.png" />



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo â€œThe test value $val1 is greater than 5â€
fi
if [ $val1 -eq $val2 ]
then
echo â€œThe values are equalâ€
else
echo â€œThe values are differentâ€
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
echo â€œThe test value $val1 is greater than 5â€
fi
if [ $val1 -eq $val2 ]
then
echo â€œThe values are equalâ€
else
echo â€œThe values are differentâ€
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="1376" height="1143" alt="image66" src="./images/image63.png" />

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo â€œ$HOME The object exists, is it a file?â€
if [ -f $HOME ]
then
echo â€œYes,$HOME it is a file!â€
else
echo â€œNo,$HOME it is not a file!â€
if [ -f $HOME/.bash_history ]
then
echo â€œBut $HOME/.bash_history is a file!â€
fi
fi
else
echo â€œSorry, the object does not existâ€
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo â€œ$HOME The object exists, is it a file?â€
if [ -f $HOME ]
then
echo â€œYes,$HOME it is a file!â€
else
echo â€œNo,$HOME it is not a file!â€
if [ -f $HOME/.bash_history ]
then
echo â€œBut $HOME/.bash_history is a file!â€
fi
fi
else
echo â€œSorry, the object does not existâ€
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
<img width="821" height="261" alt="Screenshot 2026-08-01 214653" src="./images/image64.png" />

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

<img width="2164" height="726" alt="image67" src="./images/image65.png" />

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
<img width="1551" height="1014" alt="image68" src="./images/image66.png" />

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
echo â€œword:$testâ€
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo â€œword:$testâ€
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
<img width="2149" height="731" alt="image69" src="./images/image67.png" />

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $fileâ€œ
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

<img width="2135" height="736" alt="image70" src="./images/image68.png" />

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
<img width="2167" height="726" alt="image71" src="./images/image69.png" />

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
<img width="1900" height="828" alt="image72" src="./images/image70.png" />

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

 <img width="2159" height="728" alt="image73" src="./images/image71.png" />

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
echo "The for loop is completedâ€œ
```
## OUTPUT
<img width="1780" height="884" alt="image74" src="./images/image72.png" />

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
echo "The for loop is completedâ€œ
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="1857" height="847" alt="image75" src="./images/image73.png" />

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
<img width="921" height="331" alt="Screenshot 2026-08-01 221013" src="./images/image74.png" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. â€œ
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="921" height="331" alt="Screenshot 2026-08-01 221013" src="./images/image75.png" />


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
<img width="1877" height="838" alt="image76" src="./images/image76.png" />

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

<img width="2149" height="731" alt="image77" src="./images/image77.png" />

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
<img width="2105" height="747" alt="image78" src="./images/image78.png" />

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
 
 <img width="1850" height="850" alt="image79" src="./images/image79.png" />

 
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
 <img width="1844" height="853" alt="image80" src="./images/image80.png" />

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
<img width="2167" height="725" alt="image82" src="./images/image81.png" />


# RESULT:
The Commands are executed successfully.
