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
<img width="637" height="148" alt="image" src="https://github.com/user-attachments/assets/605a949c-7a18-47b7-9deb-c328343c0109" />


cat < file2
## OUTPUT
<img width="662" height="163" alt="image" src="https://github.com/user-attachments/assets/847dc923-d7ba-4945-9909-88237a7747ad" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="660" height="55" alt="image" src="https://github.com/user-attachments/assets/983e910b-a3a3-47e3-9ee5-b67af3367934" />

comm file1 file2
 ## OUTPUT
<img width="738" height="333" alt="image" src="https://github.com/user-attachments/assets/132b52f6-85ed-459b-985b-dfea37602f09" />

 
diff file1 file2
## OUTPUT
<img width="731" height="240" alt="image" src="https://github.com/user-attachments/assets/1c93c964-db42-4db0-b4d8-353d7b281ea6" />


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
<img width="663" height="102" alt="image" src="https://github.com/user-attachments/assets/2ef99e7d-e209-4015-b6c3-2e502959dc57" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="732" height="116" alt="image" src="https://github.com/user-attachments/assets/497bd286-458d-4654-b8cb-48d2d94c971b" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="747" height="132" alt="image" src="https://github.com/user-attachments/assets/1e36bd80-50a2-4744-9f38-5737f6cea8d0" />


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

<img width="720" height="38" alt="image" src="https://github.com/user-attachments/assets/3989b66c-9be8-49ce-9065-731e2d668fcd" />

grep hello newfile 
## OUTPUT

<img width="673" height="45" alt="image" src="https://github.com/user-attachments/assets/0d1e7a34-0fdf-4514-bf87-a5e809ae9daf" />



grep -v hello newfile 
## OUTPUT

<img width="720" height="62" alt="image" src="https://github.com/user-attachments/assets/ddeb4e64-c85c-434a-8884-00fc54c398b5" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="791" height="65" alt="image" src="https://github.com/user-attachments/assets/80e60352-5706-4898-a797-71d2d478e231" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="830" height="47" alt="image" src="https://github.com/user-attachments/assets/636a6e65-f09f-4e54-b893-5804cd1666e7" />



grep -R ubuntu /etc
## OUTPUT

<img width="885" height="72" alt="image" src="https://github.com/user-attachments/assets/5c775699-2f6b-4fa5-a772-c426b3d49651" />


grep -w -n world newfile   
## OUTPUT
<img width="947" height="837" alt="image" src="https://github.com/user-attachments/assets/313b148d-5bf3-4a61-8c41-fffb48916666" />


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

<img width="812" height="237" alt="image" src="https://github.com/user-attachments/assets/91fbdce7-e7ff-46a8-8078-912e94f8566c" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="801" height="75" alt="image" src="https://github.com/user-attachments/assets/f0a77f06-5fb8-4975-bd23-ec3ca8a8cedc" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="838" height="66" alt="image" src="https://github.com/user-attachments/assets/92825a0b-e15c-4d04-ac56-59adf43c8926" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="762" height="43" alt="image" src="https://github.com/user-attachments/assets/53c866ff-f527-4781-9c33-334f4aa7f0b9" />



egrep '(world$)' newfile 
## OUTPUT
<img width="743" height="72" alt="image" src="https://github.com/user-attachments/assets/a3609d05-8b6f-4043-825a-5d436e4d86a0" />



egrep '(World$)' newfile 
## OUTPUT

<img width="766" height="62" alt="image" src="https://github.com/user-attachments/assets/d6ef6dc0-a2f8-4eca-92ac-662dfef9954b" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="795" height="98" alt="image" src="https://github.com/user-attachments/assets/00e79c65-7bec-4625-b84e-0f03ab5b91ee" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="717" height="52" alt="image" src="https://github.com/user-attachments/assets/0f7c3f67-29b3-4018-a9a6-f3baeb8ad314" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="812" height="50" alt="image" src="https://github.com/user-attachments/assets/b41d7492-90ce-4bc4-96de-d757be616c70" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="821" height="58" alt="image" src="https://github.com/user-attachments/assets/41a4fb77-710e-4303-832a-381a253b7a9b" />


egrep l{2} newfile
## OUTPUT
<img width="685" height="71" alt="image" src="https://github.com/user-attachments/assets/47595f95-0f58-4dbd-a68e-1fe5d9a62a81" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="767" height="88" alt="image" src="https://github.com/user-attachments/assets/16aaeea2-17eb-42eb-b0e8-c1a639056c76" />


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
<img width="741" height="55" alt="image" src="https://github.com/user-attachments/assets/3c3694b7-5de9-4751-9ce5-0687e9c60dd1" />



sed -n -e '$p' file23
## OUTPUT

<img width="725" height="47" alt="image" src="https://github.com/user-attachments/assets/056cb818-b2a8-456e-b60c-32db5ee38b3b" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="802" height="230" alt="image" src="https://github.com/user-attachments/assets/f8366c3f-f768-48e3-9c24-a182963c6120" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="857" height="240" alt="image" src="https://github.com/user-attachments/assets/916d9916-23ca-4171-9f73-693ec2e688b3" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="943" height="242" alt="image" src="https://github.com/user-attachments/assets/da34cffd-9adf-41a2-a650-a1f438062425" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="820" height="150" alt="image" src="https://github.com/user-attachments/assets/25520b03-671f-4806-87ee-ec2f11585b0f" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="797" height="95" alt="image" src="https://github.com/user-attachments/assets/34367900-a0bc-4ebe-8403-b58ef2bc6886" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="840" height="68" alt="image" src="https://github.com/user-attachments/assets/4a1a0438-8dcc-4545-9c5c-07d693797bdc" />



seq 10 
## OUTPUT

<img width="715" height="261" alt="image" src="https://github.com/user-attachments/assets/79264cb7-b3a6-488d-bb82-07b6027c849d" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="726" height="87" alt="image" src="https://github.com/user-attachments/assets/83acb573-18d4-4d48-b7e7-ae9878425b14" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="778" height="95" alt="image" src="https://github.com/user-attachments/assets/acad21b9-88a0-44ad-b846-428ab40e9301" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="708" height="126" alt="image" src="https://github.com/user-attachments/assets/8ceec196-ecc1-4c9c-b4cd-0295f412aef7" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="732" height="87" alt="image" src="https://github.com/user-attachments/assets/fa1d69c0-be6e-4f0e-b718-bd4921526adf" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="781" height="98" alt="image" src="https://github.com/user-attachments/assets/63e777c5-9c8e-4fb7-bf8d-de50a0906d05" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="796" height="106" alt="image" src="https://github.com/user-attachments/assets/025e7b0e-6c2f-4d9b-8ed7-719649a8b374" />


sed -n '2,4{s/$/*/;p}' file23
<img width="833" height="95" alt="image" src="https://github.com/user-attachments/assets/7196ccbe-18db-44cc-bf9b-a3d2a45b0b25" />


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
<img width="702" height="285" alt="image" src="https://github.com/user-attachments/assets/182ce348-00e4-425c-9be4-a2895cde5066" />


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
<img width="591" height="135" alt="image" src="https://github.com/user-attachments/assets/0702dc6e-ab50-427d-81cf-8564799ae1e9" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="930" height="245" alt="image" src="https://github.com/user-attachments/assets/e4be18dd-810e-4c5b-be1d-923472b2f7f4" />

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
<img width="746" height="113" alt="image" src="https://github.com/user-attachments/assets/751dd7c8-c9d4-476d-a8c4-00fef3010baf" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="817" height="120" alt="image" src="https://github.com/user-attachments/assets/02ca3d4c-4fe9-4b82-9403-74e48f22cdf0" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="783" height="210" alt="image" src="https://github.com/user-attachments/assets/cfd61f15-c955-4360-9a9a-342728dea761" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="853" height="290" alt="image" src="https://github.com/user-attachments/assets/89600089-3f4a-4957-9508-a44f51e35a9e" />

tar -xvf backup.tar
## OUTPUT
<img width="918" height="218" alt="image" src="https://github.com/user-attachments/assets/f07ed4be-d57f-42dc-b11a-83fe2cd75be1" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="746" height="70" alt="image" src="https://github.com/user-attachments/assets/40962f97-1d91-4371-961f-09ddc54f904f" />

gunzip backup.tar.gz
## OUTPUT
<img width="798" height="25" alt="image" src="https://github.com/user-attachments/assets/d0a1c08d-1956-448b-b554-5454819c4400" />

 
# Shell Script
```
cat > my-script.sh <<'EOF'
#!/bin/bash
echo "Hello World"
exit 0
EOF
chmod 755 my-script.sh
./my-script.sh
```
## OUTPUT
<img width="935" height="190" alt="image" src="https://github.com/user-attachments/assets/95d8e7d4-c96c-417e-afd8-0245ef697123" />
```

prathiksha@DESKTOP-MOHHBTU:~/Experiment1/backupdir$ cat <<EOF > herecheck.txt
hello in this world
i cant stop
for this non stop movement
EOF
cat herecheck.txt
```
## OUTPUT
<img width="870" height="212" alt="image" src="https://github.com/user-attachments/assets/4c1c299b-e4b9-4b53-8b97-1408922a7962" />
```
cat > scriptest.sh <<'EOF'
#!/bin/bash
echo "File name is $0"
echo "First argument is $1"
echo "Second argument is $2"
echo "All arguments are $@"
echo "Number of arguments is $#"
EOF
chmod 755 scriptest.sh
./scriptest.sh 1 2
File name is ./scriptest.sh
```
## OUTPUT

<img width="905" height="358" alt="image" src="https://github.com/user-attachments/assets/0a8443c3-0fcb-40fa-aa7b-ac213b97c36b" />




# RESULT:
The Commands are executed successfully.
