# Day 4 Task: Basic Linux Shell Scripting.

## What is Kernel

A kernel is the core component of an operating system that serves as a bridge between the hardware and software. It is responsible for managing system resources, such as CPU, memory, and input/output devices, and providing essential services to software applications.

## What is Shell

A program that interprets the commands you type in your terminal and pass them to the O.S. Shell accept human readable commands from user and convert them into something which kernel can understand.
Besides Bourne shell, there are other shell programs that can be installed in a Linux system. These include Korn Shell (ksh), Boune Again Shell (bash), and C Shell (csh).

## What is Linux Shell Scripting?

A shell script is a file containing series of command for the shell.
Exit from script we use zero means task completed successfully. any non-zero exit code tell the script that task is unsuccessful.
The exit code range is 0 to 255.

## structure of bash script

#!bin/bash

        #Author : Author_name
        #Date created
        #Last modified

        #Description
        #Print "my script"

        #usage
        #Script_name

        exit 0

## What is `#!/bin/bash?` can we write `#!/bin/sh` as well ?

The #!/bin/bash and #!/bin/sh lines are called shebangs, and they are used in Unix-like operating systems to specify the interpreter for a script or shell program.

## #!/bin/bash:

This line tells the system to use the Bash shell as the interpreter for the script. Bash is a popular and powerful Unix shell that provides a wide range of features for scripting and command-line tasks.

## #!/bin/sh:

This line specifies the system to use the default system shell as the interpreter. The default shell may vary from one Unix-like system to another.

## Write a Shell Script which prints `I will complete #90DaysOofDevOps challenge`

#!bin/bash

        #Author : Author_name
        #Date created
        #Last modified

        #Description
        #Print "my script"

        #usage
        #Script_name   devops.txt

        echo " I will complete #90DaysofDevOps Challenge"
        exit 0

## Write a Shell Script to take user input, input from arguments and print the variables.

#!/bin/bash

# Taking user input

read -p "Enter a value: " user_input

# Print the variables

echo "User input: $user_input"

exit 0

Run the script --> chmod +x myscript.sh change the permission.
./myscript.sh

## Write an Example of If else in Shell Scripting by comparing 2 numbers

#!/bin/bash

# Define two numbers

number1=10
number2=20

# Compare the numbers

if [ $number1 -gt $number2 ]; then
echo "$number1 is greater than $number2"
elif [ $number1 -lt $number2 ]; then
  echo "$number1 is less than $number2"
else
  echo "$number1 is equal to $number2"
fi

exit 0
