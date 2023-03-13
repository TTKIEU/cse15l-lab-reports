# Lab Report #5

## Reflection on Lab Report #3
For lab report #3, I chose to focus on the command `grep`. For me, since I didn't particularly know grep that well, I just searched up "grep cheat sheet" and from the list that I found, I chose a couple few to start with. Then from that, I searched up "grep -v" and I drifted toward a video which helped me walkthrough and understand the commands. Conveniently, the video also contained other commands that I was interested in so I just relied on that. When using them in my terminal, I tried using the same test case to show how they took the same input and outputted different things. It helped me prepare for the skill demo which I mainly used `grep` to find things in files. 

## Doing the task with `find`

## -type
  Finds all the files of a certain type. It's useful for when you only want to look at one file type or when you need to sort your folder. 
  
  `find .-type d`
 ![Image](https://cdn.discordapp.com/attachments/368995972975558656/1084934160768049272/Screen_Shot_2023-03-13_at_1.19.12_PM.png)
 
 `find .-type f`
 ![Image](https://cdn.discordapp.com/attachments/368995972975558656/1084936455761166407/Screen_Shot_2023-03-13_at_1.29.42_PM.png)
 Source: [https://quickref.me/find](https://quickref.me/find)
 
## -name
  Finds all the files with a certain string/name. It's useful for precisely searching through a folder for a certain file you have in mind. 
  
  `find -f .-name "*.txt"
  ![Image](https://media.discordapp.net/attachments/368995972975558656/1084934886277783733/Screen_Shot_2023-03-13_at_1.21.31_PM.png?width=1948&height=784)
  
  `find -f .-name "* WhatToDo.txt"`
  ![Image](https://cdn.discordapp.com/attachments/368995972975558656/1084940284447703060/Screen_Shot_2023-03-13_at_1.44.07_PM.png)
  Source: [https://quickref.me/find](https://quickref.me/find)
  
 ## -size 
 Finds files either greater of less than the specified size. Using `+` or `-` determines if you're finding files greater or less than that size. This helps eliminate big files or small fines. 
 
 `find .-size +80c`
 ![Image](https://cdn.discordapp.com/attachments/368995972975558656/1084942419067408434/Screen_Shot_2023-03-13_at_1.51.08_PM.png)
 
 `find .-size +1k`
 ![Image](https://media.discordapp.net/attachments/368995972975558656/1084942419302297830/Screen_Shot_2023-03-13_at_1.51.47_PM.png?width=1494&height=842)
  Source: [https://quickref.me/find](https://quickref.me/find)

## -maxdepth
  Finds files in the given depth of directores/subdirectories. It's useful for isolation files of a certain type or name in a directory or subdirectories. 
  `find .-maxdepth 3 -name "* .txt"
  ![Image](https://media.discordapp.net/attachments/368995972975558656/1084944635140513802/Screen_Shot_2023-03-13_at_2.00.13_PM.png?width=1948&height=92)
  
  `find .maxdepth 4 -name "*.txt"`
  ![Image](https://media.discordapp.net/attachments/368995972975558656/1084944635501228053/Screen_Shot_2023-03-13_at_2.02.10_PM.png?width=1948&height=722)
   Source: [https://quickref.me/find](https://quickref.me/find)
