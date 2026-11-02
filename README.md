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
<img width="320" height="67" alt="image" src="https://github.com/user-attachments/assets/af4c399d-6f79-4921-b632-fca55b7e6235" />


cat < file2
## OUTPUT
<img width="366" height="73" alt="image" src="https://github.com/user-attachments/assets/1d9210af-70b5-4c5b-8fb6-74a1f4db32cb" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="465" height="27" alt="image" src="https://github.com/user-attachments/assets/cb1eddd0-d347-413d-86db-c98de257c0b1" />

comm file1 file2
 ## OUTPUT
<img width="360" height="107" alt="image" src="https://github.com/user-attachments/assets/4453dbb9-a65b-47fd-b7d3-3aa1c48e617c" />
 
diff file1 file2
## OUTPUT
<img width="371" height="195" alt="image" src="https://github.com/user-attachments/assets/020ad5c7-97db-41c3-a9f3-bfa917174cc1" />


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

<img width="393" height="45" alt="image" src="https://github.com/user-attachments/assets/56a855b6-fdaf-4ae5-bfe1-cb8552dea439" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="513" height="62" alt="image" src="https://github.com/user-attachments/assets/4bf8f4be-3082-47c4-9bbd-8b989b690572" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="457" height="61" alt="image" src="https://github.com/user-attachments/assets/a4ea1520-73ee-421a-9fb3-1d13a1c980be" />


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

<img width="437" height="36" alt="image" src="https://github.com/user-attachments/assets/2e6525b2-d38d-4529-915f-75fc2d79aa29" />


grep hello newfile 
## OUTPUT

<img width="516" height="35" alt="image" src="https://github.com/user-attachments/assets/f2c41b59-2860-4b71-97eb-0726bc9d77be" />


grep -v hello newfile 
## OUTPUT

<img width="485" height="38" alt="image" src="https://github.com/user-attachments/assets/6f398291-8c8d-4d89-bf0d-f2813d66fe98" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="570" height="52" alt="image" src="https://github.com/user-attachments/assets/efa17f56-8150-4b96-83b2-a66a4bf371d5" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="548" height="32" alt="image" src="https://github.com/user-attachments/assets/a9c9d1a8-5ad1-4e41-9dbf-3dc1e0be3419" />



grep -R ubuntu /etc
## OUTPUT

<img width="1412" height="693" alt="image" src="https://github.com/user-attachments/assets/4ced6482-87b0-44ad-bcac-3dab4dcbee80" />


grep -w -n world newfile   
## OUTPUT
<img width="475" height="51" alt="image" src="https://github.com/user-attachments/assets/a02d8997-c2b6-4a7e-8880-70853d050784" />


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

<img width="385" height="40" alt="image" src="https://github.com/user-attachments/assets/a384af59-ba97-4134-b0cb-24a5ebcb3138" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="370" height="42" alt="image" src="https://github.com/user-attachments/assets/4c2c3718-fa85-4f53-ab61-ba8c4d93b1c5" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="417" height="41" alt="image" src="https://github.com/user-attachments/assets/050f7341-0e25-4cb7-9426-73f8c89162cd" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="381" height="30" alt="image" src="https://github.com/user-attachments/assets/1287e1d7-0b98-4cf7-a3ef-8ff59f595a44" />


egrep '(world$)' newfile 
## OUTPUT

<img width="365" height="45" alt="image" src="https://github.com/user-attachments/assets/dca22d6b-f2c1-4ba2-9958-0218bb2f2272" />


egrep '(World$)' newfile 
## OUTPUT

<img width="376" height="30" alt="image" src="https://github.com/user-attachments/assets/f9492fa8-7375-41ca-bf8d-323754e02770" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="397" height="53" alt="image" src="https://github.com/user-attachments/assets/14e3392a-beb9-44ce-bd79-1cb6d77ab861" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="415" height="30" alt="image" src="https://github.com/user-attachments/assets/8b6407c5-6d47-4339-9706-b6521d64e6f7" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="401" height="27" alt="image" src="https://github.com/user-attachments/assets/4fb30b53-f3cb-4e86-b67c-38262d109875" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="390" height="28" alt="image" src="https://github.com/user-attachments/assets/c9a6a021-df15-462f-91b4-99927502c8a1" />


egrep l{2} newfile
## OUTPUT

<img width="376" height="42" alt="image" src="https://github.com/user-attachments/assets/09cf95a2-dde9-4182-9718-b66389a98171" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="402" height="56" alt="image" src="https://github.com/user-attachments/assets/881ad197-32b8-4db1-a014-a0ede582c3f6" />


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

<img width="372" height="27" alt="image" src="https://github.com/user-attachments/assets/87dbf8e7-0e78-42fa-85c6-4058cceeeb62" />


sed -n -e '$p' file23
## OUTPUT

<img width="350" height="28" alt="image" src="https://github.com/user-attachments/assets/6eb9b0c7-9e4f-402d-b5c9-e73bf0a77f9b" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="355" height="125" alt="image" src="https://github.com/user-attachments/assets/112e8b33-8bd9-4829-b0c6-ad311a98ba5c" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="400" height="126" alt="image" src="https://github.com/user-attachments/assets/daf0288c-84f9-4526-a115-4491aee25c9b" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="445" height="130" alt="image" src="https://github.com/user-attachments/assets/02e9a47e-e7a1-4f3f-9f7e-2812c7698c14" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="400" height="87" alt="image" src="https://github.com/user-attachments/assets/79ec63ee-1586-469c-a936-b4a976878ada" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="407" height="60" alt="image" src="https://github.com/user-attachments/assets/11b4aca0-8355-4191-b501-150d0d4cac57" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="418" height="45" alt="image" src="https://github.com/user-attachments/assets/56e7e2a0-5c85-447f-af52-66f0fc892387" />


seq 10 
## OUTPUT

<img width="362" height="157" alt="image" src="https://github.com/user-attachments/assets/c05d93b5-9487-44e1-8d97-5f2a4247a19e" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="421" height="57" alt="image" src="https://github.com/user-attachments/assets/0337d96c-8fbe-42c9-a8cc-952296df85f2" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="337" height="57" alt="image" src="https://github.com/user-attachments/assets/b383b917-aea6-493b-b39b-8d0d06fd7d55" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="325" height="72" alt="image" src="https://github.com/user-attachments/assets/bb65f42b-c0cb-4607-8be6-543fe3e6265d" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="361" height="55" alt="image" src="https://github.com/user-attachments/assets/5b52f813-f1ae-43ce-9fd2-86a47c425d22" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="378" height="60" alt="image" src="https://github.com/user-attachments/assets/0e0d9582-f5dd-402f-9e81-277aa78886ca" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="410" height="57" alt="image" src="https://github.com/user-attachments/assets/a3f9b63d-b62b-4dec-8cae-e53e56df3507" />


sed -n '2,4{s/$/*/;p}' file23

<img width="445" height="58" alt="image" src="https://github.com/user-attachments/assets/7262956b-08e8-4b05-bf26-92d3a4c90c7c" />


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

<img width="402" height="90" alt="image" src="https://github.com/user-attachments/assets/a7ad7e3b-f799-489f-a474-4b87eb2f483b" />


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

<img width="387" height="92" alt="image" src="https://github.com/user-attachments/assets/7d483f74-8d47-4af0-889d-75d4be20a64f" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="593" height="141" alt="image" src="https://github.com/user-attachments/assets/eee65393-7e81-438e-958d-122062c4668f" />

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

<img width="522" height="65" alt="image" src="https://github.com/user-attachments/assets/cff05008-6259-4177-b107-f3a57a62bbb5" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="606" height="60" alt="image" src="https://github.com/user-attachments/assets/cc8293fd-0784-4f2b-9526-887ecf988bb5" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="482" height="137" alt="image" src="https://github.com/user-attachments/assets/cd97b1af-3ee5-425c-a8fb-2d300e155853" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="533" height="502" alt="image" src="https://github.com/user-attachments/assets/f27a3576-fc00-4b26-a4ec-a70030d8b09a" />


tar -xvf backup.tar
## OUTPUT

<img width="585" height="155" alt="image" src="https://github.com/user-attachments/assets/5367c7b6-a02d-4ba5-999b-10eeab36869d" />


gzip backup.tar
ls .gz
## OUTPUT

<img width="382" height="27" alt="image" src="https://github.com/user-attachments/assets/43a5e8a0-d7a2-4c73-a4c2-a2809b25dc7f" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="492" height="133" alt="image" src="https://github.com/user-attachments/assets/7b01995c-b18f-4122-9c89-7ccfc29d5207" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="770" height="55" alt="image" src="https://github.com/user-attachments/assets/f6535d94-184c-4dfe-b410-1fc244a1be5e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="455" height="117" alt="image" src="https://github.com/user-attachments/assets/dbfb6f6b-8b9e-4f36-abc5-b52233f590dc" />


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

<img width="385" height="163" alt="image" src="https://github.com/user-attachments/assets/bcf644fd-11a5-4b99-9eb8-928dc37ee672" />


 
ls file1
## OUTPUT

<img width="250" height="30" alt="image" src="https://github.com/user-attachments/assets/4a354d48-8201-447d-955a-ae5e80eaf923" />



echo $?
## OUTPUT

<img width="263" height="26" alt="image" src="https://github.com/user-attachments/assets/ceec2f5e-7c72-4a8a-ba6d-2f206490b0c2" />



./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="268" height="28" alt="image" src="https://github.com/user-attachments/assets/1f4a6b89-aba0-4ebe-a721-b7c853b0dd49" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="286" height="25" alt="image" src="https://github.com/user-attachments/assets/adaa2ebc-8fa8-4ae1-be96-8919b470ccee" />

 
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

<img width="527" height="247" alt="image" src="https://github.com/user-attachments/assets/1f418212-d860-43be-80e0-510ceb6eb991" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="447" height="56" alt="image" src="https://github.com/user-attachments/assets/391c7ed2-d369-41b7-a374-0c7ec7dc7bb2" />


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

<img width="547" height="192" alt="image" src="https://github.com/user-attachments/assets/6ca42947-3521-45f9-95be-4c2b006297a1" />


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

<img width="508" height="372" alt="image" src="https://github.com/user-attachments/assets/a7d80a47-6aa5-4fad-bead-5b066ca322a6" />


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

<img width="535" height="320" alt="image" src="https://github.com/user-attachments/assets/32208743-ee3d-49e7-b26a-cacb1b526f46" />


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

<img width="438" height="67" alt="image" src="https://github.com/user-attachments/assets/13865596-e717-42df-9338-7c558ded11a3" />


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

<img width="560" height="361" alt="image" src="https://github.com/user-attachments/assets/39f82f05-5e46-45f9-8ee0-739a6eda6817" />


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

<img width="570" height="195" alt="image" src="https://github.com/user-attachments/assets/f38802de-fb49-45a7-affb-2a46bea16ef3" />


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

<img width="502" height="420" alt="image" src="https://github.com/user-attachments/assets/1fb5f0b6-68a9-4e46-93ad-187658484998" />



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

<img width="497" height="227" alt="image" src="https://github.com/user-attachments/assets/5690e0f2-9f22-4cd0-ad17-40359c4f4feb" />


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

<img width="457" height="225" alt="image" src="https://github.com/user-attachments/assets/e2ef1573-def5-46b0-9981-b9fad98cdf3f" />


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

<img width="495" height="388" alt="image" src="https://github.com/user-attachments/assets/b6d6397c-1f99-4a73-883d-2fcea86ec1a3" />

 
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
 
<img width="528" height="278" alt="image" src="https://github.com/user-attachments/assets/101dc31f-6033-42ae-a9be-cec73b7eabfa" />


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

<img width="467" height="298" alt="image" src="https://github.com/user-attachments/assets/f37bf537-72a1-4a61-b50e-09da93b0ed5c" />

 
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

<img width="461" height="167" alt="image" src="https://github.com/user-attachments/assets/421e2c09-bea0-4007-9643-06bd5590a816" />


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

<img width="490" height="150" alt="image" src="https://github.com/user-attachments/assets/82c40af0-7731-4637-8bd7-be99372da668" />


 
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

<img width="453" height="297" alt="image" src="https://github.com/user-attachments/assets/ddaff681-ee42-4678-8d99-e3d23cd5c9ba" />

 
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

<img width="437" height="200" alt="image" src="https://github.com/user-attachments/assets/4f7042c6-2b14-4ea1-a341-f0e143b6249e" />
 
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


<img width="530" height="238" alt="image" src="https://github.com/user-attachments/assets/fcda31b8-2582-4139-ae4a-25a64078def5" />

 
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

 <img width="545" height="422" alt="image" src="https://github.com/user-attachments/assets/435278d2-da5f-4ef0-bc49-15c0468a5414" />

 
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

<img width="260" height="207" alt="image" src="https://github.com/user-attachments/assets/ce7bb1ad-039f-4bd0-9d20-b5eb495922da" />

 
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

<img width="521" height="466" alt="image" src="https://github.com/user-attachments/assets/2493705b-fe62-41c5-9a8b-cfbbd3b5560d" />


# RESULT:
The Commands are executed successfully.
