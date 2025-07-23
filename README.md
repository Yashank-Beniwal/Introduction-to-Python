# Introduction-to-Python
SANS BACS - 3373 final assignments

## Assignment 1 - Zip Password Cracker

### Situation Brief
After your companies head sales person left his position you discover that he used password protected zip files to store all the company spreadsheets containing critical contacts information and account numbers. You have been told by one of his co-workers that his password was the digits of a phone number, but you don't know what phone number. It could be any digit valid phone number in the format 1800555xxxx where xxxx is any digit between 0 and 9. You have been asked to write a tool to determine the password.

### Tool Requirements
You must develop a tool called "zip_crack.py". It will take one argument which will be the complete path to a password protected zip file. To determine the correct password you can repeatedly execute the "unzip" command which is in the same directory as this file and pass password attempts.

### Code 
https://github.com/Yashank-Beniwal/Introduction-to-Python/blob/main/Assignment%201%20-%20Zip%20Password%20Cracker

## Assignment 2 - Forensics Investigation

In your second assignment your company is concerned that someone is leaking important intellectual property. As a safeguard you have been given the md5 has of the intellectual property and you must scan file locations to identify any files that match that hash. You will develop a new tool to automate this search.

### Situation Brief

Your organization maintains highly valued intellectual property. Over the last few months company leaders have grown suspicious that someone is collecting and celling intellectual property to your competitors. You have been asked to write a tool to search drives and identify the presence of specific intellectual property.

### Tool Requirements

You must develop a tool called "hash_search.py". The file that will contain your code has already been created in this folder. The tool must accept exactly two command line arguments.

- HASH: The first command line argument is an MD5 Hash of a file you want to search for.
- PATH: The second command line argument is the directory you must search.

Your tool will read the command line arguments that are passed to it and stored in the variable sys.argv. The MD5sum will be in sys.argv[1]. It will be referred to as "HASH" in this document. The path to search will be in sys.argv[2] and will be referred to as "PATH" in this document. You must open every file in PATH and calculate its MD5 ".hexdigest()" on the contents of the file using the "hashlib" module. The .hexdigest() method returns a string you will compare that to the HASH in the first command line argument. When you find whose calculated MD5 hexdigest that matches the HASH from the command line you will print the name of the file.

### Code
https://github.com/Yashank-Beniwal/Introduction-to-Python/blob/main/Assignment%202%20-%20Forensics%20Investigation

## Assignment 3 - Log Analyzer

In your third assignment, you will develop a tool to analyze a log file and identify the attackers' IP Address. You are given a series of log files from an internal application. You will write a tool to analyze the logs and generate reports based on different thresholds of sensitivity.

### Situation Brief
After analyzing the same log file every day looking for signs of attackers you realize the truth, that manually analyzing log files is time consuming and are less accurate then that writing a tool to do it manually. To that end you are writing a tool to analyze the authentication logs of a server that is running on your internal network.

### Tool Requirements
You must develop a tool called "analyze_log.py". It will take the following two command line arguments:

- PATH: The first command line argument is the path to the log file you are going to analyze.
- THRESHOLD: The second command line argument is an integer.

If an IP Address appear on a line in the log in argument PATH along with the string "LOGIN FAILED" then you will count count it. Any IP Address that appears in the log file more than the integer THRESHOLD you will print.

### Code
https://github.com/Yashank-Beniwal/Introduction-to-Python/blob/main/Assignment%203%20-%20Log%20Analyzer
