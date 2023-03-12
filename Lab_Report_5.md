# Lab Report 5  
## "Done Quicker"  

`cat doneQuicker.sh` :   
`ssh cs15lwi23alt@ieng6.ucsd.edu "git clone git@github.com:frankged/lab7.git; cd lab7/; javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java ; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests; sed -i '43s/.*/index2 += 1;/' ListExamples.java; javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java ; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests; git add ListExamples.java; git commit -m “done”;git push"`  
<img width="544" alt="Screen Shot 2023-03-12 at 2 06 13 PM" src="https://user-images.githubusercontent.com/97646090/224573715-96c82495-443c-4518-b8ed-9c71cc3fa82f.png">
  
This script uses the exact same commands as in my Lab 4. Interestingly enough, this script is a single line of commands, meaning that using a script isn't any faster than copy-pasting into a terminal. Through constructing this, I realize that my "done quick" solution could have been the same speed as a bash script.
