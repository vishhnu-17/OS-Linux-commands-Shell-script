# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise

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

![Screenshot from 2025-04-25 20-48-26](https://github.com/user-attachments/assets/e3cb1695-8a27-4997-bb7e-81371f2f2878)






cat < file2
## OUTPUT

![Screenshot from 2025-04-25 20-49-29](https://github.com/user-attachments/assets/f07a90b9-4e7a-436c-a296-5a7f309c0d31)







# Comparing Files
cmp file1 file2
## OUTPUT

![Screenshot from 2025-04-25 20-50-30](https://github.com/user-attachments/assets/54ee3c79-ebdd-43cd-9e23-7b1abeb4a4aa)









 
comm file1 file2
 ## OUTPUT

 ![Screenshot from 2025-04-25 20-51-16](https://github.com/user-attachments/assets/b7aa3b03-0dbe-44b7-a706-391aacaa5cc0)


 

 
diff file1 file2
## OUTPUT

![Screenshot from 2025-04-25 20-51-53](https://github.com/user-attachments/assets/b299beae-1f2e-4b84-b1b2-883a0c1c14f2)



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

![Screenshot from 2025-04-25 20-54-35](https://github.com/user-attachments/assets/bc2cb991-18be-4bfc-8a17-51837e073266)





cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2025-04-25 20-56-30](https://github.com/user-attachments/assets/d85a8241-454c-46ee-be9d-d84b7902b1ba)




cut -d "|" -f 2 file22
## OUTPUT

![Screenshot from 2025-04-25 20-57-59](https://github.com/user-attachments/assets/81252646-acb0-458f-a7e3-d7c21cb07929)



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

![Screenshot from 2025-04-25 21-00-00](https://github.com/user-attachments/assets/44267004-9782-4fee-ab82-5666b994966d)






grep hello newfile 
## OUTPUT

![Screenshot from 2025-04-25 21-01-01](https://github.com/user-attachments/assets/d0a502c0-e66f-49e7-9945-84f929f2788e)






grep -v hello newfile 
## OUTPUT

![Screenshot from 2025-04-25 21-01-18](https://github.com/user-attachments/assets/db17482a-40aa-4d0f-b1c8-d1449688440f)






cat newfile | grep -i "hello"
## OUTPUT


![Screenshot from 2025-04-25 21-01-42](https://github.com/user-attachments/assets/87b1327d-543d-467f-8a03-d46c15c8b375)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-04-25 21-02-14](https://github.com/user-attachments/assets/4fb16060-5405-4373-b927-59a94f3f3218)








grep -w -n world newfile   
## OUTPUT

![Screenshot from 2025-04-25 21-02-47](https://github.com/user-attachments/assets/d59a9cba-d3df-4593-a583-15185845bfd0)



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

![Screenshot from 2025-04-25 21-04-39](https://github.com/user-attachments/assets/9bccb57a-6bba-42af-abe2-86cb8d3bb83f)






egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-04-25 21-05-10](https://github.com/user-attachments/assets/404c9db7-115a-4e40-8cd3-30bce36a6a1f)





egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-04-25 21-05-39](https://github.com/user-attachments/assets/e7b05656-1a51-41ea-bcbd-3774866230e1)







egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-04-25 21-06-27](https://github.com/user-attachments/assets/f67c46b7-3ace-4bc4-a6bb-a1bc9fdc236a)




egrep '(world$)' newfile 
## OUTPUT






egrep '(World$)' newfile 
## OUTPUT

![Screenshot from 2025-04-25 15-49-47](https://github.com/user-attachments/assets/d560f33c-92fb-4be3-b447-67075b3bd993)



egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2025-04-25 15-50-18](https://github.com/user-attachments/assets/af08ef07-a306-4dca-8156-ffda91a15db2)




egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-04-25 15-50-50](https://github.com/user-attachments/assets/67af3c8a-ca9e-4bdf-a7c2-21634b380813)




egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-04-25 15-51-12](https://github.com/user-attachments/assets/0019ba84-5e8e-4800-9a7a-54467f0d8766)




egrep 'Linux.*World' newfile 
## OUTPUT


egrep l{2} newfile
## OUTPUT



egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot from 2025-04-25 15-51-35](https://github.com/user-attachments/assets/ec64562b-4c12-465d-b1fa-ac2fc6d3000f)





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

![Screenshot from 2025-04-27 12-00-10](https://github.com/user-attachments/assets/95d6995f-4c0b-481c-a775-7c56071bae36)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-04-27 12-01-25](https://github.com/user-attachments/assets/5246892a-1405-4021-be5c-3b7e1caa559c)






sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-04-27 12-01-44](https://github.com/user-attachments/assets/504baae1-0800-460f-bb23-f9afcecb9164)






sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-04-27 12-02-15](https://github.com/user-attachments/assets/7706529a-56ce-4813-97fe-7490541cae0d)






sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-04-27 12-02-46](https://github.com/user-attachments/assets/ae9df86f-ac81-44f6-8db8-8be4a3baee41)






sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-27 12-03-04](https://github.com/user-attachments/assets/a714ff34-1879-49a0-b477-be3350e1b2e5)







sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-27 12-03-25](https://github.com/user-attachments/assets/884fd149-d636-44a0-b804-7d19e432eb42)






seq 10 
## OUTPUT

![Screenshot from 2025-04-27 12-03-40](https://github.com/user-attachments/assets/9c03315e-4de4-4c57-844d-cdd907cb1643)

seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-04-27 12-03-59](https://github.com/user-attachments/assets/62b31162-4f48-47bb-9dd4-6b24571e8bd0)

seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-04-27 12-04-14](https://github.com/user-attachments/assets/7b789b2a-c38f-4c51-aa8e-a888357bb197)




seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2025-04-27 12-04-39](https://github.com/user-attachments/assets/1fe683f3-68b0-413f-8c51-7f253e98e730)






seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2025-04-27 12-04-58](https://github.com/user-attachments/assets/4e371ed6-db87-4a9d-b39a-c166c9b5a4c3)





seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2025-04-27 12-05-13](https://github.com/user-attachments/assets/74fde64f-86b9-403a-910a-e864f0035ac7)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-04-27 12-05-28](https://github.com/user-attachments/assets/b185954a-ff33-43e4-bd5b-b924fedd4ed1)





sed -n '2,4{s/$/*/;p}' file23
## OUTPUT:






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

![Screenshot from 2025-04-27 12-06-24](https://github.com/user-attachments/assets/d6b54d16-7b4b-499b-9b21-88520b56f266)



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


![Screenshot from 2025-04-27 12-06-54](https://github.com/user-attachments/assets/2afd5a38-deb2-4d32-a09d-af12e66eb7b3)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 ![Screenshot from 2025-04-27 12-07-19](https://github.com/user-attachments/assets/24fa3c85-7a4c-4cae-a2e0-c3184ebe3305)


 

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

 ![Screenshot from 2025-04-27 12-09-14](https://github.com/user-attachments/assets/9e18596e-1a3c-414f-a667-aa2801a4e706)


 


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2025-04-27 12-09-57](https://github.com/user-attachments/assets/016dcae2-7589-4497-9f48-223e632d2bc9)




#Backup commands
tar -cvf backup.tar *
## OUTPUT


![432115930-2ccfbed2-734e-4e45-bbe2-1e8e07e28f89](https://github.com/user-attachments/assets/fa89ba97-992d-4a0e-aef2-a4397d57cbf0)




mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


![432116050-b090597c-0ecd-419f-a678-1ffb97768c94](https://github.com/user-attachments/assets/4579627d-b456-4f38-a369-4a67f1b6d7d9)




tar -xvf backup.tar
## OUTPUT


![432116125-1b40b14d-9db7-4c77-b36d-c850d4e1fc36](https://github.com/user-attachments/assets/95c4df4b-29c6-4814-a8d9-a53a3d4fd788)


gzip backup.tar

ls .gz
## OUTPUT
![432116203-a7eadb43-e5b0-4ac1-9762-57787e6d65c9](https://github.com/user-attachments/assets/35bc0978-22c4-42cc-bcbf-90ba1cee90d6)




 
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

![Screenshot from 2025-04-27 12-12-22](https://github.com/user-attachments/assets/603ec5e7-0d47-492b-9794-2d88ec86a55c)



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


![308621144-aa9e221b-1914-41c6-96a4-a3480fcc931c](https://github.com/user-attachments/assets/0270506e-61b7-4efb-81b6-54f3cb59e4e4)




 
ls file1
## OUTPUT
![308621222-7aa3c8d8-08cf-4789-be3e-8eb056aec0c6](https://github.com/user-attachments/assets/9f409548-1175-4d1c-bb69-5a429e20b5ca)



echo $?

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

![308621428-b392932f-12c9-47bf-9d86-fb44457adb34](https://github.com/user-attachments/assets/78b9f091-bd6e-47d8-9889-7963f660c8f0)

 
abcd
 
echo $?
 ## OUTPUT

 ![308621520-6cac1aec-beb9-4683-91ba-2a6e062a4fd3](https://github.com/user-attachments/assets/e101edfe-e3ba-4a15-848f-737c10be66c6)



 
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

![308621595-f8e710dd-372f-4b4c-9db1-efd9aa88e581](https://github.com/user-attachments/assets/c4d4c311-c7f3-4d19-af43-017e53dc650f)





chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![308621672-23f2ccf2-f9e4-4dff-98fc-0b3812c642a5](https://github.com/user-attachments/assets/c0c1e279-ec8c-46f0-89fd-dbf0587ca0e5)


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

![308621891-f0646e68-4bbe-4c0e-bf34-7212526995d8](https://github.com/user-attachments/assets/731dfc7b-7bfd-40c2-a4e9-914c3aaea85c)




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
![308622068-a2ca4461-3b62-41b0-afa0-eb9523ebc501](https://github.com/user-attachments/assets/586f1351-665e-4b57-bfdc-d4aa1c025f70)



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

![308622136-8d68fc65-0b14-4777-af74-cefbc365c662](https://github.com/user-attachments/assets/0b939587-c909-404c-94fd-bd202fe2c0d2)


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

![308622542-ef2f1f17-feed-4357-a5a0-e63e33ea14be](https://github.com/user-attachments/assets/dba45127-d481-4634-b62d-9c4631688192)

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

 ![308622796-d60ca9a2-6750-4f0e-bd8a-bad4b996fbce](https://github.com/user-attachments/assets/e9cfe8d8-821a-48d0-894d-79247ac3a8e4)


 
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

![308622964-cd016d47-b62c-4697-8211-2ccbb4e91301](https://github.com/user-attachments/assets/4c851d85-07c5-44a2-a3ce-323f1d6a4176)

 
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

![308623114-33663a39-1b90-46dc-a249-29cce8e18d43](https://github.com/user-attachments/assets/13888574-224d-4de0-86d1-e9f4a0665ff8)



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![308623114-33663a39-1b90-46dc-a249-29cce8e18d43](https://github.com/user-attachments/assets/be064b06-7f57-4d55-ba45-d266e61c44e0)




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

 ![308623958-22c9f9e9-ae69-4152-9768-0122fe2f2a21](https://github.com/user-attachments/assets/d246f1b4-ec89-47f7-954c-9c4f22ed1669)

 
 
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
![308624028-538413e2-0bfb-498f-bd90-181bb3e71a69](https://github.com/user-attachments/assets/c038013d-c56d-4d1b-92f4-5dd5c0ff9508)


 
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

## OUTPUT:

![308624193-736ba1b8-9102-4b04-bf53-666e03ad5961](https://github.com/user-attachments/assets/666defed-282b-4ac2-ac9c-cae20b2bfa5a)


# RESULT:
The Commands are executed successfully.
