# Lab Report #4
## 1. Log into ieng6 :
![Image](https://cdn.discordapp.com/attachments/368995972975558656/1084718631516115004/login.PNG)
- I had already set up my keygen in lab and I have my login in my computer notes so I `<ctr+c>` my ieng and then in my terminal, I used `<ctr+v>` to paste it into my terminal then used `<enter>` to complete my login. 
## 2. Clone your fork of the repository from your Github account - Run the tests, demonstrating that they now succeed
![Image](https://cdn.discordapp.com/attachments/368995972975558656/1084719242588471366/image.png)
After I grabbed the ssh link from the git repository with `<ctr+c>`, I went back to my terminal and typed `git clone <ctr+v>`.
## 3. Run the tests, demonstrating that they fail
![Image](https://cdn.discordapp.com/attachments/368995972975558656/1084724659662114938/Screen_Shot_2023-03-12_at_11.28.13_PM.png)
In order to be in the lab 7 directory, I used `<cd lab7>`. I then went onto the lab 3 website and used `<ctr+c>` to copy the compile command `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and then pasted into my terminal with `<ctr+v>` and preseed `<enter>`. Then I go back and`<ctr+c>` the line `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore` and press `<ctr+v>` in my terminal and typed `ListExamplesTests.java>` at the end of that and hit `<enter>`. 
## 4. Edit the code file to fix the failing test 
![Image](https://media.discordapp.net/attachments/368995972975558656/1079944547544608799/Screen_Shot_2023-02-27_at_5.00.19_PM.png?width=1296&height=843) 
After that failed, I went into the file by typing `nano ListExamples.java` and figured out the issue. To look through the code, I used the scroll wheel rather than manually pressing `<downarrow>`. It was an infinite loop so I changed `index1` to `index2`. After I was done editing I used the sequence of keys `ctr+o`+`ctr+m-a`+`ctr+x` to save and exit. 

## 5. Run the tests, demonstrating that they now succeed
![Image](https://cdn.discordapp.com/attachments/368995972975558656/1084724659431415838/Screen_Shot_2023-03-12_at_11.24.21_PM.png)
After exiting, to recompile it, I went `<up><up><up>` and `<enter>` to run the first compile line. Then I went up four times again `<up><up><up><up>` + `<enter>` to get the second compile line from earlier and saw that the tests now passed.

## 6. Commit and push the resulting change to your Github account
![Image](https://cdn.discordapp.com/attachments/368995972975558656/1079951588514340966/Screen_Shot_2023-02-27_at_6.21.38_PM.png)
I typed `git add ListExamples.java`. Next I used `git commit` and typed in my message `awesome sauce index1->index2` and used `<esc> :wp <enter> <shift+z> <shift+z>` to exit the commit. Lastly I used `git push` + `<enter>` to push the changes onto my GitHub account. 
