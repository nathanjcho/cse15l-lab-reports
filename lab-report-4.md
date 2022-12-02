# Lab Report 4


**Part One**



* The task that I chose to do from the week 6 lab in less than 30 inputs is "In DocSearchServer.java, change the name of the start parameter of getFiles, and all of its uses, to instead be called base." 
* To start I git cloned the repository `git clone https://github.com/ucsd-cse15l-f22/skill-demo1 week6-skill-demo1` and changed my directory into week6-skill-demo1. 
* Then in the terminal I typed in vim DocSearchServer.java which brought up file in my terminal as shown below. 

![step1](step1.png)

* The first command I put in vim was `:%s/start/base/gc` which searches for every instance of start and replaces every instance of start to base. I then pressed `<enter>` to execute the command which brought me here. 

![step9](step9.png)
![step2](step2.png)

* I then pressed `y` which successfully found the first instance of start and replaced it with base. It then found the second instance of start. 

![step3](step3.png)

* I pressed `y` `y` afterwards, replacing the second and third instances of start with base. It then found the last instance of start. 

![step4](step4.png)
![step5](step8.png)

* On the last instance of start, we only want to replace start with base in getFiles, so I pressed `n` which skipped the start and didn't replace it. 

![step5](step5.png)

* Afterwards, I inputted`:wq` to save the files and exit vim. I then pressed `<enter>` to execute the command. This saved my changed as shown in the photo below. 

![step10](step10.png)
![step6](step6.png)

* In order, my inputs were `:%s/start/base/gc`, `<enter>`, `y`, `y`, `y`, `n`, `:wq`, `<enter>`. This is 26 key presses which is under our threshold of 30. 

---

**Part Two**

* The first method of making the edits locally and then using scp to copy the edits to the remote server took me 2 minutes and 6 seconds. I had difficulty getting into the correct directory in order to properly scp DocSearchServer which took me extra time. 

* The second method of sshing into the remote server and making the edits remotely took me 1 minute and 39 seconds. There were no difficulties in sshing into the server and using vim on the remote server. 

* I would choose the second method if I had to work on a program that I was running remotely as I would save time making edits on the remote server itself rather than making edits locally and then copying those edits to the remote server every time. 

* The only factor that may change my decision is if it were easier to make edits and check if they are correct locally for a specific program. If it were a larger program for example, I would rather edit and run the program on my local device to ensure that it is running correctly. Then I would only have to scp once and be ensured that my program would run on the remote server. 