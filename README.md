# Shell-Data-Processing

## To get .txt file from url
* Right click in the folder where you want to this project and click Open Powershell Window here as administrator
* The curl command used to get data from the URL and store in a file is ```curl "http://shakespeare.mit.edu/hamlet/full.html" -O yourdataname.txt```. Note: Do this using Powershell not bash

## To process data
* Open git bash 
* tr commad: ```tr ' ' '\12' < yourdataname.txt``` It will transform each space ' ' into a return character '\12' (aka ASCII line feed) [2]
* Pipe command: ```tr ' ' '\12' < yourdataname.txt | sort ``` It will send the results of one command as input into another command
* Sort command: ```tr ' ' '\12' < yourdataname.txt | sort ``It will sorted output to uniq -c to count
* Uinq command and -c : ```tr ' ' '\12' < yourdataname.txt | sort | uniq -c``` It  will filter out the repeated lines in a file and will pipe the sorted output to uniq -c to count
* n and r flag: ```tr ' ' '\12' < yourdataname.txt | sort | uniq -c | sort -nr``` It will send the output i.e unique words to sort with -nr flag. Where the numerical comparison is done with reversing results.
* Output(>) command:```'\12' < yourdataname.txt | sort | uniq -c | sort -nr > result.txt```It will redirect the output to result.txt

## Hint for bash command
* Up arrow key will show you the pervious command
* cd will help you to change directory 
* ls -a lists all files including hidden files
* ls -s sort by file size