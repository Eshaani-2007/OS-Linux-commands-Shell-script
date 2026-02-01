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
<img width="427" height="125" alt="image" src="https://github.com/user-attachments/assets/34467181-7f49-4aeb-aa6a-88260855591b" />



cat < file2
## OUTPUT
<img width="453" height="187" alt="image" src="https://github.com/user-attachments/assets/fba95577-e9e8-4b16-92e2-164ddb17b591" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="533" height="57" alt="image" src="https://github.com/user-attachments/assets/bd36f297-59f6-4b3e-9ca1-0983071eff47" />
 
comm file1 file2
 ## OUTPUT
<img width="528" height="273" alt="image" src="https://github.com/user-attachments/assets/9d044b9e-441b-41e6-906e-cd5935c93df9" />

 
diff file1 file2
## OUTPUT
<img width="572" height="350" alt="image" src="https://github.com/user-attachments/assets/1561c02d-64da-433b-b1e3-0c50bfee2901" />


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
<img width="457" height="103" alt="image" src="https://github.com/user-attachments/assets/048476ea-08ed-4174-93ff-29e246590bee" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="517" height="133" alt="image" src="https://github.com/user-attachments/assets/e6d57780-a26f-4d8e-9c55-7598e0ca69ea" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="522" height="132" alt="image" src="https://github.com/user-attachments/assets/e4aa1e81-e857-43e3-a8fb-46ff61cd8fa3" />


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
<img width="522" height="70" alt="image" src="https://github.com/user-attachments/assets/3c2426f2-a840-4554-a19b-3d08d74ccd29" />



grep hello newfile 
## OUTPUT
<img width="602" height="60" alt="image" src="https://github.com/user-attachments/assets/8a6fe580-7ca7-4c08-b0d7-fb14f6be80e1" />




grep -v hello newfile 
## OUTPUT
<img width="531" height="83" alt="image" src="https://github.com/user-attachments/assets/d37bc111-c82d-4602-b81b-55d3e2d07136" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="705" height="95" alt="image" src="https://github.com/user-attachments/assets/b2daa8a8-f9b7-44fd-86fb-205dff7a934c" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="701" height="72" alt="image" src="https://github.com/user-attachments/assets/e5242050-385c-427f-9d95-1553e9b5ca2a" />




grep -R ubuntu /etc
## OUTPUT
<img width="776" height="242" alt="image" src="https://github.com/user-attachments/assets/db41810b-7464-4d28-8abf-0c8e559ac1bc" />



grep -w -n world newfile   
## OUTPUT
<img width="732" height="97" alt="image" src="https://github.com/user-attachments/assets/63bd6f4c-04ba-4d29-9c38-8d74077cbb12" />


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
<img width="765" height="87" alt="image" src="https://github.com/user-attachments/assets/e83205be-dddf-4204-bcb7-981ec6f24fa0" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="745" height="97" alt="image" src="https://github.com/user-attachments/assets/51b2a15d-b51e-43f6-8676-3f4c7ac5f8b9" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="746" height="100" alt="image" src="https://github.com/user-attachments/assets/9d115178-196a-424b-8cbc-1d7fe02f4d83" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="696" height="73" alt="image" src="https://github.com/user-attachments/assets/01ba3553-ff21-4075-9c4e-36a0a854f159" />



egrep '(world$)' newfile 
## OUTPUT
<img width="727" height="57" alt="image" src="https://github.com/user-attachments/assets/682238ac-dc99-483a-8b3f-cd320f826808" />



egrep '(World$)' newfile 
## OUTPUT
<img width="755" height="70" alt="image" src="https://github.com/user-attachments/assets/b41fd569-403c-4690-8147-72c0479d16e8" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="880" height="113" alt="image" src="https://github.com/user-attachments/assets/865b5352-b773-498b-964a-51733abe6463" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="766" height="63" alt="image" src="https://github.com/user-attachments/assets/3318a18c-456d-4459-8bc2-4e6c3e05da2e" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="726" height="72" alt="image" src="https://github.com/user-attachments/assets/6bfe0526-ba45-43d3-ab96-6fbc7684e3af" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="663" height="66" alt="image" src="https://github.com/user-attachments/assets/2a5203ee-47cc-46c3-b553-ab4e48adc0f6" />


egrep l{2} newfile
## OUTPUT
<img width="777" height="97" alt="image" src="https://github.com/user-attachments/assets/d356fb7b-d8f2-4b6a-8e42-772032e6eb11" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="762" height="131" alt="image" src="https://github.com/user-attachments/assets/f27ae57d-26bf-4ec1-a86b-c356934ac01c" />


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
<img width="533" height="61" alt="image" src="https://github.com/user-attachments/assets/8ca834a9-b47c-4c5f-9bb1-6e1852c87a8e" />



sed -n -e '$p' file23
## OUTPUT
<img width="548" height="57" alt="image" src="https://github.com/user-attachments/assets/aa9a803e-b969-4904-b443-1ef851632795" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="593" height="272" alt="image" src="https://github.com/user-attachments/assets/41dc900d-c334-4801-89bb-85baf5903d8a" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="597" height="287" alt="image" src="https://github.com/user-attachments/assets/2d25c692-a19d-4fd7-924d-f6108d04a9f5" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="656" height="286" alt="image" src="https://github.com/user-attachments/assets/717c5419-9efd-4bc7-a086-a365cf9966df" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="690" height="185" alt="image" src="https://github.com/user-attachments/assets/b3817dae-b98e-4568-9685-d72e9a274074" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="613" height="127" alt="image" src="https://github.com/user-attachments/assets/02e03dbf-5014-45e8-b55f-c767e4d8097e" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="660" height="90" alt="image" src="https://github.com/user-attachments/assets/243bac2b-a6ae-407b-8ede-e1ae4c5696d3" />



seq 10 
## OUTPUT
<img width="658" height="338" alt="image" src="https://github.com/user-attachments/assets/56439b91-3644-4d59-a51b-61a14dbbcc55" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="662" height="135" alt="image" src="https://github.com/user-attachments/assets/1676aad2-fbd4-483d-bdbc-1cace1c5a004" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="615" height="118" alt="image" src="https://github.com/user-attachments/assets/66e2070e-2374-49f3-9d4f-8bedaba0128d" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="657" height="130" alt="image" src="https://github.com/user-attachments/assets/f325b492-80de-4370-94da-e50841e451dd" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="622" height="147" alt="image" src="https://github.com/user-attachments/assets/b6271ac0-cb2f-4856-887c-603a76fdd7ca" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="605" height="122" alt="image" src="https://github.com/user-attachments/assets/9d402805-aca5-4f15-891f-efe095f08af6" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="657" height="122" alt="image" src="https://github.com/user-attachments/assets/a6cff008-48bf-4571-8aae-406c051158b0" />



sed -n '2,4{s/$/*/;p}' file23
<img width="668" height="125" alt="image" src="https://github.com/user-attachments/assets/b9f347e0-a119-4847-8535-8e3c661f6f61" />


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
<img width="422" height="195" alt="image" src="https://github.com/user-attachments/assets/525ab710-2896-4cdb-a55d-1b761dcfc3b4" />


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
<img width="448" height="183" alt="image" src="https://github.com/user-attachments/assets/c4091445-72c3-40a8-aaae-866b84aa244a" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="748" height="263" alt="image" src="https://github.com/user-attachments/assets/8fce40e3-7784-46ae-8cf6-901102cf68fc" />

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
<img width="761" height="123" alt="image" src="https://github.com/user-attachments/assets/05f6d1b0-b529-48d4-88cd-474dab107b41" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="782" height="127" alt="image" src="https://github.com/user-attachments/assets/3265f1c1-8a0d-4ee1-8c4e-eff529c5e3d9" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="397" height="91" alt="image" src="https://github.com/user-attachments/assets/dabdc5d9-e1db-406e-8e6b-e43d0839c17b" />


tar -xvf backup.tar
## OUTPUT
<img width="440" height="93" alt="image" src="https://github.com/user-attachments/assets/63fbdf15-6c24-4709-8f65-c673f5acd814" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="780" height="157" alt="image" src="https://github.com/user-attachments/assets/921b194c-238c-4f05-9058-253ede631fa8" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="783" height="227" alt="image" src="https://github.com/user-attachments/assets/7055e4f8-7a1f-4d13-a1db-787464ea4d95" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="782" height="318" alt="image" src="https://github.com/user-attachments/assets/a9752412-dbe4-472c-89c8-c55cc090a78c" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="457" height="126" alt="image" src="https://github.com/user-attachments/assets/aab45abd-9a0c-4e78-8f79-2d7701da3bcb" />


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
<img width="582" height="451" alt="image" src="https://github.com/user-attachments/assets/47fa8082-a4e8-4112-92d2-614801f1281e" />

 
ls file1
## OUTPUT
<img width="360" height="62" alt="image" src="https://github.com/user-attachments/assets/da56d6c2-0fd8-4f87-9247-2e0269a0668c" />

echo $?
## OUTPUT
<img width="375" height="68" alt="image" src="https://github.com/user-attachments/assets/9bc638d0-2134-41e6-ae21-6d54d002f947" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="351" height="91" alt="image" src="https://github.com/user-attachments/assets/1738aecc-d1d2-4816-bcca-b577fba1cb41" />

abcd
 
echo $?
 ## OUTPUT
<img width="660" height="300" alt="image" src="https://github.com/user-attachments/assets/6a920a6f-0433-411c-bdb3-f582db93bf1e" />


 
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
<img width="662" height="337" alt="image" src="https://github.com/user-attachments/assets/2e6ea8f3-44e4-4563-b7fd-24c99195a9cb" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="783" height="325" alt="image" src="https://github.com/user-attachments/assets/7948025f-2bf1-41bd-a300-9bd57baa5128" />


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
<img width="781" height="236" alt="image" src="https://github.com/user-attachments/assets/7b794120-5bb2-4495-ab33-d18a6a2a58a9" />

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
<img width="712" height="557" alt="image" src="https://github.com/user-attachments/assets/d36ad6d0-d403-4ff5-8a05-7889da11fdd1" />



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
<img width="746" height="657" alt="image" src="https://github.com/user-attachments/assets/3c75400d-6de8-4680-95d4-b090f5b34d74" />
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
<img width="772" height="662" alt="image" src="https://github.com/user-attachments/assets/91703190-abc1-4df7-8cae-793ce588e642" />

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
<img width="762" height="652" alt="image" src="https://github.com/user-attachments/assets/5ca8036f-8dbb-46c3-a4c4-dfd2847f3bc5" />


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
<img width="688" height="348" alt="image" src="https://github.com/user-attachments/assets/37a91881-163a-4687-9dd1-51625fc2a61d" />

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
<img width="645" height="215" alt="image" src="https://github.com/user-attachments/assets/cf150bbd-978f-4b9e-ae62-15efd038735c" />

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
<img width="567" height="277" alt="image" src="https://github.com/user-attachments/assets/6a712879-5236-40b3-a3be-06d40d62c10e" />


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
<img width="530" height="282" alt="image" src="https://github.com/user-attachments/assets/7ea21e8e-3837-4f69-98bb-89ce6f673e7f" />

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
<img width="781" height="302" alt="image" src="https://github.com/user-attachments/assets/bc1a7d01-95d0-4da0-a7cf-4c15f9a655c0" />

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
<img width="777" height="297" alt="image" src="https://github.com/user-attachments/assets/02c2daef-5b50-4411-8af7-6675635aefe7" />

 
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
<img width="783" height="292" alt="image" src="https://github.com/user-attachments/assets/5172f28b-c655-4af2-83cc-ca242620cf2c" />

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
<img width="785" height="307" alt="image" src="https://github.com/user-attachments/assets/9560d4f2-348b-4ce4-9b4d-e9181b6146ea" />
 
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
<img width="627" height="191" alt="image" src="https://github.com/user-attachments/assets/eb5de56e-cbd2-4d6a-bafc-9a822032983a" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="678" height="147" alt="image" src="https://github.com/user-attachments/assets/3b576f6e-618b-48d3-a2b7-134a833194e8" />



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
 ./funcex.sh <img width="661" height="20" alt="image" src="https://github.com/user-attachments/assets/97030c78-3129-4626-812f-71b78219afce" />


 
 ./funcex.sh 1 2 <img width="650" height="26" alt="image" src="https://github.com/user-attachments/assets/741986cc-4eae-4646-afc4-64da65da13be" />


 
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
<img width="636" height="62" alt="image" src="https://github.com/user-attachments/assets/a60219aa-038b-442b-a847-e2a8b8bc6cc6" />

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
<img width="783" height="72" alt="image" src="https://github.com/user-attachments/assets/007c4fc5-cdaf-4d8b-8e2c-0400d6a8727d" />

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
<img width="711" height="376" alt="image" src="https://github.com/user-attachments/assets/2a96e726-92a9-404c-92d9-a901f1d63c14" />

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
<img width="481" height="243" alt="image" src="https://github.com/user-attachments/assets/5abbf416-26b4-479f-b40e-441494fdec06" />

 
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
<img width="608" height="70" alt="image" src="https://github.com/user-attachments/assets/31ed20d3-bfa1-4775-8501-3af539e181bd" />



# RESULT:
The Commands are executed successfully.
