# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT

<img width="1920" height="111" alt="image" src="https://github.com/user-attachments/assets/e39d2af1-e0f0-4045-8bf7-fe76f9abbc01" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT

<img width="1920" height="102" alt="image" src="https://github.com/user-attachments/assets/a702a25d-98b6-4c26-af3c-e1b0e5fc7746" />

Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="1920" height="105" alt="image" src="https://github.com/user-attachments/assets/15bb1747-b15c-4216-9564-d2cbd40882c8" />

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

<img width="1920" height="113" alt="image" src="https://github.com/user-attachments/assets/78fe1b85-5337-417a-8650-4ca0d7dcf18d" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

<img width="1920" height="131" alt="image" src="https://github.com/user-attachments/assets/fba7d1c3-bc09-4a43-859a-1626281bda45" />

Remove the file hello1.txt

## COMMAND AND OUTPUT

<img width="1920" height="105" alt="image" src="https://github.com/user-attachments/assets/bf5954f2-b245-4837-a84d-b4ab9d1882b9" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

<img width="1920" height="250" alt="image" src="https://github.com/user-attachments/assets/48fcd280-09d5-46cb-bfb7-62c0d5a4aa79" />

List out all the associated file extensions 

## COMMAND AND OUTPUT

<img width="1920" height="773" alt="image" src="https://github.com/user-attachments/assets/db82bc59-7e75-4f01-8cf2-0b72535cc13e" />

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

<img width="1920" height="210" alt="image" src="https://github.com/user-attachments/assets/4294a779-0a03-4632-b5ae-310078416395" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

# program

```
@echo off
set name=John
echo Hello, %name%
pause
```
## OUTPUT

<img width="1482" height="75" alt="image" src="https://github.com/user-attachments/assets/95bef936-12a9-4d56-bea5-171704341ff0" />

Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

# program 

```
@echo off

:START

set /p num=Enter a number: 

set /a rem=%num% %% 2

if %rem%==0 (
    echo The number is Even
) else (
    echo The number is Odd
)

set /p choice=Do you want to continue (Y/N)? 

if /I "%choice%"=="Y" goto START
if /I "%choice%"=="N" goto END

echo Invalid Input
goto START

:END
echo Thank You
pause
```

## OUTPUT

<img width="1482" height="212" alt="image" src="https://github.com/user-attachments/assets/2810e359-9b40-4167-9aea-672e18e6cd5a" />

Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.


# program

```
@echo off

for /L %%i in (1,1,5) do (
    echo Number: %%i
)

pause
```

## OUTPUT

<img width="1482" height="168" alt="image" src="https://github.com/user-attachments/assets/99500f60-05b2-42d5-9310-0fa60cdccf24" />

Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

# program 

```
@echo off

if exist sample.txt (
    echo sample.txt exists
) else (
    echo sample.txt does not exist
)

pause
```

## OUTPUT

<img width="1482" height="66" alt="image" src="https://github.com/user-attachments/assets/4e5406e3-a83b-43b4-89ae-2b9b31ba23ea" />

Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

# program

```
@echo off

:MENU
echo ====================
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
echo ====================

set /p choice=Enter your choice: 

if %choice%==1 goto HELLO
if %choice%==2 goto CREATE
if %choice%==3 goto EXIT

echo Invalid Choice
goto MENU

:HELLO
echo Hello, World!
pause
goto MENU

:CREATE
echo This is a new file > newfile.txt
echo File Created
pause
goto MENU

:EXIT
echo Goodbye
pause
exit
```

## OUTPUT

<img width="1483" height="204" alt="image" src="https://github.com/user-attachments/assets/8bfc036a-8782-40c8-bddf-c050f6d598b8" />

# RESULT:
The commands/batch files are executed successfully.

