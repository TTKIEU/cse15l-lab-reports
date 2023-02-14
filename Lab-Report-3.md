# Lab Report 3 
## Grep command line options:
  
  ### `-v` : Prints every line but the String after grep
   ![Image](https://media.discordapp.net/attachments/368995972975558656/1074862583636574248/Screen_Shot_2023-02-13_at_5.19.03_PM.png?width=1840&height=1197)
   ![Image](https://media.discordapp.net/attachments/368995972975558656/1074862583636574248/Screen_Shot_2023-02-13_at_5.19.03_PM.png?width=1840&height=1197)
   In image one, I omit "Chapter 1" with `grep -v Chapter 1 ch1.txt`
   
   ```
   grep -v Chapter 1 ch1.txt   
grep: 1: No such file or directory
ch1.txt:
ch1.txt:
ch1.txt:
ch1.txt:
ch1.txt:Prolegomenon to a General Biology
```
   
   In image two, I omit "Chapter 10" with `grep -v Chapter 10 ch10.txt`
   
   ```
   grep -v Chapter 10 ch10.txt 
grep: 10: No such file or directory
ch10.txt:
ch10.txt:
ch10.txt:
ch10.txt:
ch10.txt:A Coconstructing Cosmos?
```

   `Grep -v` is used to return every line that does not contain the specified string. It's useful for when you want to leave out or get rid of sentences that contain a certain String. 
   I used Learn Linux TV's [Linux Crash Course - The grep Command](https://www.youtube.com/watch?v=Tc_jntovCM0&ab_channel=LearnLinuxTV) video at 3:58.
   
 ### `-n` : Returns the line and the line number in which it is found
   ![Image](https://media.discordapp.net/attachments/368995972975558656/1074864247709909133/Screen_Shot_2023-02-13_at_5.26.23_PM.png)
   ![Image](https://cdn.discordapp.com/attachments/368995972975558656/1074864247382749184/Screen_Shot_2023-02-13_at_5.25.35_PM.png)
   In image one, I grep'd "astrobiology" with `grep -n astrobiology ch1.txt`
    
```
grep -n astrobiology ch1.txt

47:In the summer of 1997, NASA was busy attempting to formulate what it came to call “astrobiology,” an attempt to understand the origin, evolution, and characteristics of life anywhere in the universe. Astrobiology does not yet exist = it is a field in the birthing process. Whatever the area comes to be called as it matures, it seems likely to be a field of spectacular success and deep importance in the coming century. A hint of the potential impact of astrobiology came in August 1997 with the tentative but excited reports of a Martian meteorite found in Antarctica that, NASA scientists announced, might have evidence of early Martian microbial life. The White House organized the single-day “Space Conference,” to which I was pleased to be invited. Perhaps thirty-five scientists and scholars gathered in the Old Executive OYce Building for a meeting led by Vice President Gore. The vice president began the meeting with a rather unexpected question to the group: If it should prove true that the Martian rock actually harbored fossilized microbial life, what would be the least interesting result? 
```

  In image two, I grep'd "cosmos" with `grep -n cosmos ch10.txt`.
 
``` 
grep -n cosmos ch10.txt  

7:rom biospheres to the cosmos? Yes, because they may share general themes. The major enquiry of Investigations has concerned autonomous agents and their coconstruction of biospheres and econospheres whose configuration spaces cannot be finitely prestated. These themes find echoes in thinking about the cosmos as a whole. But abundant caution: I am not a physicist, the problems are profound, and we risk nonsense.
13:The universe is enormously complex, and we don’t really yet know why. May there be new ways of thinking of the cosmos itself? If a mere glimmer can be acceptable as potentially useful early science, then the burden of this chapter is to suggest perhaps, yes.
```

`Grep -n` is used to return every line that contains the string aswell as the line number that it's on. It's useful to find words in a file and it makes it easier to look for them, given the line number.

I used Learn Linux TV's [Linux Crash Course - The grep Command](https://www.youtube.com/watch?v=Tc_jntovCM0&ab_channel=LearnLinuxTV) video at 7:37.

### `-c` : String count in a file

![Image](https://media.discordapp.net/attachments/368995972975558656/1074868038236643478/Screen_Shot_2023-02-13_at_5.41.05_PM.png)

In the first line, I searched for astrobiology in ch1.txt with `grep -c astrobiology ch1.txt`
  
  ```
  grep -c astrobiology ch1.txt
2
```

In the second line, I searched for cosmos in ch10.txt with `grep -c cosmos ch10.txt` 

```
grep -c cosmos ch10.txt
2
```

Using the examples from `-n` I can tell that these results are right. It returns the count of how many times a String is used. It's useful for finding how frequently a word pops up in a text.
I used Learn Linux TV's [Linux Crash Course - The grep Command](https://www.youtube.com/watch?v=Tc_jntovCM0&ab_channel=LearnLinuxTV) video at 8:07.

### `-r` : Recursively reads all the files in a directory
 
 ![Image](https://cdn.discordapp.com/attachments/368995972975558656/1074872048536526848/Screen_Shot_2023-02-13_at_5.57.12_PM.png)
 ![Image](https://cdn.discordapp.com/attachments/368995972975558656/1074872276534702130/Screen_Shot_2023-02-13_at_5.58.17_PM.png)
 
 In image one, I grep'd "cosmos" from the OUP directory with `grep -r cosmos`
 
 ```
 grep -r cosmos
./Kauffman/ch3.txt:Some wellspring of creation, lithe in the scattered sunlight of an early planet, whispered something to the gods, who whispered back, and the mystery came alive. Agency was spawned. With it, the nature of the universe changed, for some new union of matter, energy, information, and something more could reach out and manipulate the world on its own behalf. Selfish? Yes. But how does matter, energy, information, and something else miraculous become selfish? From that miracle grew a biosphere = and, we must surmise, from that grow other biospheres, scattered seeds and gardens across the cosmos.
./Kauffman/ch1.txt:My first eVorts had begun with twin questions. First, in addition to the known laws of thermodynamics, could there possibly be a fourth law of thermodynamics for open thermodynamic systems, some law that governs biospheres anywhere in the cosmos or the cosmos itself? Second, living entities = bacteria, plants, and animals = manipulate the world on their own behalf: the bacterium swimming upstream in a glucose gradient that is easily said to be going to get “dinner”; the paramecium, cilia beating like a Roman warship’s oars, hot after the bacterium; we humans earning our livings. Call the bacterium, paramecium, and us humans “autonomous agents,” able to act on our own behalf in an environment.
./Kauffman/ch1.txt:Might collective autocatalysis of proteins or similar polymers be the basic source of self-reproduction in molecular systems? Or must life be based on template replication, as envisioned by Watson and Crick, or as envisioned even earlier by Schrödinger in his aperiodic solid with its microcode? In view of the potential for a general biology, what, in fact, are the alternative bases for self-reproducing molecular systems here and anywhere in the cosmos? Which of these alternatives is more probable, here and anywhere?
./Kauffman/ch1.txt:Here are hints = common law, ecosystems, economic systems = that general principles govern the coevolutionary coconstruction of lives and livings, organisms and natural games, firms and economic opportunities. Perhaps such a law governs any biosphere anywhere in the cosmos.
./Kauffman/ch7.txt:rom a biosphere and its mysteries, this investigation now steps gingerly toward the cosmos. Caveat lector: I am not a physicist.
./Kauffman/ch10.txt:rom biospheres to the cosmos? Yes, because they may share general themes. The major enquiry of Investigations has concerned autonomous agents and their coconstruction of biospheres and econospheres whose configuration spaces cannot be finitely prestated. These themes find echoes in thinking about the cosmos as a whole. But abundant caution: I am not a physicist, the problems are profound, and we risk nonsense.
./Kauffman/ch10.txt:The universe is enormously complex, and we don’t really yet know why. May there be new ways of thinking of the cosmos itself? If a mere glimmer can be acceptable as potentially useful early science, then the burden of this chapter is to suggest perhaps, yes
```

In image two, I grep'd "astrobiology" from the OUP directory with `grep -r astrobiology`

```
grep -r astrobiology
./Kauffman/ch1.txt:In the summer of 1997, NASA was busy attempting to formulate what it came to call “astrobiology,” an attempt to understand the origin, evolution, and characteristics of life anywhere in the universe. Astrobiology does not yet exist = it is a field in the birthing process. Whatever the area comes to be called as it matures, it seems likely to be a field of spectacular success and deep importance in the coming century. A hint of the potential impact of astrobiology came in August 1997 with the tentative but excited reports of a Martian meteorite found in Antarctica that, NASA scientists announced, might have evidence of early Martian microbial life. The White House organized the single-day “Space Conference,” to which I was pleased to be invited. Perhaps thirty-five scientists and scholars gathered in the Old Executive OYce Building for a meeting led by Vice President Gore. The vice president began the meeting with a rather unexpected question to the group: If it should prove true that the Martian rock actually harbored fossilized microbial life, what would be the least interesting result? 
./Kauffman/ch1.txt:A general biology awaits us. Call it astrobiology if you wish. We confront the vast new task of understanding what properties and laws, if any, may characterize bio-spheres anywhere in the universe. I find the prospect stunning. I will argue that the concept of an autonomous agent will be central to the enterprise of a general biology.
```

`Grep -r` is used when you want to find a String within a directory of files. It's used to make the search process easier by going through every file and finding the String instead of manually cd'ing and grepping into each individual file. I used [Linux Command](https://linuxcommand.org/lc3_man_pages/grep1.html)


   
   
