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
<img width="420" height="116" alt="image" src="https://github.com/user-attachments/assets/7b9151a5-9ba4-4eb4-a6ce-ee56deeb7a69" />



cat < file2
## OUTPUT
<img width="452" height="183" alt="image" src="https://github.com/user-attachments/assets/3257d706-fbe7-4dbd-aa58-5b5c598906cd" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="513" height="60" alt="image" src="https://github.com/user-attachments/assets/9b754b2a-b5a2-4596-8203-8fd4f68ea0f3" />
 
comm file1 file2
 ## OUTPUT
<img width="496" height="281" alt="image" src="https://github.com/user-attachments/assets/ff96f8da-bea6-4b6d-a641-36775446f3ef" />

 
diff file1 file2
## OUTPUT
<img width="572" height="355" alt="image" src="https://github.com/user-attachments/assets/9f92b7a0-7fde-4e0e-8872-c63cc95d45e9" />


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
<img width="463" height="112" alt="image" src="https://github.com/user-attachments/assets/7e5477f5-d41d-449c-9cd7-bb0ba7d85170" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="525" height="137" alt="image" src="https://github.com/user-attachments/assets/b776568d-d625-4bdf-9670-4e00f37aa228" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="521" height="132" alt="image" src="https://github.com/user-attachments/assets/471c1800-25b3-434f-9c24-300ae4004e55" />


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
<img width="522" height="70" alt="image" src="https://github.com/user-attachments/assets/1cd86e12-4a42-4160-b1f4-ac0041c932b8" />



grep hello newfile 
## OUTPUT
<img width="517" height="71" alt="image" src="https://github.com/user-attachments/assets/a4af7aa1-7cee-49bd-8f5f-3f07ac38912c" />




grep -v hello newfile 
## OUTPUT
<img width="530" height="82" alt="image" src="https://github.com/user-attachments/assets/a585caa0-069b-4c45-adb7-679787293432" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="667" height="98" alt="image" src="https://github.com/user-attachments/assets/75039795-dea8-4bc3-9bb8-e10891dcde67" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="687" height="68" alt="image" src="https://github.com/user-attachments/assets/aaa72c39-1ea8-4e18-b9f6-41b349a6605a" />




grep -R ubuntu /etc
## OUTPUT
<img width="777" height="245" alt="image" src="https://github.com/user-attachments/assets/b13b1365-8f04-4822-95bd-fde36e41eca0" />



grep -w -n world newfile   
## OUTPUT
<img width="697" height="91" alt="image" src="https://github.com/user-attachments/assets/7140deb3-2a37-4c1c-b6b1-e5989ff0b436" />


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
<img width="750" height="97" alt="image" src="https://github.com/user-attachments/assets/9f13b8bf-482a-4911-93bf-b10c3fd028c6" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="722" height="97" alt="image" src="https://github.com/user-attachments/assets/fe21074f-fa54-43c6-bcac-8154bdf03cd1" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="741" height="100" alt="image" src="https://github.com/user-attachments/assets/f330b551-cae4-4ffe-b3eb-1183ef64527f" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="705" height="80" alt="image" src="https://github.com/user-attachments/assets/9a79c306-a0db-4f68-85c1-55750b6610f1" />



egrep '(world$)' newfile 
## OUTPUT
<img width="658" height="73" alt="image" src="https://github.com/user-attachments/assets/488cd677-6375-4601-894a-ce549c1e82c5" />



egrep '(World$)' newfile 
## OUTPUT
<img width="833" height="72" alt="image" src="https://github.com/user-attachments/assets/1b72b651-c844-483b-98ef-370540d021b0" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="673" height="93" alt="image" src="https://github.com/user-attachments/assets/9f325aa1-2dec-4730-b38f-75f907ee9bfa" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="707" height="71" alt="image" src="https://github.com/user-attachments/assets/da6a3651-4ebd-447e-8ad5-5080b532cced" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="725" height="75" alt="image" src="https://github.com/user-attachments/assets/8f2b13c8-2a35-4b0f-92da-5b9a6a7f058b" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="667" height="65" alt="image" src="https://github.com/user-attachments/assets/4ce97986-2ba6-4cc6-9399-76de8d14fa0b" />


egrep l{2} newfile
## OUTPUT
<img width="775" height="100" alt="image" src="https://github.com/user-attachments/assets/5ea22950-46aa-4e5f-9b04-a4aaacbdb9fe" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="766" height="129" alt="image" src="https://github.com/user-attachments/assets/6c76b47c-82ce-4943-8ddd-c90163004072" />


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
<img width="536" height="61" alt="image" src="https://github.com/user-attachments/assets/390a977b-b2e8-4c6a-9e4a-8fb85592767a" />



sed -n -e '$p' file23
## OUTPUT
<img width="552" height="62" alt="image" src="https://github.com/user-attachments/assets/649bc1b5-7136-457c-a3f3-5f7655808fd0" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="592" height="270" alt="image" src="https://github.com/user-attachments/assets/f5af7909-0f27-448b-b31b-92d06a3caab4" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="603" height="281" alt="image" src="https://github.com/user-attachments/assets/924530d4-dc37-4138-84f0-899b7ebd4c6d" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="667" height="287" alt="image" src="https://github.com/user-attachments/assets/f6c494a5-32d7-4da9-906d-38ac2946b7e6" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="667" height="190" alt="image" src="https://github.com/user-attachments/assets/cc857af3-d4cc-47d3-9166-1e88bb83b0f1" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="612" height="128" alt="image" src="https://github.com/user-attachments/assets/f830cb9f-e8fc-442f-bde8-30bf971e4320" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="661" height="93" alt="image" src="https://github.com/user-attachments/assets/f9ed6af0-7319-48d3-a8f0-7cef305febe6" />



seq 10 
## OUTPUT
<img width="666" height="338" alt="image" src="https://github.com/user-attachments/assets/60e46bb8-8637-4b31-970f-75562f1419a3" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="655" height="132" alt="image" src="https://github.com/user-attachments/assets/72842a06-46a7-4502-a969-f5940b8de166" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="602" height="122" alt="image" src="https://github.com/user-attachments/assets/d171c3c4-a3cf-4649-a539-302fa998b627" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="661" height="123" alt="image" src="https://github.com/user-attachments/assets/405e28d3-805d-4222-9045-3202fdbd02f0" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="617" height="147" alt="image" src="https://github.com/user-attachments/assets/8b360795-6614-4dc9-9e8f-3dfeb17358ba" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="601" height="126" alt="image" src="https://github.com/user-attachments/assets/dd565ab6-28cc-40c6-acaf-08639a3cc260" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="652" height="117" alt="image" src="https://github.com/user-attachments/assets/1688a7fc-86f8-48db-b5ea-ac81590842ab" />



sed -n '2,4{s/$/*/;p}' file23
<img width="666" height="123" alt="image" src="https://github.com/user-attachments/assets/df62bb33-9b45-4771-9bc9-ceae0669308e" />


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
<img width="422" height="196" alt="image" src="https://github.com/user-attachments/assets/8aeea1fb-df68-4797-9463-b34ad9b788da" />


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
<img width="447" height="178" alt="image" src="https://github.com/user-attachments/assets/a4a80cd3-0e94-44bd-aa25-e14624b4799b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="757" height="268" alt="image" src="https://github.com/user-attachments/assets/3bf5b3c3-252c-4d11-8a48-90535e8457a4" />

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
<img width="791" height="127" alt="image" src="https://github.com/user-attachments/assets/3239b166-c08c-47b9-bd09-2651041b6982" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="787" height="133" alt="image" src="https://github.com/user-attachments/assets/2ce6a60b-5ccf-45b2-be84-0a67bd808df5" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="412" height="101" alt="image" src="https://github.com/user-attachments/assets/90aedabf-8e01-4f85-8c6a-0153ddbeca3f" />


tar -xvf backup.tar
## OUTPUT
<img width="418" height="102" alt="image" src="https://github.com/user-attachments/assets/7ad714ad-82ff-4333-8cde-beb6e3fb925b" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="792" height="161" alt="image" src="https://github.com/user-attachments/assets/ec6c883f-32ea-4e6e-b534-43baffc10d7b" />

gunzip backup.tar.gz
## OUTPUT
<img width="787" height="221" alt="image" src="https://github.com/user-attachments/assets/5af82efe-3f55-4112-80b8-01d802ad619d" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="782" height="325" alt="image" src="https://github.com/user-attachments/assets/bfc0fc1e-dcb5-490c-8568-038fe60b1114" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="457" height="127" alt="image" src="https://github.com/user-attachments/assets/3236861a-f87e-4bd5-8df1-3afdc1507964" />


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
<img width="585" height="448" alt="image" src="https://github.com/user-attachments/assets/852800cc-0aca-4906-9e11-80a843c5b3d9" />

 
ls file1
## OUTPUT
<img width="357" height="71" alt="image" src="https://github.com/user-attachments/assets/1ce391f6-6e3e-4f28-aa9a-e6314a91bdd6" />

echo $?
## OUTPUT <img width="373" height="73" alt="image" src="https://github.com/user-attachments/assets/a26264e4-43e2-4009-9414-f9dc816ed0ba" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="342" height="83" alt="image" src="https://github.com/user-attachments/assets/30f1c17b-17f9-4f23-83f8-935ba2aaf8e9" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="660" height="302" alt="image" src="https://github.com/user-attachments/assets/04383063-a27f-4185-b866-78ea6b40d7a5" />


 
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
<img width="668" height="333" alt="image" src="https://github.com/user-attachments/assets/b5512ae2-1c44-443b-a7bb-4483a0d0ede7" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="785" height="330" alt="image" src="https://github.com/user-attachments/assets/45f8fb86-e2b4-4c4a-a9dc-34ee8667937b" />


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
<img width="857" height="220" alt="image" src="https://github.com/user-attachments/assets/8c91ba20-293f-42db-8134-aa3d2b1e3fca" />

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
<img width="713" height="568" alt="image" src="https://github.com/user-attachments/assets/96f73011-1af6-4ef5-b86b-37f1ccf89b41" />



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
<img width="712" height="657" alt="image" src="https://github.com/user-attachments/assets/51a0e6d1-8f4b-449f-803d-9abe9b6f7fd8" />

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
<img width="772" height="668" alt="image" src="https://github.com/user-attachments/assets/9d7125e7-95e6-4454-ac59-3b59c096d3ab" />

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
<img width="760" height="652" alt="image" src="https://github.com/user-attachments/assets/b5f6f8b5-0e29-492b-8d21-993736652f2b" />


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
<img width="698" height="352" alt="image" src="https://github.com/user-attachments/assets/02b3eec3-c556-472c-8c2b-29915a2ac62b" />

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

## OUTPUT <img width="642" height="217" alt="image" src="https://github.com/user-attachments/assets/a66e0e76-8ad7-423b-ab28-5f8e471a65ca" />

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
<img width="552" height="278" alt="image" src="https://github.com/user-attachments/assets/00f86036-c0ff-467f-8b9a-e3996677a887" />


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
<img width="526" height="283" alt="image" src="https://github.com/user-attachments/assets/e29ea580-97a8-4c36-b60b-5fa32942910a" />

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
<img width="787" height="300" alt="image" src="https://github.com/user-attachments/assets/13578d4e-d220-4e7e-a20c-272670978d30" />

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
<img width="791" height="296" alt="image" src="https://github.com/user-attachments/assets/24c9ab99-6712-435b-9ab9-45a11dabeb6b" />

 
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
<img width="792" height="300" alt="image" src="https://github.com/user-attachments/assets/68b124fd-1eac-42de-91d1-15e54a1652eb" />

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
<img width="735" height="306" alt="image" src="https://github.com/user-attachments/assets/35f559fd-9729-4be4-ba10-0bfdb75a5bbc" />
 
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
<img width="616" height="188" alt="image" src="https://github.com/user-attachments/assets/a610544b-70fe-4d6e-a06a-7a38ea9e7fb4" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="772" height="137" alt="image" src="https://github.com/user-attachments/assets/a3224284-080b-4dc3-a4b5-32c186aed6b6" />



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
<img width="786" height="32" alt="image" src="https://github.com/user-attachments/assets/e16699b8-cf32-4b5b-bf58-5c9cfbc6851f" />

 
 ./funcex.sh 1 2
<img width="676" height="32" alt="image" src="https://github.com/user-attachments/assets/c144f80d-d78a-4244-a31b-42074fc2b710" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT <img width="522" height="65" alt="image" src="https://github.com/user-attachments/assets/a551cf73-fad2-4727-b2f4-7c67aa978fdf" />

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
## OUTPUT <img width="638" height="77" alt="image" src="https://github.com/user-attachments/assets/d37c3d2b-9218-4c6f-96b3-a4f0c12fdc58" />

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
## OUTPUT <img width="677" height="376" alt="image" src="https://github.com/user-attachments/assets/3d088aa1-d305-4aab-b425-43a682ee0ab5" />

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
 <img width="482" height="251" alt="image" src="https://github.com/user-attachments/assets/c3cacf22-0ee9-4b14-90bb-a89a389ea9b7" />

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
<img width="630" height="78" alt="image" src="https://github.com/user-attachments/assets/47b188e8-acf9-4b68-8aa1-710f3623f637" />


# RESULT:
The Commands are executed successfully.
