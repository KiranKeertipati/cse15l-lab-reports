# Lab Report 5 #

## Part 1 - Debugging Scenario ##

### Orginal Post of Student on Edstem: ###
![EDSTEM1](edstem1.png)

![EDSTEM2](edstem2.png)

![EDSTEM3](edstem3.png)

### Response from a TA ###
Thanks for reaching out! I believe that the issue is with your bash script. Bash code usually requires specific puntuation and spacing, which is often easy to overlook. The assignment of your valiables is probably where you went wrong. Specifically on lines 1 and 2 in `script.sh`. I believe that your spacing is wrong for those lines. The code should instead be: `file1="$1"` and `file2="$2"` on lines 1 and 2 respectively. That is, you should remove any spaces around the `=`. Apart from this your code and command look fine. Ensure that you are in the right directly when you run the command after making the required changes. Please feel free to reach out if you are still having trouble running the command.


### The corrected code and correct output after trying what the TA suggested ###
