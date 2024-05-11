# Assignment 1

**Due:** ?

**Instructions:** 
  * Please turn in the answers to this assignment as a .txt document. To create a .txt document in R, go to **New File**, then select **Text file**. You can use any other text editor if you like. Please do not use Mac's Text Edit application, though.
  * DO NOT include the questions in the document you turn in. Answers only!
  * TURN in your assignment on canvas
  * If you are already versed in R, please feel free to substitute out any questions with the [BONUS Content](#bonus-content) at the end of this document. 
  
:white_check_mark: These are the learning objectives associated with each question

-----

## QUESTION 1 (5 pts) 

:white_check_mark: The purpose is to build curiosity. Students can imagine what R packages will work for their individual goals and projects.

A. Answer the following: **What is your field of research?** You can use a rotation project or in-lab project. If you don't have a designated field of research, what is a field you would like to move into in the future?

I work in systematics. It's the study of evolutionary relationships between biological information units, be they point mutations, genes, genomes, species, or higher taxa. I have a particular interest in parasite systematics, as they're incredibly challenging for modern methods to deal with, exposing problems with the field as a whole. 

B. Think about the research you would like to do. Use the [Bioconductor Website](https://www.bioconductor.org/) to explore topics that are relevant to you. Answer the following: **What are the names and url's of 2 - 3 packages you would be interested to learn more about?**

GO.db
https://www.bioconductor.org/packages/release/data/annotation/html/GO.db.html

This package performs gene ontology analyses on datasets just like the one's I've generated for my current project on parasitic plants. 

BUS
https://www.bioconductor.org/packages/release/bioc/html/BUS.html

BUS estimates the interactions between macromolecules and genes, which could be useful for analyzing my gene similarity matrices. Could also come in handy once I get my hands on existing protein structures of these genes' products, or reconstruct protein structures for uncharacterized genes I find. 

RCy3
https://www.bioconductor.org/packages/release/bioc/html/RCy3.html

This is just a network display package which could be useful for displaying the interactome of gene coevolution I hope to reconstruct. 

C. Evaluate the documentation your packages have available. Compare the documentation between the 2 - 3 packages you selected. Answer: **Which packages appear easier to learn and why?**

RCy3 wouldn't talke long to learn at all. It's just a graphical display package. I imagine most of the headaches would have to do with my data structure and commands which call various functions in RCy3. Once I make all the easy mistakes, it should be simple to plug along. 
Gene ontology would be pretty easy to learn since many of my colleagues have done it and could lend me a hand. 
BUS looks completely foreign to me, and the documentation doesn't look very extensive. 

## QUESTION 2 (5 pts)

:white_check_mark: Students will learn how to interface with R and RStudio

*Let's explore R-studio a little bit by learning about shortcut keys. Try the following and report what happens: (answers in words, phrases, or short sentences)**

A. What happens when you press **Alt+Shift+K** on a PC/Linux or **Option+Shift+K** on a Mac?

It brings up an overlay of the keyboard shortcut guide. 

B. What happens when you are working on the "Console" and you press the **up arrow**?

It loads the previously entered console command to the current line. 

C. What happens when you are working on the "Console" and you press **CTRL+L**?

This clears the console but preserves previously entered commands for recovery via the up arrow. 

D. What shortcut key helps you escape out of an executed command on the "Console"? For example, try executing a sleep function. This puts R to sleep for 5 minutes. (in other words - What would you press to return to the prompt before 5 minutes is complete?)

Ctrl-C

```r
Sys.sleep(5)
```


-----


## QUESTION 3 (5 pts) 

:white_check_mark: Students will become familiar with a few basic R objects - vectors

:white_check_mark: Students will execute a few basic R functions

*We learned that vectors come in different classes depending on the data type they house. Answer the following in phrases or sentences.*

A. What are the classes of each of these vectors? 
```r
users <- c("alvin", "viet", "leila")
class(users)
logins <- c(12, 5, 34)
class(logins)
```

B. If we merge these vectors together into super_vector by concatenating them together (below), what is the class of super\_vector? Why do you think this happened?

```r
super_vector <- c(users, logins)
class(super_vector)
```

C. How would you force super\_vector into a numeric sub-class? *write the line of code* What happens? *copy the output and write a sentence explanation*

-----

## QUESTION 4 (5 pts) 

:white_check_mark: Students will become familiar with a few basic R objects - data frames

:white_check_mark: Students will execute a few basic R functions

Heather has written some code to create a data frame with columns for "languages", "greetings", and "partings". Each line of her code except the last line has a bug, or error. Can you de-bug Heather's code? Submit the re-written code.

```
# Heather's code:
languages <- ("English", "Spanish", "Japanese", "French")
_greetings_ <- c("hello", "hola", "ohio", "bonjour")
partings < c("bye", "adios", "mata", "salut")
dictionary <- DataFrame(languages, _greetings_, partings)
dimens(dictionary)
dictionary

```

*Hint: The final line of code should give you the following output:*

```
  languages greetings partings
1   English     hello      bye
2   Spanish      hola    adios
3  Japanese      ohio     mata
4    French   bonjour    salut
```

Turn in the amended code block.

-----


## QUESTION 5 (5 pts)

Let's practice importing some data. Here is a real supplementary dataset that my lab recently published for a manuscript. 

[Table_S4_Signal_to_noise_quantification_table.csv](https://drive.google.com/file/d/1bJy_ELikr5F264xRe-ASNI4iXBVYuxIP/view?usp=sharing)

  * Download the file to your computer.
  * Ensure your working directory is set properly
  * Import the dataset into R using `read.csv()` and save it as an object called `signal_to_noise`
  * Note - .csv stands for "comma separated value"
  * What is the output of `str(signal_to_noise)`? **Copy and paste it here as the answer to this question.**
  * If you were NOT able to get this to work, please explain what you tried, what is going wrong, and any output or error messages you are getting.

-----

# Bonus content

:white_check_mark: Students are encouraged to cultivate their own personal curiosity in R, data science, and programming. Feel free to turn in any of these answers in lieu of Question 1 - 5 if you are experienced user.

  1. Explore the [Base R Cheatsheet](https://iqss.github.io/dss-workshops/R/Rintro/base-r-cheat-sheet.pdf)
  
   What is a function or object you haven't used before? Explore it. Write down what you tried and how it works. Submit code showing what you have done.
    
  2. Explore the [R Graph Gallery](https://www.r-graph-gallery.com/index.html).
  
   Choose a category of R plots that you would like to learn more about. Using the R Graph Gallery pages, wikipedia, and other internet resources, learn how these plots generate their data. Think about which plots you might use in your own research. 

   Next, read through some of the R code in the Gallery associated with each plot. Even if you don't understand the R code, just give it a try. Notice the difference between reading the comments versus the code.

   Write down the type of plot you explored and describe how you would like to use it in your work.

  3. Explore [Our World In Data](https://ourworldindata.org/).

   Click on **Articles By Topic** to activate a pull down menu to explore. You can download any dataset you want. 

   For example, if you go to [Internet access per country over time](https://ourworldindata.org/internet#internet-access), you can see different plots like so...

<img src="webContent/Screen Shot 2023-01-23 at 6.00.02 AM.png" width="600">

   You can select the **Download** menu tab at the bottom, and download the full dataset as a .csv file. Try it! Explore the data you've obtained!

<img src="webContent/Screen Shot 2023-01-23 at 6.00.16 AM.png" width="600">


    Try downloading and importing some of this data. Make a plot. Explain and turn in what you did. 
