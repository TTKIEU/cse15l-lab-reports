# Lab Report #4
## 1. Log into ieng6 :
![Image](https://media.discordapp.net/attachments/368995972975558656/1079944410302791801/Screen_Shot_2023-02-26_at_9.11.11_PM.png?width=1296&height=843)
1. Typing in ssh-keygen
    `<enter><enter><enter>`
2. copy and paste my ssh ieng6 login from a note sheet: `<cmd+c><cmd+v>`
3. Typed in `mkdir .ssh` and then `exit` to log out
4. I used `<cmd+f>` to find public key in my terminal and copy and pasted that `<cmd+c><cmd+v>` into the recent line of my terminal with ssh and copy and paste `<cmd+c><cmd+v>` my ieng6 username + `:~/.ssh/authorized_keys` from the 15L website.
5. After I manually enter my password, I go up a few times `<up><up><up><up><up>` until I reach my original ssh login from step 1 and `<enter>`. 
## 2. Clone your fork of the repository from your Github account - Run the tests, demonstrating that they now succeed
![Image](https://cdn.discordapp.com/attachments/368995972975558656/1079945376196468796/Screen_Shot_2023-02-27_at_5.57.04_PM.png)
1. Grab the ssh link from the git repository 
2. I went back to my terminal and typed `git clone <ctr+v>`
3. I used cd'd into `lab7`
4. I then used `<ctr+c><ctr+v>` `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`
5. Then I `<ctr+c>` from the website and `<ctr+v>` `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore + ListExamplesTests.java>`
6. After that failed, I went into the file with `nano ListExamples.java` and figured out the issue. It was an infinite loop so I changed `index1` to `index2`. ![Image](https://media.discordapp.net/attachments/368995972975558656/1079944547544608799/Screen_Shot_2023-02-27_at_5.00.19_PM.png?width=1296&height=843)
7. After I was done editing I used `ctr+x` to exit and `enter`
8. To recompile it, I went `<up><up><up>` and `<enter>` to run step 4. Then I went up four times again to get step 5 `<up><up><up><up>` + `<enter>` and saw that the tests now passed.

## 3. Commit and push the resulting change to your Github account
![Image](https://cdn.discordapp.com/attachments/368995972975558656/1079951588514340966/Screen_Shot_2023-02-27_at_6.21.38_PM.png)
1. I typed `git add ListExamples.java
2. Next I used `git commit` and typed in my message `awesome sauce index1->index2` and used `<esc> :wp <enter> <shift+z> <shift+z>` to exit the commit
3. Lastly I used `git push`
