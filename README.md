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
```
mkdir wick
```

<img width="463" height="27" alt="Screenshot 2026-09-09 104733" src="https://github.com/user-attachments/assets/2ba73f37-a1ea-4782-9b43-e76b2d2d8713" />



## COMMAND AND OUTPUT

Remove the directory "my-folder"
```
rmdir wick
```

<img width="447" height="27" alt="Screenshot 2026-09-09 104740" src="https://github.com/user-attachments/assets/689953ce-904a-47d9-8e94-0834dc5f4f3b" />


## COMMAND AND OUTPUT


Create the file Rose.txt
```
type nul > rose.txt
```

<img width="587" height="43" alt="Screenshot 2026-09-09 104821" src="https://github.com/user-attachments/assets/b1ee7319-5bd6-4314-8481-9841749aa042" />

## COMMAND AND OUTPUT

Create the file hello.txt using echo and redirection
```
echo Hello World > hello.txt
```
<img width="687" height="33" alt="Screenshot 2026-09-09 104841" src="https://github.com/user-attachments/assets/20e976e0-c4ff-40cb-be49-6b1b43ff641e" />


## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt
```
copy hello.txt hello1.txt
```
<img width="658" height="55" alt="Screenshot 2026-09-09 104906" src="https://github.com/user-attachments/assets/aea9611f-5688-47e1-af51-1aee4e729006" />


## COMMAND AND OUTPUT

Remove the file hello1.txt
## COMMAND AND OUTPUT

Compare the file hello.txt and rose.txt
```
fc hello.txt rose.txt
```


<img width="597" height="156" alt="Screenshot 2026-09-09 105039" src="https://github.com/user-attachments/assets/889436d0-caf7-4e77-8bea-d58fc6490bf6" />


## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".


```
@echo off
set name=John
echo Hello, %name%
pause
```


## OUTPUT

<img width="1298" height="345" alt="image" src="https://github.com/user-attachments/assets/f8cfe47a-f9fa-46ee-ab6c-b77921f0294b" />

Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
@echo off
:START
set /p num=Enter a number: 

set /a rem=%num% %% 2

if %rem%==1 (
    echo The number %num% is ODD
) else (
    echo The number %num% is NOT ODD
)

:CHOICE
set /p choice=Do you want to check another number? (Y/N): 

if /I "%choice%"=="Y" goto START
if /I "%choice%"=="N" goto END

echo Invalid choice. Please enter Y or N.
goto CHOICE
:END
echo Thank you!
pause
```


## OUTPUT

<img width="1476" height="471" alt="image" src="https://github.com/user-attachments/assets/b978e23b-d420-466a-9e26-92874c550038" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
```

<img width="1472" height="397" alt="image" src="https://github.com/user-attachments/assets/1df85c09-1d59-47f0-ab71-40ee939c8e2a" />

Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

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

<img width="1702" height="60" alt="image" src="https://github.com/user-attachments/assets/2dd081ce-3f38-4a49-9910-7166829a8343" />



Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

```
@echo off
:MENU
cls
echo ===== MENU =====
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
echo =================
set /p choice=Enter your choice: 

if "%choice%"=="1" goto HELLO
if "%choice%"=="2" goto CREATE
if "%choice%"=="3" goto EXIT

echo Invalid choice!
pause
goto MENU

:HELLO
echo Hello, World!
pause
goto MENU

:CREATE
echo This is a new file > newfile.txt
echo File created successfully!
pause
goto MENU
:EXIT
echo Goodbye!
pause
exit
```

## OUTPUT 1
<img width="1919" height="212" alt="image" src="https://github.com/user-attachments/assets/d0bc2301-a74f-4a04-ad81-dfe661c3af7d" />

## OUTPUT 2
<img width="1919" height="231" alt="image" src="https://github.com/user-attachments/assets/307433b5-fe2d-4f39-95e0-cd0b48a406a4" />

## OUTPUT 3
<img width="1919" height="213" alt="image" src="https://github.com/user-attachments/assets/001129c8-c70d-40ef-a847-36cb893bcb99" />



# RESULT:
The commands/batch files are executed successfully.

