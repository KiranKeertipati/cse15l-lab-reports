# Lab Report 3 #

### Researching Commands #
Out of the three commands we had to pick: `less`, `find`, and `grep`, and I chose the `grep` command.

## The `grep` Command: #

This is the link I used to research the different ways to implement the `grep` command: `https://www.geeksforgeeks.org/grep-command-in-unixlinux/`. I types out grep command line operations in my google browser and this was one of the links I got. All the commands that I used in this report were from this link. This is the hyperlinked version of the link to the website I used for this lab report: [LinkToResource](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

## The 4 Command-line options: #
I used all of these variations of the `grep` command on the files and directories from `./technical`.


This is the normal `grep` command which finds all the lines with `Our` in `preface.txt`. I chose to include the normal `grep` command to showcase the difference when we use the other variations:
```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep "Our"  technical/911report/preface.txt
```
The following was the output of the above command:
```
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
            Our aim has not been to assign individual blame. Our aim has been to provide the
```
--------

### 1. `grep -i` command:

- **Example 1:**

This command bellow is the normal `grep`command that tries finds all the lines in `preface.txt` which match with the string `OuR`, but since there are no lines with the specific `OuR` string, it has no output:
```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep "OuR" technical/911report/preface.txt
```
Now, when we use the `grep -i` command before `OuR`, this changes the command to now ignore the case (upper/lower case) of the string/word we are searching for. Hence now the command searches for the letters o,u,r strung together in any case within the file `preface.txt`. Below is the command the resulting output:

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep -i "OuR" technical/911report/preface.txt
                Democrats chosen by elected leaders from our nation's capital at a time of great
            We have come together with a unity of purpose because our nation demands it.
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
                aviation, the role of congressional oversight and resource allocation, and other
                areas determined relevant by the Commission. In pursuing our mandate, we have
                our mandate. We have sought to be independent, impartial, thorough, and nonpartisan.
                From the outset, we have been committed to share as much of our investigation as we
            Our aim has not been to assign individual blame. Our aim has been to provide the
                political grievances, but its hostility toward us and our values is limitless. Its
            We learned that the institutions charged with protecting our borders, civil aviation,
                fault lines within our government-between foreign and domestic intelligence, and
            At the outset of our work, we said we were looking backward in order to look forward.
                the same time protecting our country against future attacks. We have been forced to
                think about the way our government is organized. The massive departments and
            As we complete our final report, we want to begin by thanking our fellow
                dialogue. We want to express our considerable respect for the intellect and judgment
                of our colleagues, as well as our great affection for them.
                Philip Zelikow, has contributed innumerable hours to the completion of this report,
                built. They have given good advice, and faithfully carried out our guidance. They
                the sources we have consulted. But in an event of this scale, touching so many
                issues and organizations, we are conscious of our limits. We have not interviewed
                understanding of a landmark in the history of our nation.
                the American people and their amazing resilience and courage as they fought back. We
                pause, reflect, and sometimes change our minds as we studied these problems and
                considered the views of others. We hope our report will encourage our fellow
```
- **Example 2:**

The following is another command I used. The command matches `waTER` regardless of the case of the letters and the output is all the lines in `water_fees.txt` that match this requirement. Hence the output is all the lines with `water` or even `Water`.

 ```
 kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep -i "waTER"  technical/government/Media/water_fees.txt
Alpaugh water fees may triple
Alpaugh residents may see their water fees triple to avoid
The debate will unfold tonight at a Tulare County Water Works
District 1 meeting. The district, which provides water service to
water.
Tulare County Water Works' contract with its only supplier,
Alpaugh Irrigation District, which supplies water to farmers in the
area, ends July 1. And Alpaugh Irrigation, which provides water,
recordkeeping and maintenance services to Tulare County Water
Works, is scaling back its role. The district will sell only water
fast enough to meet the rising cost of delivering water, amassed an
If Tulare County Water Works wants to keep its 170 hookups
Tulare County Water Works can't raise prices until a July 17
under Proposition 218, a process Tulare County Water Works
At tonight's Tulare County Water Works' informational meeting,
County Water Works board president, interrupted an interview
The farmworker thought the water was getting turned off today,
Tulare County Water Works may also come under Schneider's
yet sure whether Tulare County Water Works will accept renters'
```
**What `grep -i` does and why it could be useful:**

The `grep -i` command matches the lines in the file with the string provided in the command regardess of the case of the letters in the string. This is helpful if we want to find all lines containing the word in a file regardless of whether the word is capitalized or not. This way we can get the accurate lines that match with the string provided without having to use grep multiple times to check any variations in the case of the letters in the string.

--------

### 2. `grep -c` command:
This command counts the number of lines in the file that match with the string provided in the command line.

- **Example 1:**

The following is an example of using the `grep -c` command to count the number of lines `Our` occurs in the file `preface.txt`. I produces the output 2, because there are two lines in `preface.txt` that match the given string ` Our`. The following is the command I used and the resulting output:

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep -c "Our" technical/911report/preface.txt
2
```
- **Example 2:**

This example counts the number of lines the string `disaster` matches with in the file `Disaster_center.txt`. The code block bellow shows the command I used and the output, from which one can understand that there are 5 lines which have `disaster` in them in the file `Disaster_center.txt`.

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep -c "disaster" technical/government/Media/Disaster_center.txt
5
```
**What `grep -c` does and why it could be useful:**

The `grep -c` command can be used to count the number of lines in which the given string/word occurs in the specified file. This could be useful if we what to just count how many times a word occurs in a very large file. And if we would want a number to show the ammount of occurances rather than printing out all the lines of occurance in such a large file. This would serve to be more consize rather than using the grep command and manually counting the number of times the string matched.

--------

### 3. `grep -n` command:

This command includes the lines that match with the given string and it also includes the line number of the lines in the specified file. When the line matches it displays the line number also in the output.

- **Example 1:**

The following example uses the `grep -n` command to check the matches of the string `Our` in the file `preface.txt`. This results in the output having the lines which contain the string `Our`, anong with their respective line numbers. The following code block is the command and the output that was displayed by it:

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep -n "Our" technical/911report/preface.txt
17:            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
30:            Our aim has not been to assign individual blame. Our aim has been to provide the
```
- **Example 2:**

The following example uses `grep -n` to output the lines along with the lines numbers which match with the string `residents` in the file `residents_sue_city.txt`. The following code block shows the command that I passed in the output with the line numbers and the lines that match displayed:

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep -n "residents" technical/government/Media/residents_sue_city.txt
5:Mobile home residents sue city for loss, moving costs
8:Residents and former residents of a Lincoln Place mobile home
12:On Friday, a group of residents filed a lawsuit against
26:Raimondi has been evicting residents and demolishing trailers
42:lawsuit. He said the city still maintains that the residents of the
```

**What `grep -n` does and why it could be useful:**

The `grep -n` command can be used to get both the line numbers and the lines that match the string in the command line, displayed in the output. This could be helpful to later find which exact lines match the string. Instead of searching through the entire file for these particular lines, now with the line numbers we could easily identify which line matches in the file. This could help if the user wanted to check if which lines in the files contain a particular word, and then later wanted to get more context and would re-check the lines from the file itself. Knowing the line numbers for such situations could prove to be useful, since it provides the user more information about the lines that match and hence the user can easily pick them up from the file itself.

--------

### 4. `grep -v` command:
This command displays all the lines that do not match/contain the string/word from the command line. When we want all the lines that do not match with a specific string.

- **Example1:**

This example tries to find all the lines in `preface.txt` that do not contain the string `our`. Hence all the lines apart from the lines having the string `our` are displayed as the output for this particular command line. The block code below shows the command line and the resulting output:

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep -v "our" technical/911report/preface.txt

    
        
            PREFACE
            We present the narrative of this report and the recommendations that flow from it to
                the President of the United States, the United States Congress, and the American
                people for their consideration. Ten Commissioners-five Republicans and five
                partisan division-have come together to present this report without dissent.
                September 11, 2001, was a day of unprecedented shock and suffering in the history of
                the United States. The nation was unprepared. How did this happen, and how can we
                avoid such tragedy again?
            To answer these questions, the Congress and the President created the National
                Commission on Terrorist Attacks Upon the United States (Public Law 107-306, November
                27, 2002).
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
                relating to the terrorist attacks of September 11, 2001," including those relating
                to intelligence agencies, law enforcement agencies, diplomacy, immigration issues
                and border control, the flow of assets to terrorist organizations, commercial
                reviewed more than 2.5 million pages of documents and interviewed more than 1,200
                individuals in ten countries. This included nearly every senior official from the
                current and previous administrations who had responsibility for topics covered in
                can with the American people. To that end, we held 19 days of hearings and took
                public testimony from 160 witnesses.
            Our aim has not been to assign individual blame. Our aim has been to provide the
                fullest possible account of the events surrounding 9/11 and to identify lessons
                learned.
            We learned about an enemy who is sophisticated, patient, disciplined, and lethal. The
                enemy rallies broad support in the Arab and Muslim world by demanding redress of
                purpose is to rid the world of religious and political pluralism, the plebiscite,
                and equal rights for women. It makes no distinction between military and civilian
                targets. Collateral damage is not in its lexicon.
                and national security did not understand how grave this threat could be, and did not
                adjust their policies, plans, and practices to deter or defeat it. We learned of
                between and within agencies. We learned of the pervasive problems of managing and
                sharing information across a large and unwieldy government that had been built in a
                different era to confront different dangers.
                We hope that the terrible losses chronicled in this report can create something
                positive-an America that is safer, stronger, and wiser. That September day, we came
                together as a nation. The test before us is to sustain that unity of purpose and
                meet the challenges now confronting us. We need to design a balanced strategy for
                the long haul, to attack terrorists and prevent their ranks from swelling while at
                agencies that prevailed in the great struggles of the twentieth century must work
                together in new ways, so that all the instruments of national power can be combined.
                Congress needs dramatic change as well to strengthen oversight and focus
                accountability.
                Commissioners, whose dedication to this task has been profound. We have reasoned
                together over every page, and the report has benefited from this remarkable
            We want to thank the Commission staff. The dedicated professional staff, headed by
                setting aside other important endeavors to take on this all-consuming assignment.
                They have conducted the exacting investigative work upon which the Commission has
                have been superb. We thank the Congress and the President. Executive branch agencies
                have searched records and produced a multitude of documents for us. We thank
                officials, past and present, who were generous with their time and provided us with
                insight. The PENTTBOM team at the FBI, the Director's Review Group at the CIA, and
                Inspectors General at the Department of Justice and the CIA provided great
                assistance. We owe a huge debt to their investigative labors, painstaking attention
                to detail, and readiness to share what they have learned. We have built on the work
                of several previous Commissions, and we thank the Congressional Joint Inquiry, whose
                fine work helped us get started. We thank the City of New York for assistance with
                documents and witnesses, and the Government Printing Office and W.W. Norton
                & Company for helping to get this report to the broad public.
            We conclude this list of thanks by coming full circle: We thank the families of 9/11,
                whose persistence and dedication helped create the Commission. They have been with
                us each step of the way, as partners and witnesses. They know better than any of us
                the importance of the work we have undertaken.
            We want to note what we have done, and not done. We have endeavored to provide the
                most complete account we can of the events of September 11, what happened and why.
                This final report is only a summary of what we have done, citing only a fraction of
                every knowledgeable person or found every relevant piece of paper. New information
                inevitably will come to light. We present this report as a foundation for a better
            We have listened to scores of overwhelming personal tragedies and astounding acts of
                heroism and bravery. We have examined the staggering impact of the events of 9/11 on
                have admired their determination to do their best to prevent another tragedy while
                preparing to respond if it becomes necessary. We emerge from this investigation with
                enormous sympathy for the victims and their loved ones, and with enhanced respect
                for the American people. We recognize the formidable challenges that lie ahead.
            We also approach the task of recommendations with humility. We have made a limited
                number of them. We decided consciously to focus on recommendations we believe to be
                most important, whose implementation can make the greatest difference. We came into
                this process with strong opinions about what would work. All of us have had to
                citizens to study, reflect-and act.
            Thomas H. Kean, chair
            Lee H. Hamilton, vice chair
            
```

- **Example2:**

This example displays all the lines in `water_fees.txt` that do not contain the first letter capatilized string `Water`. This would be useful if we wanted to find all the lines that do not have the word 'water' with a capital 'w'. The following block code contains the command line and the output that it displays:

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep -v "Water" technical/government/Media/water_fees.txt




Alpaugh water fees may triple

It's either a big increase or a loss of service for the Tulare
County town.
By Joan Obra
Alpaugh residents may see their water fees triple to avoid
losing service at the end of the month.
District 1 meeting. The district, which provides water service to
homes in Alpaugh, faces an unpalatable choice: raise its monthly
$20 household fee or go without the arsenic-tainted and undrinkable
water.
Alpaugh Irrigation District, which supplies water to farmers in the
area, ends July 1. And Alpaugh Irrigation, which provides water,
Works, is scaling back its role. The district will sell only water
as of July 1, at a monthly price of $43.50 for a household.
"We can no longer do it for $20," said Alpaugh Irrigation board
president Steve Martin. The district, which didn't increase prices
fast enough to meet the rising cost of delivering water, amassed an
estimated $330,000 power bill during the state energy crisis. Last
month, Alpaugh Irrigation customers approved a monthly fee increase
from $20 to $68.
flowing, Martin said, it must also raise rates.
election. The propertyrelated fee increase requires voter approval
officials started after they learned the outcome of Alpaugh
Irrigation's vote.
leaders will explain the rules. To block the possible fee increase,
51% of property owners in the district must submit protest votes in
writing. No protest vote means approval of the price jump.
But misinformation already is rampant. Sandra Meraz, Tulare
Tuesday when a screaming and crying farmworker arrived.
The farmworker thought the water was getting turned off today,
Meraz explained later.
Part of the confusion stems from Prop. 218. A section of it
calls eligible voters "owners of record." Another calls them
"tenants ... directly liable to pay the assessment, fee, or charge
in question."
Alpaugh Irrigation's board limited the voter pool to property
owners, sending each English-only notices.
There weren't enough Spanish-speaking voters to warrant
bilingual notices, Martin explained in May.
But that move left Spanish speakers and renters angry. As a
result, Chris Schneider, executive director of Central California
Legal Services, is building a lawsuit against Alpaugh
Irrigation.
The district "should have sent notices to renters in addition to
property owners," he said.
fire.
The district sent notices only to property owners because "it's
a property-related fee," attorney Patrick Enright said. He's not
protest votes at the July 17 meeting

```


**What `grep -v` does and why it could be useful:**

The `grep -v` command can be used to get all the lines in a particular file that do not contain a particular string/word. This could be useful if you want to ensure that a string is not repeated in almost all the lines of the file. Or, this command could have use if the user would like to examine the lines that do not contain the string for extra context or for information about the file that does not directly relate to that particular string/word.
