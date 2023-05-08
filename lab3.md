# Lab Report 3 #

## Researching Commands #
Out of the three commands we had to pick: `less`, `find`, and `grep`, I choose the `find` command.

### `grep` command: #

This command finds all the lines with Our in preface.txt
```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep "Our"  technical/911report/preface.txt
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
            Our aim has not been to assign individual blame. Our aim has been to provide the
```

This command finds all the lines with OuR, but since there are no lines with it, it prints nothing:
```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep "OuR" technical/911report/preface.txt
```
Now, the -i before OuR, changes the command to now ignore the case of the string/word we are searching for, hence it searches for the letter o,u,r strung together in any case within the file preface.txt
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
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % 
```

This counts the number of matches in the file: (-c)
```kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep -c "Our" technical/911report/preface.txt
2
```

This considers the string given as the entire word and doesnt match it if it is just part of a word (-w)

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep -w "an" technical/911report/preface.txt
            We learned about an enemy who is sophisticated, patient, disciplined, and lethal. The
                positive-an America that is safer, stronger, and wiser. That September day, we came
                the sources we have consulted. But in an event of this scale, touching so many
```
This is searching for an with the -w so it only counts the words

But below is if we dont use -w
```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % grep "an" technical/911report/preface.txt
            We present the narrative of this report and the recommendations that flow from it to
                the President of the United States, the United States Congress, and the American
                people for their consideration. Ten Commissioners-five Republicans and five
                partisan division-have come together to present this report without dissent.
            We have come together with a unity of purpose because our nation demands it.
                September 11, 2001, was a day of unprecedented shock and suffering in the history of
                the United States. The nation was unprepared. How did this happen, and how can we
            To answer these questions, the Congress and the President created the National
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
                and border control, the flow of assets to terrorist organizations, commercial
                aviation, the role of congressional oversight and resource allocation, and other
                areas determined relevant by the Commission. In pursuing our mandate, we have
                reviewed more than 2.5 million pages of documents and interviewed more than 1,200
                current and previous administrations who had responsibility for topics covered in
                our mandate. We have sought to be independent, impartial, thorough, and nonpartisan.
                can with the American people. To that end, we held 19 days of hearings and took
                fullest possible account of the events surrounding 9/11 and to identify lessons
            We learned about an enemy who is sophisticated, patient, disciplined, and lethal. The
                enemy rallies broad support in the Arab and Muslim world by demanding redress of
                political grievances, but its hostility toward us and our values is limitless. Its
                purpose is to rid the world of religious and political pluralism, the plebiscite,
                and equal rights for women. It makes no distinction between military and civilian
                and national security did not understand how grave this threat could be, and did not
                adjust their policies, plans, and practices to deter or defeat it. We learned of
                fault lines within our government-between foreign and domestic intelligence, and
                between and within agencies. We learned of the pervasive problems of managing and
                sharing information across a large and unwieldy government that had been built in a
                different era to confront different dangers.
                We hope that the terrible losses chronicled in this report can create something
                positive-an America that is safer, stronger, and wiser. That September day, we came
                together as a nation. The test before us is to sustain that unity of purpose and
                meet the challenges now confronting us. We need to design a balanced strategy for
                the long haul, to attack terrorists and prevent their ranks from swelling while at
                think about the way our government is organized. The massive departments and
                together in new ways, so that all the instruments of national power can be combined.
                Congress needs dramatic change as well to strengthen oversight and focus
            As we complete our final report, we want to begin by thanking our fellow
                together over every page, and the report has benefited from this remarkable
                dialogue. We want to express our considerable respect for the intellect and judgment
            We want to thank the Commission staff. The dedicated professional staff, headed by
                setting aside other important endeavors to take on this all-consuming assignment.
                built. They have given good advice, and faithfully carried out our guidance. They
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
                the sources we have consulted. But in an event of this scale, touching so many
                issues and organizations, we are conscious of our limits. We have not interviewed
                every knowledgeable person or found every relevant piece of paper. New information
                understanding of a landmark in the history of our nation.
            We have listened to scores of overwhelming personal tragedies and astounding acts of
                heroism and bravery. We have examined the staggering impact of the events of 9/11 on
                the American people and their amazing resilience and courage as they fought back. We
                have admired their determination to do their best to prevent another tragedy while
                enormous sympathy for the victims and their loved ones, and with enhanced respect
                for the American people. We recognize the formidable challenges that lie ahead.
                most important, whose implementation can make the greatest difference. We came into
                pause, reflect, and sometimes change our minds as we studied these problems and
                citizens to study, reflect-and act.
            Thomas H. Kean, chair
            
  ```


### `Find` command: #

This is the link I used to research the different ways to implement the `find` command: `https://www.redhat.com/sysadmin/linux-find-command` This is the hyperlinked version of the link of the website that I used for this lab report: [LinkToResource](https://www.redhat.com/sysadmin/linux-find-command)



find:
```
kirankeertipati@Kirans-MacBook-Pro stringsearch % find stringsearch-data/technical/911report
stringsearch-data/technical/911report
stringsearch-data/technical/911report/chapter-13.4.txt
stringsearch-data/technical/911report/chapter-13.5.txt
stringsearch-data/technical/911report/chapter-13.1.txt
stringsearch-data/technical/911report/chapter-13.2.txt
stringsearch-data/technical/911report/chapter-13.3.txt
stringsearch-data/technical/911report/chapter-3.txt
stringsearch-data/technical/911report/chapter-2.txt
stringsearch-data/technical/911report/chapter-1.txt
stringsearch-data/technical/911report/chapter-5.txt
stringsearch-data/technical/911report/chapter-6.txt
stringsearch-data/technical/911report/chapter-7.txt
stringsearch-data/technical/911report/chapter-9.txt
stringsearch-data/technical/911report/chapter-8.txt
stringsearch-data/technical/911report/preface.txt
stringsearch-data/technical/911report/chapter-12.txt
stringsearch-data/technical/911report/chapter-10.txt
stringsearch-data/technical/911report/chapter-11.txt
kirankeertipati@Kirans-MacBook-Pro stringsearch %
```

find -name:

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % find technical/911report -name
 "chapter*.txt"
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-3.txt
technical/911report/chapter-2.txt
technical/911report/chapter-1.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/911report/chapter-8.txt
technical/911report/chapter-12.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
```

find -iname: (finds a single file by approximate name)
(finds files using name and ignoring case(t and T)
```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % find technical/911report -inam
e "*apter*txt"
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-3.txt
technical/911report/chapter-2.txt
technical/911report/chapter-1.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/911report/chapter-8.txt
technical/911report/chapter-12.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
```

find everything (find the file and whatever is in it also):
```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % find technical/government -ls
13782724        0 drwxr-xr-x    8 kirankeertipati  staff                 256 May  7 11:14 technical/government
13782725        0 drwxr-xr-x   19 kirankeertipati  staff                 608 May  7 11:14 technical/government/About_LSC
13782730       16 -rwxr-xr-x    1 kirankeertipati  staff                7083 May  7 11:14 technical/government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
13782733       96 -rwxr-xr-x    1 kirankeertipati  staff               47991 May  7 11:14 technical/government/About_LSC/Progress_report.txt
13782738      136 -rwxr-xr-x    1 kirankeertipati  staff               67527 May  7 11:14 technical/government/About_LSC/Strategic_report.txt
13782727       40 -rwxr-xr-x    1 kirankeertipati  staff               20130 May  7 11:14 technical/government/About_LSC/Comments_on_semiannual.txt
13782735       88 -rwxr-xr-x    1 kirankeertipati  staff               41409 May  7 11:14 technical/government/About_LSC/Special_report_to_congress.txt
13782726       32 -rwxr-xr-x    1 kirankeertipati  staff               13558 May  7 11:14 technical/government/About_LSC/CONFIG_STANDARDS.txt
13782739      440 -rwxr-xr-x    1 kirankeertipati  staff              223414 May  7 11:14 technical/government/About_LSC/commission_report.txt
13782728       56 -rwxr-xr-x    1 kirankeertipati  staff               28121 May  7 11:14 technical/government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
13782732       72 -rwxr-xr-x    1 kirankeertipati  staff               34008 May  7 11:14 technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt
13782729       56 -rwxr-xr-x    1 kirankeertipati  staff               27109 May  7 11:14 technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt
13782741       48 -rwxr-xr-x    1 kirankeertipati  staff               23451 May  7 11:14 technical/government/About_LSC/diversity_priorities.txt
13782742       40 -rwxr-xr-x    1 kirankeertipati  staff               17770 May  7 11:14 technical/government/About_LSC/reporting_system.txt
13782736      304 -rwxr-xr-x    1 kirankeertipati  staff              152067 May  7 11:14 technical/government/About_LSC/State_Planning_Report.txt
13782734       32 -rwxr-xr-x    1 kirankeertipati  staff               13682 May  7 11:14 technical/government/About_LSC/Protocol_Regarding_Access.txt
13782731       16 -rwxr-xr-x    1 kirankeertipati  staff                6118 May  7 11:14 technical/government/About_LSC/ODonnell_et_al_v_LSCdecision.txt
13782740       32 -rwxr-xr-x    1 kirankeertipati  staff               13828 May  7 11:14 technical/government/About_LSC/conference_highlights.txt
13782737       64 -rwxr-xr-x    1 kirankeertipati  staff               29963 May  7 11:14 technical/government/About_LSC/State_Planning_Special_Report.txt
13782748        0 drwxr-xr-x   16 kirankeertipati  staff                 512 May  7 11:14 technical/government/Env_Prot_Agen
13782757      384 -rwxr-xr-x    1 kirankeertipati  staff              195851 May  7 11:14 technical/government/Env_Prot_Agen/multi102902.txt
13782760      104 -rwxr-xr-x    1 kirankeertipati  staff               52552 May  7 11:14 technical/government/Env_Prot_Agen/section-by-section_summary.txt
13782756      128 -rwxr-xr-x    1 kirankeertipati  staff               62387 May  7 11:14 technical/government/Env_Prot_Agen/jeffordslieberm.txt
13782755       72 -rwxr-xr-x    1 kirankeertipati  staff               32919 May  7 11:14 technical/government/Env_Prot_Agen/final.txt
13782753      160 -rwxr-xr-x    1 kirankeertipati  staff               77895 May  7 11:14 technical/government/Env_Prot_Agen/ctf7-10.txt
13782752      152 -rwxr-xr-x    1 kirankeertipati  staff               73979 May  7 11:14 technical/government/Env_Prot_Agen/ctf1-6.txt
13782759       40 -rwxr-xr-x    1 kirankeertipati  staff               19798 May  7 11:14 technical/government/Env_Prot_Agen/ro_clear_skies_book.txt
13782754      264 -rwxr-xr-x    1 kirankeertipati  staff              131959 May  7 11:14 technical/government/Env_Prot_Agen/ctm4-10.txt
13782749       40 -rwxr-xr-x    1 kirankeertipati  staff               19836 May  7 11:14 technical/government/Env_Prot_Agen/1-3_meth_901.txt
13782750      144 -rwxr-xr-x    1 kirankeertipati  staff               72635 May  7 11:14 technical/government/Env_Prot_Agen/atx1-6.txt
13782762       32 -rwxr-xr-x    1 kirankeertipati  staff               13279 May  7 11:14 technical/government/Env_Prot_Agen/tech_sectiong.txt
13782751      480 -rwxr-xr-x    1 kirankeertipati  staff              243860 May  7 11:14 technical/government/Env_Prot_Agen/bill.txt
13782758       64 -rwxr-xr-x    1 kirankeertipati  staff               31404 May  7 11:14 technical/government/Env_Prot_Agen/nov1.txt
13782761      352 -rwxr-xr-x    1 kirankeertipati  staff              178501 May  7 11:14 technical/government/Env_Prot_Agen/tech_adden.txt
13782743        0 drwxr-xr-x    6 kirankeertipati  staff                 192 May  7 11:14 technical/government/Alcohol_Problems
13782745       72 -rwxr-xr-x    1 kirankeertipati  staff               35927 May  7 11:14 technical/government/Alcohol_Problems/Session2-PDF.txt
13782746      192 -rwxr-xr-x    1 kirankeertipati  staff               94212 May  7 11:14 technical/government/Alcohol_Problems/Session3-PDF.txt
13782744       64 -rwxr-xr-x    1 kirankeertipati  staff               31843 May  7 11:14 technical/government/Alcohol_Problems/DraftRecom-PDF.txt
13782747      160 -rwxr-xr-x    1 kirankeertipati  staff               80034 May  7 11:14 technical/government/Alcohol_Problems/Session4-PDF.txt
13782763        0 drwxr-xr-x   93 kirankeertipati  staff                2976 May  7 11:14 technical/government/Gen_Account_Office
13782789      256 -rwxr-xr-x    1 kirankeertipati  staff              127448 May  7 11:14 technical/government/Gen_Account_Office/d0269g.txt
13782779      192 -rwxr-xr-x    1 kirankeertipati  staff               96111 May  7 11:14 technical/government/Gen_Account_Office/Testimony_cg00010t.txt
13782830       24 -rwxr-xr-x    1 kirankeertipati  staff               11370 May  7 11:14 technical/government/Gen_Account_Office/og97032.txt
13782853       16 -rwxr-xr-x    1 kirankeertipati  staff                6582 May  7 11:14 technical/government/Gen_Account_Office/og99036.txt
13782764      488 -rwxr-xr-x    1 kirankeertipati  staff              246218 May  7 11:14 technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
13782775      224 -rwxr-xr-x    1 kirankeertipati  staff              113222 May  7 11:14 technical/government/Gen_Account_Office/Sept27-2002_d02966.txt
13782787      272 -rwxr-xr-x    1 kirankeertipati  staff              137553 May  7 11:14 technical/government/Gen_Account_Office/d01376g.txt
13782776      600 -rwxr-xr-x    1 kirankeertipati  staff              306011 May  7 11:14 technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
13782826       16 -rwxr-xr-x    1 kirankeertipati  staff                6506 May  7 11:14 technical/government/Gen_Account_Office/og97019.txt
13782854      400 -rwxr-xr-x    1 kirankeertipati  staff              202066 May  7 11:14 technical/government/Gen_Account_Office/pe1019.txt
13782777       80 -rwxr-xr-x    1 kirankeertipati  staff               37156 May  7 11:14 technical/government/Gen_Account_Office/Testimony_Jul15-2002_d02940t.txt
13782795      216 -rwxr-xr-x    1 kirankeertipati  staff              106907 May  7 11:14 technical/government/Gen_Account_Office/gg96118.txt
13782827       24 -rwxr-xr-x    1 kirankeertipati  staff                8511 May  7 11:14 technical/government/Gen_Account_Office/og97020.txt
13782794       56 -rwxr-xr-x    1 kirankeertipati  staff               26946 May  7 11:14 technical/government/Gen_Account_Office/ffm.txt
13782828       16 -rwxr-xr-x    1 kirankeertipati  staff                6830 May  7 11:14 technical/government/Gen_Account_Office/og97023.txt
13782766      160 -rwxr-xr-x    1 kirankeertipati  staff               80304 May  7 11:14 technical/government/Gen_Account_Office/July11-2001_gg00172r.txt
13782784       16 -rwxr-xr-x    1 kirankeertipati  staff                4185 May  7 11:14 technical/government/Gen_Account_Office/d01121g.txt
13782798       32 -rwxr-xr-x    1 kirankeertipati  staff               16331 May  7 11:14 technical/government/Gen_Account_Office/og96011.txt
13782793      136 -rwxr-xr-x    1 kirankeertipati  staff               68219 May  7 11:14 technical/government/Gen_Account_Office/d03419sp.txt
13782769       64 -rwxr-xr-x    1 kirankeertipati  staff               29503 May  7 11:14 technical/government/Gen_Account_Office/Letter_Walkeraug17let.txt
13782838       24 -rwxr-xr-x    1 kirankeertipati  staff                9350 May  7 11:14 technical/government/Gen_Account_Office/og97051.txt
13782835       16 -rwxr-xr-x    1 kirankeertipati  staff                7459 May  7 11:14 technical/government/Gen_Account_Office/og97045.txt
13782780       80 -rwxr-xr-x    1 kirankeertipati  staff               38526 May  7 11:14 technical/government/Gen_Account_Office/Testimony_d01609t.txt
13782837       24 -rwxr-xr-x    1 kirankeertipati  staff               11282 May  7 11:14 technical/government/Gen_Account_Office/og97050.txt
13782815       32 -rwxr-xr-x    1 kirankeertipati  staff               16152 May  7 11:14 technical/government/Gen_Account_Office/og96038.txt
13782845       16 -rwxr-xr-x    1 kirankeertipati  staff                5455 May  7 11:14 technical/government/Gen_Account_Office/og98029.txt
13782774      136 -rwxr-xr-x    1 kirankeertipati  staff               65794 May  7 11:14 technical/government/Gen_Account_Office/Sept14-2002_d011070.txt
13782792       96 -rwxr-xr-x    1 kirankeertipati  staff               47581 May  7 11:14 technical/government/Gen_Account_Office/d03273g.txt
13782771       72 -rwxr-xr-x    1 kirankeertipati  staff               36163 May  7 11:14 technical/government/Gen_Account_Office/Oct15-1999_gg00026t.txt
13782799       24 -rwxr-xr-x    1 kirankeertipati  staff               10622 May  7 11:14 technical/government/Gen_Account_Office/og96012.txt
13782836       16 -rwxr-xr-x    1 kirankeertipati  staff                7547 May  7 11:14 technical/government/Gen_Account_Office/og97046.txt
13782839       24 -rwxr-xr-x    1 kirankeertipati  staff               10000 May  7 11:14 technical/government/Gen_Account_Office/og97052.txt
13782791      120 -rwxr-xr-x    1 kirankeertipati  staff               59136 May  7 11:14 technical/government/Gen_Account_Office/d03232sp.txt
13782834       24 -rwxr-xr-x    1 kirankeertipati  staff               10616 May  7 11:14 technical/government/Gen_Account_Office/og97043.txt
13782767      104 -rwxr-xr-x    1 kirankeertipati  staff               52587 May  7 11:14 technical/government/Gen_Account_Office/June30-2000_gg00135r.txt
13782788      592 -rwxr-xr-x    1 kirankeertipati  staff              302040 May  7 11:14 technical/government/Gen_Account_Office/d01591sp.txt
13782772      144 -rwxr-xr-x    1 kirankeertipati  staff               73339 May  7 11:14 technical/government/Gen_Account_Office/Oct15-2001_d0224.txt
13782808       16 -rwxr-xr-x    1 kirankeertipati  staff                7780 May  7 11:14 technical/government/Gen_Account_Office/og96028.txt
13782800       24 -rwxr-xr-x    1 kirankeertipati  staff                9289 May  7 11:14 technical/government/Gen_Account_Office/og96014.txt
13782833       24 -rwxr-xr-x    1 kirankeertipati  staff               11124 May  7 11:14 technical/government/Gen_Account_Office/og97041.txt
13782801       16 -rwxr-xr-x    1 kirankeertipati  staff                6002 May  7 11:14 technical/government/Gen_Account_Office/og96015.txt
13782785       48 -rwxr-xr-x    1 kirankeertipati  staff               23821 May  7 11:14 technical/government/Gen_Account_Office/d01145g.txt
13782765       56 -rwxr-xr-x    1 kirankeertipati  staff               28350 May  7 11:14 technical/government/Gen_Account_Office/InternalControl_ai00021p.txt
13782809       24 -rwxr-xr-x    1 kirankeertipati  staff               10461 May  7 11:14 technical/government/Gen_Account_Office/og96031.txt
13782786       72 -rwxr-xr-x    1 kirankeertipati  staff               34274 May  7 11:14 technical/government/Gen_Account_Office/d01186g.txt
13782811       16 -rwxr-xr-x    1 kirankeertipati  staff                6598 May  7 11:14 technical/government/Gen_Account_Office/og96033.txt
13782807       24 -rwxr-xr-x    1 kirankeertipati  staff               11321 May  7 11:14 technical/government/Gen_Account_Office/og96027.txt
13782842       24 -rwxr-xr-x    1 kirankeertipati  staff               10504 May  7 11:14 technical/government/Gen_Account_Office/og98022.txt
13782806       32 -rwxr-xr-x    1 kirankeertipati  staff               14287 May  7 11:14 technical/government/Gen_Account_Office/og96026.txt
13782810       24 -rwxr-xr-x    1 kirankeertipati  staff                8900 May  7 11:14 technical/government/Gen_Account_Office/og96032.txt
13782796      232 -rwxr-xr-x    1 kirankeertipati  staff              115899 May  7 11:14 technical/government/Gen_Account_Office/im814.txt
13782813       32 -rwxr-xr-x    1 kirankeertipati  staff               12456 May  7 11:14 technical/government/Gen_Account_Office/og96036.txt
13782804       32 -rwxr-xr-x    1 kirankeertipati  staff               14691 May  7 11:14 technical/government/Gen_Account_Office/og96022.txt
13782805       24 -rwxr-xr-x    1 kirankeertipati  staff                9806 May  7 11:14 technical/government/Gen_Account_Office/og96023.txt
13782814       24 -rwxr-xr-x    1 kirankeertipati  staff                9158 May  7 11:14 technical/government/Gen_Account_Office/og96037.txt
13782847       24 -rwxr-xr-x    1 kirankeertipati  staff                8588 May  7 11:14 technical/government/Gen_Account_Office/og98032.txt
13782844       16 -rwxr-xr-x    1 kirankeertipati  staff                5537 May  7 11:14 technical/government/Gen_Account_Office/og98026.txt
13782846       16 -rwxr-xr-x    1 kirankeertipati  staff                6142 May  7 11:14 technical/government/Gen_Account_Office/og98030.txt
13782843       16 -rwxr-xr-x    1 kirankeertipati  staff                6966 May  7 11:14 technical/government/Gen_Account_Office/og98024.txt
13782797       16 -rwxr-xr-x    1 kirankeertipati  staff                6804 May  7 11:14 technical/government/Gen_Account_Office/og96009.txt
13782803       16 -rwxr-xr-x    1 kirankeertipati  staff                6969 May  7 11:14 technical/government/Gen_Account_Office/og96021.txt
13782840       16 -rwxr-xr-x    1 kirankeertipati  staff                5937 May  7 11:14 technical/government/Gen_Account_Office/og98018.txt
13782781      192 -rwxr-xr-x    1 kirankeertipati  staff               97533 May  7 11:14 technical/government/Gen_Account_Office/ai00134.txt
13782812       24 -rwxr-xr-x    1 kirankeertipati  staff               10364 May  7 11:14 technical/government/Gen_Account_Office/og96034.txt
13782841       16 -rwxr-xr-x    1 kirankeertipati  staff                5372 May  7 11:14 technical/government/Gen_Account_Office/og98019.txt
13782802       24 -rwxr-xr-x    1 kirankeertipati  staff                8703 May  7 11:14 technical/government/Gen_Account_Office/og96020.txt
13782778      128 -rwxr-xr-x    1 kirankeertipati  staff               61940 May  7 11:14 technical/government/Gen_Account_Office/Testimony_Jul17-2002_d02957t.txt
13782821       24 -rwxr-xr-x    1 kirankeertipati  staff                9811 May  7 11:14 technical/government/Gen_Account_Office/og96047.txt
13782783      224 -rwxr-xr-x    1 kirankeertipati  staff              114375 May  7 11:14 technical/government/Gen_Account_Office/ai9868.txt
13782849       16 -rwxr-xr-x    1 kirankeertipati  staff                6930 May  7 11:14 technical/government/Gen_Account_Office/og98041.txt
13782831       16 -rwxr-xr-x    1 kirankeertipati  staff                7976 May  7 11:14 technical/government/Gen_Account_Office/og97038.txt
13782773      104 -rwxr-xr-x    1 kirankeertipati  staff               49912 May  7 11:14 technical/government/Gen_Account_Office/Paper_Walker11-2002_acpro122.txt
13782825       16 -rwxr-xr-x    1 kirankeertipati  staff                8173 May  7 11:14 technical/government/Gen_Account_Office/og97011.txt
13782832       24 -rwxr-xr-x    1 kirankeertipati  staff                9835 May  7 11:14 technical/government/Gen_Account_Office/og97039.txt
13782770      224 -rwxr-xr-x    1 kirankeertipati  staff              114375 May  7 11:14 technical/government/Gen_Account_Office/May1998_ai98068.txt
13782848       24 -rwxr-xr-x    1 kirankeertipati  staff                8547 May  7 11:14 technical/government/Gen_Account_Office/og98040.txt
13782820       24 -rwxr-xr-x    1 kirankeertipati  staff               10365 May  7 11:14 technical/government/Gen_Account_Office/og96045.txt
13782850       16 -rwxr-xr-x    1 kirankeertipati  staff                5969 May  7 11:14 technical/government/Gen_Account_Office/og98044.txt
13782817       40 -rwxr-xr-x    1 kirankeertipati  staff               16629 May  7 11:14 technical/government/Gen_Account_Office/og96041.txt
13782790      280 -rwxr-xr-x    1 kirankeertipati  staff              140071 May  7 11:14 technical/government/Gen_Account_Office/d02701.txt
13782822       16 -rwxr-xr-x    1 kirankeertipati  staff                6891 May  7 11:14 technical/government/Gen_Account_Office/og97001.txt
13782829       16 -rwxr-xr-x    1 kirankeertipati  staff                5826 May  7 11:14 technical/government/Gen_Account_Office/og97028.txt
13782782      144 -rwxr-xr-x    1 kirankeertipati  staff               70286 May  7 11:14 technical/government/Gen_Account_Office/ai2132.txt
13782768       16 -rwxr-xr-x    1 kirankeertipati  staff                7852 May  7 11:14 technical/government/Gen_Account_Office/Letter_WalkerJan30-2001.txt
13782816       24 -rwxr-xr-x    1 kirankeertipati  staff                9710 May  7 11:14 technical/government/Gen_Account_Office/og96040.txt
13782851       24 -rwxr-xr-x    1 kirankeertipati  staff                8927 May  7 11:14 technical/government/Gen_Account_Office/og98045.txt
13782818       24 -rwxr-xr-x    1 kirankeertipati  staff                8973 May  7 11:14 technical/government/Gen_Account_Office/og96042.txt
13782823       16 -rwxr-xr-x    1 kirankeertipati  staff                6755 May  7 11:14 technical/government/Gen_Account_Office/og97002.txt
13782824       24 -rwxr-xr-x    1 kirankeertipati  staff               11267 May  7 11:14 technical/government/Gen_Account_Office/og97003.txt
13782819       24 -rwxr-xr-x    1 kirankeertipati  staff               10684 May  7 11:14 technical/government/Gen_Account_Office/og96043.txt
13782852       16 -rwxr-xr-x    1 kirankeertipati  staff                7108 May  7 11:14 technical/government/Gen_Account_Office/og98046.txt
13783001        0 drwxr-xr-x   16 kirankeertipati  staff                 512 May  7 11:14 technical/government/Post_Rate_Comm
13783008       48 -rwxr-xr-x    1 kirankeertipati  staff               22775 May  7 11:14 technical/government/Post_Rate_Comm/Gleiman_EMASpeech.txt
13783012       80 -rwxr-xr-x    1 kirankeertipati  staff               37843 May  7 11:14 technical/government/Post_Rate_Comm/Mitchell_spyros-first-class.txt
13783003       88 -rwxr-xr-x    1 kirankeertipati  staff               42507 May  7 11:14 technical/government/Post_Rate_Comm/Cohenetal_CreamSkimming.txt
13783004       64 -rwxr-xr-x    1 kirankeertipati  staff               32627 May  7 11:14 technical/government/Post_Rate_Comm/Cohenetal_DeliveryCost.txt
13783011       96 -rwxr-xr-x    1 kirankeertipati  staff               45459 May  7 11:14 technical/government/Post_Rate_Comm/Mitchell_RMVancouver.txt
13783009       56 -rwxr-xr-x    1 kirankeertipati  staff               26143 May  7 11:14 technical/government/Post_Rate_Comm/Gleiman_gca2000.txt
13783002       48 -rwxr-xr-x    1 kirankeertipati  staff               20822 May  7 11:14 technical/government/Post_Rate_Comm/Cohenetal_Cost_Function.txt
13783013       48 -rwxr-xr-x    1 kirankeertipati  staff               21178 May  7 11:14 technical/government/Post_Rate_Comm/Redacted_Study.txt
13783010      152 -rwxr-xr-x    1 kirankeertipati  staff               75973 May  7 11:14 technical/government/Post_Rate_Comm/Mitchell_6-17-Mit.txt
13783007       80 -rwxr-xr-x    1 kirankeertipati  staff               39854 May  7 11:14 technical/government/Post_Rate_Comm/Cohenetal_comparison.txt
13783006       72 -rwxr-xr-x    1 kirankeertipati  staff               35913 May  7 11:14 technical/government/Post_Rate_Comm/Cohenetal_Scale.txt
13783005       72 -rwxr-xr-x    1 kirankeertipati  staff               33903 May  7 11:14 technical/government/Post_Rate_Comm/Cohenetal_RuralDelivery.txt
13783014       64 -rwxr-xr-x    1 kirankeertipati  staff               32630 May  7 11:14 technical/government/Post_Rate_Comm/ReportToCongress2002WEB.txt
13783015       24 -rwxr-xr-x    1 kirankeertipati  staff               11609 May  7 11:14 technical/government/Post_Rate_Comm/WolakSpeech_usps.txt
13782855        0 drwxr-xr-x  147 kirankeertipati  staff                4704 May  7 11:14 technical/government/Media
13782897        8 -rwxr-xr-x    1 kirankeertipati  staff                3784 May  7 11:14 technical/government/Media/Federal_agency.txt
13783000        8 -rwxr-xr-x    1 kirankeertipati  staff                3107 May  7 11:14 technical/government/Media/water_fees.txt
13782913       16 -rwxr-xr-x    1 kirankeertipati  staff                6287 May  7 11:14 technical/government/Media/Helping_Out.txt
13782987       16 -rwxr-xr-x    1 kirankeertipati  staff                4279 May  7 11:14 technical/government/Media/balance_scales_of_justice.txt
13782878        8 -rwxr-xr-x    1 kirankeertipati  staff                2421 May  7 11:14 technical/government/Media/BusinessWire2.txt
13782925       16 -rwxr-xr-x    1 kirankeertipati  staff                5965 May  7 11:14 technical/government/Media/Legal-aid_chief.txt
13782977       16 -rwxr-xr-x    1 kirankeertipati  staff                6453 May  7 11:14 technical/government/Media/Unusual_Woodburn.txt
13782905        8 -rwxr-xr-x    1 kirankeertipati  staff                2078 May  7 11:14 technical/government/Media/Funding_cuts_force.txt
13782908       16 -rwxr-xr-x    1 kirankeertipati  staff                6946 May  7 11:14 technical/government/Media/Good_guys_reward.txt
13782865       16 -rwxr-xr-x    1 kirankeertipati  staff                5947 May  7 11:14 technical/government/Media/Anthem_Payout.txt
13782892        8 -rwxr-xr-x    1 kirankeertipati  staff                2980 May  7 11:14 technical/government/Media/Donald_Hilliker.txt
13782903        8 -rwxr-xr-x    1 kirankeertipati  staff                2702 May  7 11:14 technical/government/Media/Free_legal_service.txt
13782947        8 -rwxr-xr-x    1 kirankeertipati  staff                2611 May  7 11:14 technical/government/Media/Owning_a_Piece.txt
13782967       16 -rwxr-xr-x    1 kirankeertipati  staff                6011 May  7 11:14 technical/government/Media/Targeting_Domestic_Violence.txt
13782993       16 -rwxr-xr-x    1 kirankeertipati  staff                4112 May  7 11:14 technical/government/Media/highlight_Senior_Day.txt
13782964        8 -rwxr-xr-x    1 kirankeertipati  staff                3798 May  7 11:14 technical/government/Media/State_funding.txt
13782898       16 -rwxr-xr-x    1 kirankeertipati  staff                5577 May  7 11:14 technical/government/Media/Few_who_need.txt
13782881       16 -rwxr-xr-x    1 kirankeertipati  staff                6104 May  7 11:14 technical/government/Media/City_Council_Budget.txt
13782933       16 -rwxr-xr-x    1 kirankeertipati  staff                7218 May  7 11:14 technical/government/Media/Legal_system_fails_poor.txt
13782965       16 -rwxr-xr-x    1 kirankeertipati  staff                4570 May  7 11:14 technical/government/Media/Supporting_Legal_Center.txt
13782935       16 -rwxr-xr-x    1 kirankeertipati  staff                4547 May  7 11:14 technical/government/Media/Lindsays_legacy.txt
13782944        8 -rwxr-xr-x    1 kirankeertipati  staff                4075 May  7 11:14 technical/government/Media/New_funding_sources.txt
13782870       16 -rwxr-xr-x    1 kirankeertipati  staff                4540 May  7 11:14 technical/government/Media/Barnes_new_job.txt
13782956        8 -rwxr-xr-x    1 kirankeertipati  staff                2768 May  7 11:14 technical/government/Media/Providing_Legal_Aid.txt
13782945       16 -rwxr-xr-x    1 kirankeertipati  staff                4208 May  7 11:14 technical/government/Media/Nonprofit_Buys.txt
13782929        8 -rwxr-xr-x    1 kirankeertipati  staff                3889 May  7 11:14 technical/government/Media/Legal_Aid_in_Clay_County.txt
13782890       16 -rwxr-xr-x    1 kirankeertipati  staff                5158 May  7 11:14 technical/government/Media/Domestic_Violence_Ruling.txt
13782860       16 -rwxr-xr-x    1 kirankeertipati  staff                6261 May  7 11:14 technical/government/Media/Abuse_penalties.txt
13782922        8 -rwxr-xr-x    1 kirankeertipati  staff                3610 May  7 11:14 technical/government/Media/Law_Award_from_College.txt
13782923       24 -rwxr-xr-x    1 kirankeertipati  staff                8530 May  7 11:14 technical/government/Media/Law_Schools.txt
13782957       16 -rwxr-xr-x    1 kirankeertipati  staff                5215 May  7 11:14 technical/government/Media/Raising_the_Bar.txt
13782918       16 -rwxr-xr-x    1 kirankeertipati  staff                5451 May  7 11:14 technical/government/Media/Justice_for_all.txt
13782986        8 -rwxr-xr-x    1 kirankeertipati  staff                2609 May  7 11:14 technical/government/Media/agency_expands.txt
13782912        8 -rwxr-xr-x    1 kirankeertipati  staff                2009 May  7 11:14 technical/government/Media/Helping_Hands.txt
13782931        8 -rwxr-xr-x    1 kirankeertipati  staff                2788 May  7 11:14 technical/government/Media/Legal_hotline.txt
13782996        8 -rwxr-xr-x    1 kirankeertipati  staff                3993 May  7 11:14 technical/government/Media/not_accessible_to_disabled.txt
13782880        8 -rwxr-xr-x    1 kirankeertipati  staff                1708 May  7 11:14 technical/government/Media/Campaign_Pays.txt
13782943       16 -rwxr-xr-x    1 kirankeertipati  staff                4179 May  7 11:14 technical/government/Media/New_Online_Resources.txt
13782864       16 -rwxr-xr-x    1 kirankeertipati  staff                4866 May  7 11:14 technical/government/Media/Annual_Fee.txt
13782946       16 -rwxr-xr-x    1 kirankeertipati  staff                4314 May  7 11:14 technical/government/Media/Oregon_Poor.txt
13782871        8 -rwxr-xr-x    1 kirankeertipati  staff                2241 May  7 11:14 technical/government/Media/Barnes_pro_bono.txt
13782951        8 -rwxr-xr-x    1 kirankeertipati  staff                2155 May  7 11:14 technical/government/Media/Poor_Lacking_Legal_Aid.txt
13782948        8 -rwxr-xr-x    1 kirankeertipati  staff                2947 May  7 11:14 technical/government/Media/Paralegal_Honored.txt
13782984        8 -rwxr-xr-x    1 kirankeertipati  staff                3834 May  7 11:14 technical/government/Media/Workers_aid_center.txt
13782949       16 -rwxr-xr-x    1 kirankeertipati  staff                4263 May  7 11:14 technical/government/Media/Philly_Lawyers.txt
13782974       16 -rwxr-xr-x    1 kirankeertipati  staff                5450 May  7 11:14 technical/government/Media/Too_Crucial_to_Take_Cut.txt
13782954        8 -rwxr-xr-x    1 kirankeertipati  staff                4057 May  7 11:14 technical/government/Media/Pro_Bono_Services.txt
13782961        8 -rwxr-xr-x    1 kirankeertipati  staff                3720 May  7 11:14 technical/government/Media/Rumble_in_the_Bronx.txt
13782901        8 -rwxr-xr-x    1 kirankeertipati  staff                3664 May  7 11:14 technical/government/Media/FortWorthStarTelegram.txt
13782997       24 -rwxr-xr-x    1 kirankeertipati  staff                8383 May  7 11:14 technical/government/Media/predatory_loans.txt
13782966       24 -rwxr-xr-x    1 kirankeertipati  staff                9085 May  7 11:14 technical/government/Media/Survey.txt
13782857        8 -rwxr-xr-x    1 kirankeertipati  staff                2401 May  7 11:14 technical/government/Media/AP_LawSchoolDebts.txt
13782985       16 -rwxr-xr-x    1 kirankeertipati  staff                5109 May  7 11:14 technical/government/Media/Working_for_Free.txt
13782894        8 -rwxr-xr-x    1 kirankeertipati  staff                4021 May  7 11:14 technical/government/Media/Eviction_law.txt
13782921        8 -rwxr-xr-x    1 kirankeertipati  staff                3892 May  7 11:14 technical/government/Media/Law-school_grads.txt
13782895        8 -rwxr-xr-x    1 kirankeertipati  staff                2519 May  7 11:14 technical/government/Media/FY_04_Budget_Outlook.txt
13782992        8 -rwxr-xr-x    1 kirankeertipati  staff                3710 May  7 11:14 technical/government/Media/help_rent-to-own_tenants.txt
13782969       16 -rwxr-xr-x    1 kirankeertipati  staff                5294 May  7 11:14 technical/government/Media/Texas_Lawyer.txt
13782888        8 -rwxr-xr-x    1 kirankeertipati  staff                3539 May  7 11:14 technical/government/Media/Disaster_center.txt
13782920        8 -rwxr-xr-x    1 kirankeertipati  staff                3306 May  7 11:14 technical/government/Media/Kiosks_for_court_forms.txt
13782914        8 -rwxr-xr-x    1 kirankeertipati  staff                3740 May  7 11:14 technical/government/Media/Higher_Registration_Fees.txt
13782899        8 -rwxr-xr-x    1 kirankeertipati  staff                1757 May  7 11:14 technical/government/Media/Fire_Victims_Sue.txt
13782906        8 -rwxr-xr-x    1 kirankeertipati  staff                4080 May  7 11:14 technical/government/Media/Funds_Shortage.txt
13782968       32 -rwxr-xr-x    1 kirankeertipati  staff               14232 May  7 11:14 technical/government/Media/Terrorist_Attack.txt
13782879        8 -rwxr-xr-x    1 kirankeertipati  staff                3459 May  7 11:14 technical/government/Media/Butler_Co_attorneys.txt
13782873       16 -rwxr-xr-x    1 kirankeertipati  staff                7511 May  7 11:14 technical/government/Media/BergenCountyRecord.txt
13782989        8 -rwxr-xr-x    1 kirankeertipati  staff                3045 May  7 11:14 technical/government/Media/families_saved.txt
13782886        8 -rwxr-xr-x    1 kirankeertipati  staff                1941 May  7 11:14 technical/government/Media/Court_Keeps_Judge_From.txt
13782980       16 -rwxr-xr-x    1 kirankeertipati  staff                4347 May  7 11:14 technical/government/Media/Volunteers_Step_Up.txt
13782885       32 -rwxr-xr-x    1 kirankeertipati  staff               14442 May  7 11:14 technical/government/Media/Coup_Reshapes_Legal_Aid.txt
13782916       16 -rwxr-xr-x    1 kirankeertipati  staff                7727 May  7 11:14 technical/government/Media/IOLTA_INTEREST_RATE.txt
13782907        8 -rwxr-xr-x    1 kirankeertipati  staff                3133 May  7 11:14 technical/government/Media/Ginny_Kilgore.txt
13782930        8 -rwxr-xr-x    1 kirankeertipati  staff                2844 May  7 11:14 technical/government/Media/Legal_Aid_looks_to_legislators.txt
13782952       24 -rwxr-xr-x    1 kirankeertipati  staff                8627 May  7 11:14 technical/government/Media/Poverty_Lawyers.txt
13782983        8 -rwxr-xr-x    1 kirankeertipati  staff                2553 May  7 11:14 technical/government/Media/Wingates_winds.txt
13782868       16 -rwxr-xr-x    1 kirankeertipati  staff                7375 May  7 11:14 technical/government/Media/Avoids_Budget_Cut.txt
13782991       16 -rwxr-xr-x    1 kirankeertipati  staff                5387 May  7 11:14 technical/government/Media/grants_fail_to_come.txt
13782937        8 -rwxr-xr-x    1 kirankeertipati  staff                3658 May  7 11:14 technical/government/Media/Lockyer_Warns.txt
13782917        8 -rwxr-xr-x    1 kirankeertipati  staff                1999 May  7 11:14 technical/government/Media/It_Pays_to_Know.txt
13782962        8 -rwxr-xr-x    1 kirankeertipati  staff                1742 May  7 11:14 technical/government/Media/Self-Help_Website.txt
13782958        8 -rwxr-xr-x    1 kirankeertipati  staff                3968 May  7 11:14 technical/government/Media/Rental_rules.txt
13782978       24 -rwxr-xr-x    1 kirankeertipati  staff                8629 May  7 11:14 technical/government/Media/Using_Tech_Tools.txt
13782866       24 -rwxr-xr-x    1 kirankeertipati  staff               10950 May  7 11:14 technical/government/Media/Assuring_Underprivileged.txt
13782875        8 -rwxr-xr-x    1 kirankeertipati  staff                2106 May  7 11:14 technical/government/Media/Boone_legal_service.txt
13782900        8 -rwxr-xr-x    1 kirankeertipati  staff                3562 May  7 11:14 technical/government/Media/Firm_to_the_Poor_Needs_Help.txt
13782940       16 -rwxr-xr-x    1 kirankeertipati  staff                5847 May  7 11:14 technical/government/Media/Making_a_case.txt
13782869        8 -rwxr-xr-x    1 kirankeertipati  staff                2154 May  7 11:14 technical/government/Media/Barnes_Volunteers.txt
13782884        8 -rwxr-xr-x    1 kirankeertipati  staff                2311 May  7 11:14 technical/government/Media/Commercial_Appeal.txt
13782919        8 -rwxr-xr-x    1 kirankeertipati  staff                1741 May  7 11:14 technical/government/Media/Justice_requests.txt
13782902       16 -rwxr-xr-x    1 kirankeertipati  staff                5262 May  7 11:14 technical/government/Media/Free_Legal_Assistance.txt
13782936       16 -rwxr-xr-x    1 kirankeertipati  staff                6893 May  7 11:14 technical/government/Media/Local_Attorneys.txt
13782970        8 -rwxr-xr-x    1 kirankeertipati  staff                3702 May  7 11:14 technical/government/Media/Texas_Supreme_Court.txt
13782882        8 -rwxr-xr-x    1 kirankeertipati  staff                2418 May  7 11:14 technical/government/Media/Civil_Matters.txt
13782938        8 -rwxr-xr-x    1 kirankeertipati  staff                2715 May  7 11:14 technical/government/Media/Low-income_children.txt
13782995       16 -rwxr-xr-x    1 kirankeertipati  staff                5675 May  7 11:14 technical/government/Media/man_on_national_team.txt
13782877       16 -rwxr-xr-x    1 kirankeertipati  staff                5613 May  7 11:14 technical/government/Media/BusinessWire.txt
13782904        8 -rwxr-xr-x    1 kirankeertipati  staff                3133 May  7 11:14 technical/government/Media/Funding_May_Limit.txt
13782972        8 -rwxr-xr-x    1 kirankeertipati  staff                2695 May  7 11:14 technical/government/Media/The_Columbian.txt
13782915        8 -rwxr-xr-x    1 kirankeertipati  staff                2334 May  7 11:14 technical/government/Media/Higher_court.txt
13782963       16 -rwxr-xr-x    1 kirankeertipati  staff                5182 May  7 11:14 technical/government/Media/Service_Agency.txt
13782941       16 -rwxr-xr-x    1 kirankeertipati  staff                7732 May  7 11:14 technical/government/Media/Marylands_Legal_Aid.txt
13782874        8 -rwxr-xr-x    1 kirankeertipati  staff                2156 May  7 11:14 technical/government/Media/Bias_on_the_Job.txt
13782867        8 -rwxr-xr-x    1 kirankeertipati  staff                2244 May  7 11:14 technical/government/Media/Attorney_gives_his_time.txt
13782934       16 -rwxr-xr-x    1 kirankeertipati  staff                4663 May  7 11:14 technical/government/Media/Library_Lawyers.txt
13782887        8 -rwxr-xr-x    1 kirankeertipati  staff                3746 May  7 11:14 technical/government/Media/Crains_New_York_Business.txt
13782911        8 -rwxr-xr-x    1 kirankeertipati  staff                3706 May  7 11:14 technical/government/Media/Hard_to_Get.txt
13782973       24 -rwxr-xr-x    1 kirankeertipati  staff                8304 May  7 11:14 technical/government/Media/The_State_of_Pro_Bono.txt
13782999        8 -rwxr-xr-x    1 kirankeertipati  staff                2978 May  7 11:14 technical/government/Media/residents_sue_city.txt
13782926        8 -rwxr-xr-x    1 kirankeertipati  staff                2094 May  7 11:14 technical/government/Media/Legal_Aid_Society.txt
13782910       16 -rwxr-xr-x    1 kirankeertipati  staff                5440 May  7 11:14 technical/government/Media/GreensburgDailyNews.txt
13782939       16 -rwxr-xr-x    1 kirankeertipati  staff                6721 May  7 11:14 technical/government/Media/Major_Changes.txt
13782955        8 -rwxr-xr-x    1 kirankeertipati  staff                3763 May  7 11:14 technical/government/Media/Program_Lodges.txt
13782982        8 -rwxr-xr-x    1 kirankeertipati  staff                2042 May  7 11:14 technical/government/Media/Wilmington_lawyer.txt
13782863        8 -rwxr-xr-x    1 kirankeertipati  staff                2183 May  7 11:14 technical/government/Media/All_May_Have_Justice.txt
13782891        8 -rwxr-xr-x    1 kirankeertipati  staff                3765 May  7 11:14 technical/government/Media/Domestic_violence_aid.txt
13782861        8 -rwxr-xr-x    1 kirankeertipati  staff                2869 May  7 11:14 technical/government/Media/Advocate_for_Poor.txt
13782990        8 -rwxr-xr-x    1 kirankeertipati  staff                2806 May  7 11:14 technical/government/Media/fight_domestic_abuse.txt
13782883       16 -rwxr-xr-x    1 kirankeertipati  staff                6363 May  7 11:14 technical/government/Media/CommercialAppealMemphis2.txt
13782981       16 -rwxr-xr-x    1 kirankeertipati  staff                6924 May  7 11:14 technical/government/Media/Weak_economy.txt
13782924        8 -rwxr-xr-x    1 kirankeertipati  staff                1992 May  7 11:14 technical/government/Media/Lawyer_Web_Survey.txt
13782979        8 -rwxr-xr-x    1 kirankeertipati  staff                2249 May  7 11:14 technical/government/Media/Valley_Needing_Legal_Services.txt
13782872        8 -rwxr-xr-x    1 kirankeertipati  staff                3951 May  7 11:14 technical/government/Media/Barr_sharpening_ax.txt
13782927        8 -rwxr-xr-x    1 kirankeertipati  staff                3591 May  7 11:14 technical/government/Media/Legal_Aid_attorney.txt
13782971        8 -rwxr-xr-x    1 kirankeertipati  staff                3138 May  7 11:14 technical/government/Media/The_Bend_Bulletin.txt
13782932        8 -rwxr-xr-x    1 kirankeertipati  staff                4047 May  7 11:14 technical/government/Media/Legal_services_for_poor.txt
13782896       24 -rwxr-xr-x    1 kirankeertipati  staff                9553 May  7 11:14 technical/government/Media/Farm_workers.txt
13782893       16 -rwxr-xr-x    1 kirankeertipati  staff                4366 May  7 11:14 technical/government/Media/Entities_Merge.txt
13782994        8 -rwxr-xr-x    1 kirankeertipati  staff                3137 May  7 11:14 technical/government/Media/less_legal_aid.txt
13782976       16 -rwxr-xr-x    1 kirankeertipati  staff                5820 May  7 11:14 technical/government/Media/Understanding.txt
13782889        8 -rwxr-xr-x    1 kirankeertipati  staff                2358 May  7 11:14 technical/government/Media/Do-it-yourself_divorce.txt
13782950       16 -rwxr-xr-x    1 kirankeertipati  staff                5114 May  7 11:14 technical/government/Media/Politician_Practices.txt
13782988        8 -rwxr-xr-x    1 kirankeertipati  staff                3698 May  7 11:14 technical/government/Media/defend_yourself.txt
13782975       16 -rwxr-xr-x    1 kirankeertipati  staff                4136 May  7 11:14 technical/government/Media/Towson_Attorney.txt
13782953        8 -rwxr-xr-x    1 kirankeertipati  staff                3976 May  7 11:14 technical/government/Media/Pro-bono_road_show.txt
13782858        8 -rwxr-xr-x    1 kirankeertipati  staff                2187 May  7 11:14 technical/government/Media/A_Perk_of_Age.txt
13782859       16 -rwxr-xr-x    1 kirankeertipati  staff                7163 May  7 11:14 technical/government/Media/A_helping_hand.txt
13782998        8 -rwxr-xr-x    1 kirankeertipati  staff                3485 May  7 11:14 technical/government/Media/pro_bono_efforts.txt
13782856        8 -rwxr-xr-x    1 kirankeertipati  staff                3035 May  7 11:14 technical/government/Media/5_Legal_Groups.txt
13782909       16 -rwxr-xr-x    1 kirankeertipati  staff                7294 May  7 11:14 technical/government/Media/Greedy_Generous.txt
13782959       16 -rwxr-xr-x    1 kirankeertipati  staff                5225 May  7 11:14 technical/government/Media/Retirement_Has_Its_Appeal.txt
13782960        8 -rwxr-xr-x    1 kirankeertipati  staff                4081 May  7 11:14 technical/government/Media/RoanokeTimes.txt
13782942       24 -rwxr-xr-x    1 kirankeertipati  staff                8713 May  7 11:14 technical/government/Media/NJ_Legal_Services.txt
13782876       16 -rwxr-xr-x    1 kirankeertipati  staff                5442 May  7 11:14 technical/government/Media/Bridging_legal_aid_gap.txt
13782928        8 -rwxr-xr-x    1 kirankeertipati  staff                2850 May  7 11:14 technical/government/Media/Legal_Aid_campaign.txt
13782862        8 -rwxr-xr-x    1 kirankeertipati  staff                2851 May  7 11:14 technical/government/Media/Aid_Gets_7_Million.txt
```
find -type d:
(lists all the directories)

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % find technical -type d
technical
technical/government
technical/government/About_LSC
technical/government/Env_Prot_Agen
technical/government/Alcohol_Problems
technical/government/Gen_Account_Office
technical/government/Post_Rate_Comm
technical/government/Media
technical/plos
technical/biomed
technical/911report
```

https://www.geeksforgeeks.org/find-command-in-linux-with-examples/

find -type f -empty: (finds empty files, but since there are no empty files in technical there is no output)
```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % find technical -empty
```
find -exec grep 'Our':

```
kirankeertipati@Kirans-MacBook-Pro stringsearch-data % find technical/911report -exec grep 'Our' {} \;
grep: technical/911report: Is a directory
                2003; Apr. 5, 2004. Our investigation has uncovered no evidence that the 9/11
                report, list of Flight 93 victims, undated (as of July 9, 2004). Our conclusion that
                Revisiting Our 1995 Estimate," ICB 97-8, Apr. 1997, p. 1.
                Muslim ummah [community of believers] are treated with contempt and dishonour. Our
                religion is denigrated. Our holy places desecrated. Our countries are occupied. Our
                and overall policy by J-5. Our concept combines the J-2 and J-3 functions
            Our recommendation to leave counterterrorism intelligence collection in the United
                home?" Our national defense at home is the responsibility, first, of the Department
            Our investigation built on the work of many others, including the Joint Inquiry of
            108. Hamilton, How Congress Works, p. 17. Our review of the classified schedules of
                of a new type of terrorism. Our overview of U.S. capabilities for dealing with it
                al Qaeda as "your agents." Bin Ladin has stated flatly,"Our fight against these
                and accessed from this country. Our investigation has uncovered no credible evidence
                money. Our knowledge of the funding during this period, before the operatives
            Our only sources for what intelligence officials thought at the time are what they
            Our inability to ascertain the activities of Hazmi and Mihdhar during their first two
            Our investigators who have dealt directly with him and studied his background find
            Our knowledge of the international travels of the al Qaeda operatives selected for
                Qaeda and the Taliban argued over strategy for 2001. Our focus has naturally been on
                recommendations to address this critical need. Our recommendations grow out of the
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
            Our aim has not been to assign individual blame. Our aim has been to provide the
                communities in non-Muslim countries. Our enemy is twofold: al Qaeda, a stateless
            Terrorism is a tactic used by individuals and organizations to kill and destroy. Our
                nations as partners in its development and implementation. Our effort should be
            Our strategy should also include defenses. America can be attacked in many ways and
                Our report shows a determined and capable group of plotters. Yet the group was
                ratio is against us! Our cost is billions against the terrorists' costs of
            These are the right questions. Our answer is that we need short-term action on a
                Recommendation: Our report shows that al Qaeda has tried to acquire
                safer, they are not safe. Our report shows that the terrorists analyze defenses.
            Our investigation showed that two systemic weaknesses came together in our border
            Our border screening system should check people efficiently and welcome friends.
            Our borders and immigration system, including law enforcement, ought to send a
                terrorist attack at home. Our history has shown us that insecurity threatens
                attacks and have since found no evidence to change that conclusion. Our own
                our many Arab friends. Our enemy is a radical network of terrorists, and every
            President Bush argued that the new war went beyond Bin Ladin." Our war on terror
                to publicize an assessment of the growing al Qaeda danger. Our government could
 
 ```
 
