
# Linux SLA  A029
## Q.1 Write a shell script that takes a user's name as input and greets them.

```
terminal
nvim greet.sh 
chmod +x greet.sh 
./greet.sh
```

```
Shell Script
#! /bin/bash
echo "Enter your name:"
read name
echo "Hello, $name!"
```


## Q.2 Create a shell script that checks if a file exists in the current directory.

```
terminal
touch ok.txt
nvim file.sh
chmod +x check_file.sh
./check_file.sh
```

```
shell script
#! /bin/bash 
echo "Enter the file name:" 
read file 
if [ -e "$file" ]; 
then 
echo "File exists." 
else 
echo "File does not exist." 
fi
```




## Q.3 Write a Shell Script for output a specified directory's size.

```
Terminal
chmod +x ok.sh
./ok.sh
```

```
Shell Script
#! /bin/bash
echo "Enter directory name:"
read directory
du -sh "$directory"
```
## Q.4 Write a Shell Bash Script for evaluating the status of a file/directory.


```
terminal
chmod +x check.sh
./check.sh
```

```
Shell Script
#! /bin/bash
echo "Enter file or directory name:"
read item
if [ -e "$item" ]; then
if [ -f "$item" ]; then
echo "$item is a file."
elif [ -d "$item" ]; then
echo "$item is a directory."
fi
else
echo "$item does not exist."
fi
```

## Q.5 Read 'n' and generate a pattern given below:

```
Terminal
chmod +x woo.sh
./woo.sh
```

```
Shell Script
#! /bin/bash
echo "Enter the number of lines:"
read n
i=1
while [ $i -le $n ]
do
j=1
while [ $j -le $i ]
do
echo -n "$j"
j=$(( j + 1 ))
done
echo ""
i=$(( i + 1 ))
done 
```
