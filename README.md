 OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# NAME : JAIRAM J
# REG NO : 212225040141

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
<img width="569" height="155" alt="1" src="https://github.com/user-attachments/assets/800222a8-42da-4954-b2d1-a045f188db10" />



cat < file2
## OUTPUT
<img width="567" height="149" alt="1b" src="https://github.com/user-attachments/assets/f495b5d0-c5e0-4234-ab36-f038f386e166" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="564" height="219" alt="1c" src="https://github.com/user-attachments/assets/68df3eb1-5979-4cff-8002-a8b5d7335ca1" />



comm file1 file2
 ## OUTPUT

 <img width="572" height="302" alt="1d" src="https://github.com/user-attachments/assets/78b3ebda-be15-49d2-9480-2b74c0b3f41c" />

diff file1 file2
## OUTPUT
<img width="569" height="210" alt="2a" src="https://github.com/user-attachments/assets/3b330cae-548f-4752-ad4e-927ff8a16454" />


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


<img width="552" height="232" alt="2b" src="https://github.com/user-attachments/assets/de730664-4737-4cf2-9031-6ecd62d32da6" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="412" height="87" alt="2c" src="https://github.com/user-attachments/assets/98022bb4-fdc6-4d4f-87d5-8d36e16aaf0d" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="497" height="133" alt="2d" src="https://github.com/user-attachments/assets/bad52617-837b-4e67-a9af-e3d25dbc93af" />

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 output
<img width="511" height="114" alt="2f" src="https://github.com/user-attachments/assets/5a633187-c176-4795-b1fb-81dee1bafcc4" />

grep Hello newfile 
## OUTPUT

<img width="539" height="55" alt="2g" src="https://github.com/user-attachments/assets/3afa3b04-5d63-4225-b0f0-fbc25941f6c6" />


grep hello newfile 
## OUTPUT

<img width="561" height="77" alt="2h" src="https://github.com/user-attachments/assets/38355937-378c-42bc-bc18-b1d2a1cc4ca9" />



grep -v hello newfile 
## OUTPUT

<img width="506" height="82" alt="2i" src="https://github.com/user-attachments/assets/2837a88c-4019-4ea6-8e04-de919406c5a9" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="542" height="100" alt="2j" src="https://github.com/user-attachments/assets/f0534c26-32f2-4103-8095-0fdc7fde21c6" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="564" height="85" alt="2k" src="https://github.com/user-attachments/assets/500ecc7c-fae2-44e5-92b9-fb05f70f4a5f" />



grep -R ubuntu /etc
## OUTPUT

<img width="807" height="604" alt="2l" src="https://github.com/user-attachments/assets/04166daa-6039-47f4-af28-f9b26e8c3346" />


grep -w -n world newfile   
## OUTPUT
<img width="528" height="102" alt="2m" src="https://github.com/user-attachments/assets/28b54dea-6773-4ab8-bd86-ef52ddb5a937" />


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
output
<img width="633" height="300" alt="3a" src="https://github.com/user-attachments/assets/59f0f659-6219-48d6-848b-93be6dca9fd6" />

egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="799" height="77" alt="3b" src="https://github.com/user-attachments/assets/aea00946-cf2c-480a-bfbc-f669016c2088" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="824" height="95" alt="3c" src="https://github.com/user-attachments/assets/c87e73e7-39eb-4cb0-930e-efad43a3a771" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="576" height="100" alt="3d" src="https://github.com/user-attachments/assets/657921b3-6ad7-4968-b022-36ef3f26f1ad" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="615" height="86" alt="3e" src="https://github.com/user-attachments/assets/d8830397-0588-46c6-bc99-b2db880906b3" />


egrep '(world$)' newfile 
## OUTPUT
<img width="815" height="106" alt="3f" src="https://github.com/user-attachments/assets/f6ef6751-96f2-44cb-8e06-448403be1b86" />



egrep '(World$)' newfile 
## OUTPUT

<img width="815" height="106" alt="3f" src="https://github.com/user-attachments/assets/dc12b68c-18a8-4486-b3b1-d0cbb8b101f2" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="815" height="106" alt="3f" src="https://github.com/user-attachments/assets/823ada53-b08a-4bfd-af63-576389a83385" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="671" height="77" alt="3g" src="https://github.com/user-attachments/assets/675ca7c7-1a21-457a-baf7-bd5eee1602d5" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="771" height="79" alt="3h" src="https://github.com/user-attachments/assets/3e5e6074-a6e3-465a-8662-14860afac410" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="433" height="79" alt="3i" src="https://github.com/user-attachments/assets/92a2e61f-7057-490b-9dd1-daee96905c56" />


egrep l{2} newfile
## OUTPUT
<img width="397" height="108" alt="3j" src="https://github.com/user-attachments/assets/2d55e5b4-1ad7-4cff-be86-affe5e9f0f45" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="834" height="133" alt="3k" src="https://github.com/user-attachments/assets/28d133f6-d3d2-4a92-85bc-b922b1592fb9" />


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
output
<img width="407" height="504" alt="4a" src="https://github.com/user-attachments/assets/65e0a421-e0f5-45d7-b705-7a82b37d0dc7" />


sed -n -e '3p' file23
## OUTPUT

<img width="340" height="80" alt="4b" src="https://github.com/user-attachments/assets/e18c9750-09b9-4bdb-8fa1-0b7bbce7fd67" />


sed -n -e '$p' file23
## OUTPUT

<img width="467" height="74" alt="4c" src="https://github.com/user-attachments/assets/c2bc4214-91b9-4e8a-bd40-376f62d45e20" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="425" height="249" alt="4d" src="https://github.com/user-attachments/assets/d112adba-a63e-4382-8bd2-ba7aa7168c73" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="447" height="257" alt="4e" src="https://github.com/user-attachments/assets/dcd356e0-2d60-4bbc-8324-b9978ab06696" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="563" height="248" alt="4f" src="https://github.com/user-attachments/assets/b869c70e-9c67-4c7c-977d-1f9b0640cd0c" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="390" height="180" alt="4g" src="https://github.com/user-attachments/assets/416b5951-9104-4c98-bade-5358a8887746" />



sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="634" height="132" alt="4h" src="https://github.com/user-attachments/assets/283a77ff-9365-456f-8f95-e01adf3b80c2" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="679" height="107" alt="4k" src="https://github.com/user-attachments/assets/0878d283-3b23-4fc3-819b-7079c23c0c2c" />

seq 10 
## OUTPUT

<img width="389" height="306" alt="4l" src="https://github.com/user-attachments/assets/eea8f169-523d-4b82-8234-cfe639d0e044" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="499" height="138" alt="4m" src="https://github.com/user-attachments/assets/1fa437d7-fdd1-44a0-a345-a9dcf2af6b69" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="393" height="132" alt="4n" src="https://github.com/user-attachments/assets/12ea2fb5-4bce-463e-bfd7-ef4880118925" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="475" height="153" alt="4o" src="https://github.com/user-attachments/assets/a9ab67db-e45d-40d2-ae2c-ebfe6274929d" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="565" height="123" alt="4p" src="https://github.com/user-attachments/assets/e7754107-2ce4-4daa-a6bf-eaaa8cc772a0" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="546" height="132" alt="4q" src="https://github.com/user-attachments/assets/1b361eac-7837-4e4b-90bf-b2439bbe149c" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="429" height="127" alt="4r" src="https://github.com/user-attachments/assets/1c80b31c-7c0b-4b3c-a774-f3b7630f2de6" />


sed -n '2,4{s/$/*/;p}' file23
<img width="429" height="127" alt="4r" src="https://github.com/user-attachments/assets/8f4d972f-613c-4414-8152-d90a43456dc4" />


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
<img width="525" height="330" alt="5a" src="https://github.com/user-attachments/assets/e8c94492-cc6e-4337-b7ec-6575d6855a23" />


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
<img width="396" height="355" alt="5b" src="https://github.com/user-attachments/assets/f4da8664-029b-4b11-956f-5a6562a5581e" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="640" height="178" alt="5c" src="https://github.com/user-attachments/assets/e8e129eb-d4fc-400e-b919-61890e4dab9b" />

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

<img width="493" height="204" alt="5d" src="https://github.com/user-attachments/assets/348c93f3-1730-4f76-abac-718f811b35f0" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="669" height="107" alt="5f" src="https://github.com/user-attachments/assets/3ed075e0-2c5c-4df4-becd-2b28151243df" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="634" height="353" alt="5g" src="https://github.com/user-attachments/assets/9892da89-cc98-4355-8d0c-2ba2d6b3e65b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="634" height="353" alt="5g" src="https://github.com/user-attachments/assets/bfdf0de7-8a18-4251-aea7-e35090dbd121" />


tar -xvf backup.tar
## OUTPUT
<img width="634" height="353" alt="5g" src="https://github.com/user-attachments/assets/afdfd515-8b51-4063-8329-8ecde5afa994" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="634" height="353" alt="5g" src="https://github.com/user-attachments/assets/c49782f9-d625-42ee-ac09-8401c2bb035b" />

gunzip backup.tar.gz
## OUTPUT

 <img width="669" height="107" alt="5f" src="https://github.com/user-attachments/assets/f4bf81e2-de8a-4348-9cf4-19a1af840509" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="634" height="292" alt="6a" src="https://github.com/user-attachments/assets/8652633c-885c-4f5f-bec3-db8657ceafe8" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="394" height="282" alt="6b" src="https://github.com/user-attachments/assets/b457392f-9875-43f9-90fb-a2b0fc5e9a50" />


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

 <img width="484" height="429" alt="6c" src="https://github.com/user-attachments/assets/a3d046a0-6a1e-43a3-9776-f26122686c78" />

ls file1
## OUTPUT
<img width="608" height="87" alt="6d" src="https://github.com/user-attachments/assets/7420d289-f0c3-4cb5-989c-31a35a21c584" />

echo $?
## OUTPUT

 <img width="615" height="84" alt="6e" src="https://github.com/user-attachments/assets/497f7b3c-8a31-444a-8512-a77a9b2c9c1b" />
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
 <img width="568" height="86" alt="6f" src="https://github.com/user-attachments/assets/a67aab71-3deb-4c06-94e0-89c9d1e39398" />


abcd
 
echo $?
 ## OUTPUT

<img width="570" height="74" alt="6h" src="https://github.com/user-attachments/assets/f1f5e34e-34b9-45ba-b468-b060627b6b10" />

 
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
<img width="795" height="119" alt="6i" src="https://github.com/user-attachments/assets/38052fe4-8744-4353-9b7a-5c01c6711249" />


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
<img width="595" height="331" alt="image" src="https://github.com/user-attachments/assets/5cd1cfa4-d480-4a7e-a8e8-7fcc3c3ce784" />

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

<img width="788" height="488" alt="7a" src="https://github.com/user-attachments/assets/dd00f3de-9d7b-4736-a0d4-08b62a9b64e7" />


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
<img width="580" height="427" alt="7b" src="https://github.com/user-attachments/assets/ca22a4a0-b9f1-4c2b-b5f6-bec90ac462a6" />

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
<img width="475" height="481" alt="7c" src="https://github.com/user-attachments/assets/f9102495-666d-4514-a709-5d1f06ce1faa" />

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

<img width="650" height="459" alt="7d" src="https://github.com/user-attachments/assets/c5dff5b7-558a-4067-873a-303d50c0d4e3" />

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
<img width="690" height="427" alt="7e" src="https://github.com/user-attachments/assets/eb86ff16-ea10-46bd-9aff-c0cad9658671" />

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
 output:
 <img width="750" height="598" alt="7g" src="https://github.com/user-attachments/assets/f31d3cff-374b-4ea6-8e46-73b4439c5adb" />

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
 output:
 
 <img width="742" height="509" alt="7h" src="https://github.com/user-attachments/assets/a069cf0d-9413-466d-aa63-65133c1b0cfe" />

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
 output:
 <img width="467" height="380" alt="7i" src="https://github.com/user-attachments/assets/d5de2c57-a204-4765-9945-01a219140762" />

 <img width="581" height="226" alt="7j" src="https://github.com/user-attachments/assets/d1996bb9-34b4-4469-b541-1e86afa604fc" />

 
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
 output:
 <img width="801" height="318" alt="7k" src="https://github.com/user-attachments/assets/8c2082c1-e75b-4bb1-b1c1-9e764589c47f" />

 
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
 output:
 <img width="802" height="302" alt="7l" src="https://github.com/user-attachments/assets/bebd9ff4-efca-4b9e-a1f1-e7becc1d47c4" />

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
 output:
 <img width="813" height="403" alt="7m" src="https://github.com/user-attachments/assets/e22641a3-d66f-4326-8bc6-16ad768dd84f" />

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
<img width="728" height="332" alt="7n" src="https://github.com/user-attachments/assets/d3342a43-4d95-4315-b452-c32f02257f75" />

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

<img width="797" height="502" alt="7o" src="https://github.com/user-attachments/assets/f3fe679a-7d2d-481c-97fd-70e74f239b8b" />

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

<img width="412" height="406" alt="7p" src="https://github.com/user-attachments/assets/62ccf726-72ee-4547-a8db-eb1066b32805" />

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

<img width="452" height="225" alt="7q" src="https://github.com/user-attachments/assets/26f9d1c9-196c-4514-a4fa-cc57ee981edf" />

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

 <img width="652" height="395" alt="7r" src="https://github.com/user-attachments/assets/bc9b804c-ddab-437d-b674-c33df6ce7c1c" />

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

<img width="627" height="122" alt="7s" src="https://github.com/user-attachments/assets/0c7e73db-ac49-4efb-88d4-3bf935fdbb65" />

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
 <img width="804" height="219" alt="7t" src="https://github.com/user-attachments/assets/cf3e97c7-0d38-4311-84e6-5fc5a239f849" />

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
<img width="749" height="310" alt="7v" src="https://github.com/user-attachments/assets/e7dc508f-5441-4e4f-b3e6-f03d389912a6" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="749" height="310" alt="7v" src="https://github.com/user-attachments/assets/9039622a-cbd8-4e99-a079-681103bff89c" />


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
<img width="776" height="407" alt="8a" src="https://github.com/user-attachments/assets/9557363e-80ba-45a9-ace8-780369cf2d96" />

 
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
<img width="572" height="375" alt="8b" src="https://github.com/user-attachments/assets/f0dfdd65-3637-4932-91a1-015afc64219b" />

 
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
<img width="437" height="173" alt="8c" src="https://github.com/user-attachments/assets/3b7885ae-b7ed-47d2-b735-77a55362ff29" />

 
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
 <img width="363" height="403" alt="8d" src="https://github.com/user-attachments/assets/617b2616-a2d2-4b33-8fc4-f4f526731562" />

 
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
 
 <img width="325" height="373" alt="8e" src="https://github.com/user-attachments/assets/b8c50666-fe14-4dbc-a8b0-74e83a6495c8" />

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
<img width="704" height="163" alt="8f" src="https://github.com/user-attachments/assets/4af18118-1ddd-4817-90b0-30959f033e0f" />


# RESULT:
The Commands are executed successfully.
