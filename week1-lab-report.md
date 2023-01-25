# Week 1 Lab Report 
## Accessing my CSE15L account
[UCSD Account LookUp](https://sdacs.ucsd.edu/~icc/index.php)
I clicked the link above and entering in my credentials and scrolling down till I saw "_Additional Accounts_" with my CSE15L username boxed. I was then prompted to change my password through the "_Global Password Change_". After choosing a password for my account, I made sure to only change my password for the CSE15L account specifically.

## Remotely Connecting and Installing VSC
I already had VSC installed but in the chance that you don't, goto the [Visual Studio Code Website](https://code.visualstudio.com/) and click download. After agreeing with the License Agreement, setup based on preferences and click finish. Launch Visual Studio Code and it will open. This is what my VSC looks like on default:
![Image](https://media.discordapp.net/attachments/368995972975558656/1063181555352211516/Screen_Shot_2023-01-12_at_10.21.07_AM.png?width=1440&height=936)

If you don't want to install it, just use your computer's built in terminal and it works the same. I'm working on a macbook so I didn't have to install git or git bash. Now to actually log in, open your terminal and enter 
* `ssh cs15lwi23zz@ieng6.ucsd.edu`
replacing zz with your own CSE15L username. 

After, I was prompted to enter in the password that I reset back when I was accessing my account credentials. I couldn't see what I was typing but I just trusted myself. If all goes well, your terminal should look like this: 
![Image](https://media.discordapp.net/attachments/368995972975558656/1063180340182663209/Screen_Shot_2023-01-12_at_11.38.14_AM.png)

## Running Commands 
I was a bit late to the login step so I was looking for commands my teammates hadn't used yet. I first listed all the files in my current directory and then opened `hello.txt` with cat. Then I tried using `ls /home/…` without putting `ls` in front which verifies that my classmate’s directory does exist. When I attempted again with `ls`, not captured within the screenshot, I got a message saying that my permission was denied.
![Image](https://media.discordapp.net/attachments/368995972975558656/1063180867419250698/Screen_Shot_2023-01-12_at_10.50.31_AM.png)

## Creating this website
I had a preexisting github account so all I needed to do was create a new repository and add .md to the new file I created within it. I played around with my website and created this with markdown features:
![Image](https://media.discordapp.net/attachments/368995972975558656/1063182701647101962/Screen_Shot_2023-01-12_at_11.47.59_AM.png?width=786&height=935)

