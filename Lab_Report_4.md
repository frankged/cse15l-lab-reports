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
`<enter`
<img width="735" alt="Screen Shot 2023-02-24 at 12 40 44 AM" src="https://user-images.githubusercontent.com/97646090/221132324-cb4bcb8f-30f2-428a-a02e-e35f7845e978.png">
  
This is the expected output from the code block complete with steps 5-9.

### Breakdown 

Step 5:  
`git clone git@github.com:frankged/lab7.git` `<enter>`
<img width="528" alt="Screen Shot 2023-03-11 at 11 44 43 AM" src="https://user-images.githubusercontent.com/97646090/224508523-e25dc413-5ba9-44a8-9bd2-f44d94685412.png">  

Step 6:
`cd lab7/`  
`<enter`
`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`  
`<enter`
`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`  
`<enter`

<img width="730" alt="Screen Shot 2023-03-11 at 11 48 01 AM" src="https://user-images.githubusercontent.com/97646090/224508659-bf6f5e26-07de-435b-b873-75e2fe9c5662.png">  

Step 7:  
<img width="259" alt="Screen Shot 2023-03-11 at 11 50 50 AM" src="https://user-images.githubusercontent.com/97646090/224508783-4270df6a-2fa6-4af2-8694-022d5eaf89d8.png">

`sed -i '43s/.*/index2 += 1;/' ListExamples.java`
`<enter`

<img width="262" alt="Screen Shot 2023-03-11 at 11 51 35 AM" src="https://user-images.githubusercontent.com/97646090/224508817-162ccea8-e07a-4970-88e4-93a96bef445b.png">  

Step 8:  

`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java ; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`
`<enter`


<img width="733" alt="Screen Shot 2023-03-11 at 11 53 37 AM" src="https://user-images.githubusercontent.com/97646090/224508886-c441f153-ec17-4909-9568-d45eabc946d0.png">

Step 9:
`git add ListExamples.java`  
`<enter`  
`git commit -m “done”`  
`<enter`  
`git push`  
`<enter`  

<img width="521" alt="Screen Shot 2023-03-11 at 11 58 07 AM" src="https://user-images.githubusercontent.com/97646090/224509069-340050cd-c92e-4319-abf8-1fdcd959f954.png">


