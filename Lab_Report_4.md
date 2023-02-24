# Lab Report 4
## "Done Quick"
In order to complete the task, I had to open a terminal, fork the proper repository, and have the string below in my clipboard.  
```
git clone git@github.com:frankged/lab7.git; cd lab7/; javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java ; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples; sed -i '43s/.*/index2 += 1;/' ListExamples.java; javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java ; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples; git add ListExamples.java; git commit -m “done”;git push
```
Once this setup is complete, the remaining keystrokes were:  
`<up>` (to bring up my ssh login which is the first item in my local history)  
`<enter>` (to login, there was no need to type a password because of the ssh key saved from earlier in the lab)  
`Ctrl-V`  (to paste the aforementioned string into the remote server)  
`<enter>` (to run what I had pasted into the terminal)  
and the task was complete.

Step 2:  
<img width="697" alt="Screen Shot 2023-02-24 at 12 26 31 AM" src="https://user-images.githubusercontent.com/97646090/221129462-57260075-21e1-4321-97f6-bc9dbb13b28b.png">

Step 4:  
<img width="696" alt="Screen Shot 2023-02-24 at 12 22 14 AM" src="https://user-images.githubusercontent.com/97646090/221128624-22a78acd-c596-491b-89f8-85c16be55320.png">

Steps 5-9:  

<img width="795" alt="Screen Shot 2023-02-24 at 12 30 22 AM" src="https://user-images.githubusercontent.com/97646090/221130220-57e10445-5211-4ccd-9a73-1d9780928cfa.png">
  
Let it be noted that as of the current moment, the above code block will not work due to the names of the Lab 7 files being changed. However, this issue has the simple fix of changing each instance of "TestListExamples" to "ListExamplesTests".
This new "updated" version with the correct file names works great!  
```
git clone git@github.com:frankged/lab7.git; cd lab7/; javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java ; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests; sed -i '43s/.*/index2 += 1;/' ListExamples.java; javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java ; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests; git add ListExamples.java; git commit -m “done”;git push
```
<img width="735" alt="Screen Shot 2023-02-24 at 12 40 44 AM" src="https://user-images.githubusercontent.com/97646090/221132324-cb4bcb8f-30f2-428a-a02e-e35f7845e978.png">
  
This is the expected output from the code block complete with steps 5-9.
