# Code Clones: Hands-on Lecture

This repository presents a practical lecture on using Code Clones Tools.

## Task 1: Manual Code Clone Detection (10 min)

We start with the ultimate clone detector: the developer. Look at the folder ```ShortCodeExample''' and open the Java Class inside of it on your favorite IDE. Try to find pieces of code that seem to be close related for about 10 minutes. 

Questions:
- Can you detect duplication with your bare eyes?
- Which methods seem to be similar?

Main lesson: Manual clone detection does not scale very well. We will therefore use some tools to do the tedious comparisons.

## Task 2: Automated Small Scale Clone Detection (10 min)

Let's use an automated tool for duplicate detection, [Dude](http://wettel.github.io/dude.html). This tool uses line similarity to find clones. 
Now, we will use Dude to detect clones on the ```ShortCodeExample/DuplicationSuspect.java''' file. 

Download and execute Dude. Since it is a java executable, Dude should run on any platform with a JVM. On the main interface, click on the "Home/House" icon (or menu 'Search' -> 'Set starting directory') and select the folder with ```ShortCodeExample'''. Make sure there are no other files in this folder otherwise Dude will also try to detect clones on them. Then click on the 'Search' icon (or menu 'Search' -> 'Search').

Questions:
- How easy was to use this tool?
- Did the tool detect more or fewer duplicates than you?
- Can you determine any refactoring candidates based on this tool output?

Main lesson: Any laborious activity may be much better served by an automated tool. I am positive, this tool detected more clones than you did in much less time. Code clones is one of the major smells for refactoring, therefore, this tool could be very useful.

## Task 3: Customizing Small Scale Clone Detection (10 min)

Lets change some of the parameters on Dude, and see how that could affect the clone detection.

Click on the "Wrench"icon (or menu 'Search' -> 'Configure Parameters'). Change the 'Line Comparison Strategy' option to 'Tokenized Distance'. Moreover, make sure the Similarity Threshold is at 80%. After confirming the new configuration, click on the 'Search' icon again (or menu 'Search' -> 'Search'). 

Questions:
- By chaging the configuration, did the tool detected more clones?
- How is it different to set the parameters for exact matching (the default configuration) compared to other similarities? 

Try to change other parameters of DuDe and see how that affects the detected clones. The minimum size of the duplication chain (min SDC) is the threshold based on which we filter the insignificant results. The maximum line biax (max LB) is the maximum length of the gap that is allowed to link two consecutive exact chunks within a duplication chain. The minimum size of the exact chunk (min SEC) is the smallest size for a exact chain allowed to be part of a duplication chain.

## Task 4: 


http://wettel.github.io/dude.html

https://www.txl.ca/txl-nicaddownload.html

https://sourceforge.net/projects/freemercator/
