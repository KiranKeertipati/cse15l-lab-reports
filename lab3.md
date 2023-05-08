# Lab Report 3 #

## Researching Commands #
Out of the three commands we had to pick: `less`, `find`, and `grep`, I choose the `find` command.

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
