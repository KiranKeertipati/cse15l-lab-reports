# Lab Report 5 #

## Part 1 - Debugging Scenario ##

### Orginal Post of Student on Edstem: ###
![EDSTEM1](edstem1.png)

![EDSTEM2](edstem2.png)

![EDSTEM](edstem.png)

### Response from a TA ###
Thanks for reaching out! I believe that the issue is with your bash script. Bash code usually requires specific puntuation and spacing, which is often easy to overlook. The assignment of your valiables is probably where you went wrong. Specifically on lines 1 and 2 in `script.sh`. I believe that your spacing is wrong for those lines. The code should instead be: `file1="$1"` and `file2="$2"` on lines 1 and 2 respectively. That is, you should remove any spaces around the `=`. Apart from this your code and command look fine. Ensure that you are in the right directly when you run the command after making the required changes. Please feel free to reach out if you are still having trouble running the command.


### The corrected code and correct output after trying what the TA suggested ###

The image below shows the corrected code in `script.sh`, after removing the unnecessary spacing around the `=` sign:

![correctedcode](correctedcode.png)

The image below shows the command that was used to execute the code in `script.sh`:

![correctedcommand](correctedcommand.png)

The image below shows the actual expected output with the corrected code. This `combined.txt` file now contains all the contents of the files `chapter-1.txt` and `chapter-2.txt` which are present in `stringsearch-data/technical/911report`:

![correctedoutput](correctedoutput.png)

**The clear decription of the bug:** 
The bug was a mistake in the code written in `script.sh`. The code initially did not follow the syntax that is required for bash. The error was specifically on lines 1 and 2 when the student was trying to create the variables `file1` and `file2`. The student initially has the following code: `file1 = "$1"` amd `file2 = "$2` which is incorrect because there is extra spacing around the equal sign. This is what causes the error. The variables were hence never properly assigned and the code was wrong hence the student got the error that the files could not be found and that the command was wrong. But after fixing this bug to now have the code read `file1=$1` and `file2=$2` the errors no longer showed up in the terminal and the concatinated/combined contents of the two files was found in `combined.txt`.

### Information needed for the setup: ###

**The file & directory structure needed**

**The contents of each file before fixing the bug**

**The full command line (or lines) you ran to trigger the bug**

**A description of what to edit to fix the bug**

