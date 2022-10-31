# Lab Report 3

**Researching Commands**

---

**-iname**

* -iname takes the name of the file or directory regardless of whether it is lower or uppercase, making it so that more files can be grouped and found together in a specific method. 

```
[cs15lfa22lc@ieng6-201]:docsearch:168$ find technical -name "help*"
technical/government/Media/help_rent-to-own_tenants.txt
[cs15lfa22lc@ieng6-201]:docsearch:169$ find technical -iname "help*"
technical/government/Media/Helping_Hands.txt
technical/government/Media/Helping_Out.txt
technical/government/Media/help_rent-to-own_tenants.txt
```
* In this example, we can see that the command -name only calls on one file which happens to be lowercase sensitive to due "help*" being lowercase. When using -iname, we can call on uppercase files that contain help in addition to the file that we called earlier. 

```
[cs15lfa22lc@ieng6-201]:docsearch:170$ find technical -name "legal*"
[cs15lfa22lc@ieng6-201]:docsearch:171$ find technical -iname "legal*"
technical/government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt
technical/government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
```

* In this example, we can see that no fiales were called when using "legal*" as there were no files that contained "legal" in lowercase. However, when using -iname, we see that we called on three files that contained "legal" in uppercase. 

```
[cs15lfa22lc@ieng6-201]:docsearch:178$ find technical/911report -name "*Txt"    
[cs15lfa22lc@ieng6-201]:docsearch:179$ find technical/911report -iname "*Txt"   
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/911report/preface.txt
```

* In this example, we see that -name produces no results as there are no .txt files that exist with an uppercase T. However, when we use -iname, we can bypass this error and call lowercase .txt files. 

---

**-type f & -type d**

* -type f and -type d respectively call upon either a file or directory depending on which method is used, making it easier to filter and sort. 

```
[cs15lfa22lc@ieng6-201]:docsearch:177$ find technical/911report -type f -name "*.txt"                                    
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/911report/preface.txt
```

* As our command line is searching for .txt files in technical/911report, we can see that -type f will affect the result as everything that is called is arleady a file. 

```
[cs15lfa22lc@ieng6-201]:docsearch:180$ find technical/911report -type d -name "*.txt"
```

* However, when we try to run the same command with -type d, we will see that no results will be produced as -type d searches for directories even though we called for .txt files. 

```
[cs15lfa22lc@ieng6-201]:docsearch:181$ find technical -iname "tech*"
technical
technical/government/Env_Prot_Agen/tech_adden.txt
technical/government/Env_Prot_Agen/tech_sectiong.txt
[cs15lfa22lc@ieng6-201]:docsearch:184$ find technical -type d -iname "tech*"    
technical
```

* In this example, we see how our first command line produces both the technical directory as well as two txt files that contain "tech". However, when we use -type d in the second command line, we see that only the technical directory is called. 

---

**-delete**

* -delete deletes the selected files or directories that are called in find

```
[cs15lfa22lc@ieng6-201]:docsearch:188$ find technical/911report -type f -iname "chapter*"
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
[cs15lfa22lc@ieng6-201]:docsearch:189$ find technical/911report -type f -iname "13*"
[cs15lfa22lc@ieng6-201]:docsearch:190$ find technical/911report -type f -iname "chapter-13*"
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
[cs15lfa22lc@ieng6-201]:docsearch:191$ find technical/911report -type f -iname "chapter-13*" -delete
[cs15lfa22lc@ieng6-201]:docsearch:192$ find technical/911report -type f -iname "chapter*"        
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
```

* We first call all the "chapter-13" files in the technical/911report directory to see if the correct files will be called. Then we delete those files and call all the files in the 911report directory to see that all the "chapter-13" files have been cleared. 

```
[cs15lfa22lc@ieng6-201]:docsearch:193$ find technical -iname "tech*"
technical
technical/government/Env_Prot_Agen/tech_adden.txt
technical/government/Env_Prot_Agen/tech_sectiong.txt
[cs15lfa22lc@ieng6-201]:docsearch:195$ find technical -type f -iname "tech*" -delete
[cs15lfa22lc@ieng6-201]:docsearch:197$ find technical -iname "tech*"
technical
```

* We call all the files and directories that contain "tech" which consist of the technical directory and two files. Then, we delete specifically the two files with -type f, and then when using the same command line, we see that only the technical directory is called. 

```
[cs15lfa22lc@ieng6-201]:docsearch:199$ find technical/911report -type d -iname "chapter*" -delete
[cs15lfa22lc@ieng6-201]:docsearch:200$ find technical/911report -iname "chapter*"
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
```

* We called all directories in technical/911report that contained "chapter" and deleted them. However, as no directories exist with this condition, nothing happens and when we print out the directory, we see that there has been no effect and all the files are called.  