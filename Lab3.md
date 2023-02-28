# The -find Command
#### Below we will explore four different ways we can use the "-find" terminal command which uses the syntax:
`find [path] [expression]`

#### In all examples we will be working within the ../skill-demo1-data/written_2 directory within the ssh server 

*All commands were found using chatGBT [click here for a link to the copy of the chat](https://docs.google.com/document/d/1hYW7CyUJ-t4eKVQHVktVMLhEMzHA57P4zT7Q97ptr8o/edit?usp=sharing)

## The -name expression
The -name command specifies find to search for files based on their name.

Syntax: find [path] -name [pattern]

* Example 1: If we want to quickly look for a specific single file, perhaps to know where it's located or if it exists, -name can be very useful. In the example below, we find the file "IntroEgypt". 
  
  Command: `./travel_guides/berlitz1/IntroEgypt.txt`
  
  Output: 
``
./written_2/travel_guides/berlitz1/IntroEgypt.txt``

* Example 2: Similarly, we can use the -name option more generally to find a specific character or phrase. Let's say we quickly want to find all the History txt files in travel_guides, the example below implements. The command has find search for files start with the "History" in their name, and end with ".txt". 
 
  Command: `find -name History*.txt`
  
  Output:
``
./travel_guides/berlitz1/HistoryDublin.txt
./travel_guides/berlitz1/HistoryEdinburgh.txt
./travel_guides/berlitz1/HistoryEgypt.txt
./travel_guides/berlitz1/HistoryFWI.txt
./travel_guides/berlitz1/HistoryFrance.txt
./travel_guides/berlitz1/HistoryGreek.txt
./travel_guides/berlitz1/HistoryHawaii.txt
./travel_guides/berlitz1/HistoryHongKong.txt
./travel_guides/berlitz1/HistoryIbiza.txt
./travel_guides/berlitz1/HistoryIndia.txt
./travel_guides/berlitz1/HistoryIsrael.txt
./travel_guides/berlitz1/HistoryIstanbul.txt
./travel_guides/berlitz1/HistoryItaly.txt
./travel_guides/berlitz1/HistoryJamaica.txt
./travel_guides/berlitz1/HistoryJapan.txt
./travel_guides/berlitz1/HistoryJerusalem.txt
./travel_guides/berlitz1/HistoryLakeDistrict.txt
./travel_guides/berlitz1/HistoryLasVegas.txt
./travel_guides/berlitz1/HistoryMadeira.txt
./travel_guides/berlitz1/HistoryMadrid.txt
./travel_guides/berlitz1/HistoryMalaysia.txt
./travel_guides/berlitz1/HistoryMallorca.txt``

## The -type expression 
The -type option specifies the type of certain file find should look for. The type of file is denoted by a single letter after a dash.
Syntax: find [path] -type [type]


* Example 1: The type option can be useful when you want to search for specific types of files or directories in a directory hierarchy. It allows us to narrow down our search results and save time. In the example below, the -type d option instructs find to only list directories. The "d" represented directories in our command.

  Command: `find -type d`

  Output:
``
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Berk
./non-fiction/OUP/Castro
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Rybczynski
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz2``

* Example 2: Maybe we are deciding where to go on vacation, and specifically want to find files that are txt files within travel_guides. In the example below we have find search for files in travel_guides, as well as the name command discussed earlier to search for specifically txt files.
  
  Command: find ../written_2/travel_guides -type f -name "*.txt"
  
  Output:
``
../written_2/travel_guides/berlitz1/HandRHawaii.txt
../written_2/travel_guides/berlitz1/HandRHongKong.txt
../written_2/travel_guides/berlitz1/HandRIbiza.txt
../written_2/travel_guides/berlitz1/HandRIsrael.txt
../written_2/travel_guides/berlitz1/HandRIstanbul.txt
../written_2/travel_guides/berlitz1/HandRJamaica.txt
../written_2/travel_guides/berlitz1/HandRJerusalem.txt
../written_2/travel_guides/berlitz1/HandRLakeDistrict.txt
../written_2/travel_guides/berlitz1/HandRLasVegas.txt
../written_2/travel_guides/berlitz1/HandRLisbon.txt
../written_2/travel_guides/berlitz1/HandRLosAngeles.txt
../written_2/travel_guides/berlitz1/HandRMadeira.txt
../written_2/travel_guides/berlitz1/HandRMadrid.txt
../written_2/travel_guides/berlitz1/HandRMallorca.txt
../written_2/travel_guides/berlitz1/HistoryDublin.txt
../written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
../written_2/travel_guides/berlitz1/HistoryEgypt.txt
../written_2/travel_guides/berlitz1/HistoryFWI.txt
../written_2/travel_guides/berlitz1/HistoryFrance.txt
../written_2/travel_guides/berlitz1/HistoryGreek.txt
../written_2/travel_guides/berlitz1/HistoryHawaii.txt
../written_2/travel_guides/berlitz1/HistoryHongKong.txt
../written_2/travel_guides/berlitz1/HistoryIbiza.txt
../written_2/travel_guides/berlitz1/HistoryIndia.txt
../written_2/travel_guides/berlitz1/HistoryIsrael.txt
../written_2/travel_guides/berlitz1/HistoryIstanbul.txt
../written_2/travel_guides/berlitz1/HistoryItaly.txt
../written_2/travel_guides/berlitz1/HistoryJamaica.txt
../written_2/travel_guides/berlitz1/HistoryJapan.txt
../written_2/travel_guides/berlitz1/HistoryJerusalem.txt
../written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt
../written_2/travel_guides/berlitz1/HistoryLasVegas.txt
../written_2/travel_guides/berlitz1/HistoryMadeira.txt
../written_2/travel_guides/berlitz1/HistoryMadrid.txt
../written_2/travel_guides/berlitz1/HistoryMalaysia.txt
../written_2/travel_guides/berlitz1/HistoryMallorca.txt
../written_2/travel_guides/berlitz1/IntroDublin.txt
../written_2/travel_guides/berlitz1/IntroEdinburgh.txt
../written_2/travel_guides/berlitz1/IntroEgypt.txt
../written_2/travel_guides/berlitz1/IntroFWI.txt
../written_2/travel_guides/berlitz1/IntroFrance.txt
../written_2/travel_guides/berlitz1/IntroGreek.txt
../written_2/travel_guides/berlitz1/IntroHongKong.txt
../written_2/travel_guides/berlitz1/IntroIbiza.txt
../written_2/travel_guides/berlitz1/IntroIndia.txt
../written_2/travel_guides/berlitz1/IntroIsrael.txt
../written_2/travel_guides/berlitz1/IntroIstanbul.txt
../written_2/travel_guides/berlitz1/IntroItaly.txt
../written_2/travel_guides/berlitz1/IntroJamaica.txt
../written_2/travel_guides/berlitz1/IntroJapan.txt
../written_2/travel_guides/berlitz1/IntroJerusalem.txt
../written_2/travel_guides/berlitz1/IntroLakeDistrict.txt
../written_2/travel_guides/berlitz1/IntroLasVegas.txt
../written_2/travel_guides/berlitz1/IntroLosAngeles.txt
../written_2/travel_guides/berlitz1/IntroMadeira.txt
../written_2/travel_guides/berlitz1/IntroMadrid.txt
../written_2/travel_guides/berlitz1/IntroMalaysia.txt
../written_2/travel_guides/berlitz1/IntroMallorca.txt
../written_2/travel_guides/berlitz1/JungleMalaysia.txt
../written_2/travel_guides/berlitz1/WhatToDublin.txt
../written_2/travel_guides/berlitz1/WhatToEdinburgh.txt
../written_2/travel_guides/berlitz1/WhatToEgypt.txt
../written_2/travel_guides/berlitz1/WhatToFWI.txt
../written_2/travel_guides/berlitz1/WhatToFrance.txt
../written_2/travel_guides/berlitz1/WhatToGreek.txt
../written_2/travel_guides/berlitz1/WhatToHawaii.txt
../written_2/travel_guides/berlitz1/WhatToHongKong.txt
../written_2/travel_guides/berlitz1/WhatToIbiza.txt
../written_2/travel_guides/berlitz1/WhatToIndia.txt
../written_2/travel_guides/berlitz1/WhatToIsrael.txt
../written_2/travel_guides/berlitz1/WhatToIstanbul.txt
../written_2/travel_guides/berlitz1/WhatToItaly.txt
../written_2/travel_guides/berlitz1/WhatToJamaica.txt
../written_2/travel_guides/berlitz1/WhatToJapan.txt
../written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt
../written_2/travel_guides/berlitz1/WhatToLasVegas.txt
../written_2/travel_guides/berlitz1/WhatToLosAngeles.txt
../written_2/travel_guides/berlitz1/WhatToMadeira.txt
../written_2/travel_guides/berlitz1/WhatToMalaysia.txt
../written_2/travel_guides/berlitz1/WhatToMallorca.txt
../written_2/travel_guides/berlitz1/WhereToDublin.txt
../written_2/travel_guides/berlitz1/WhereToEdinburgh.txt
../written_2/travel_guides/berlitz1/WhereToEgypt.txt
../written_2/travel_guides/berlitz1/WhereToFWI.txt
../written_2/travel_guides/berlitz1/WhereToFrance.txt
../written_2/travel_guides/berlitz1/WhereToGreek.txt
../written_2/travel_guides/berlitz1/WhereToHawaii.txt
../written_2/travel_guides/berlitz1/WhereToHongKong.txt
../written_2/travel_guides/berlitz1/WhereToIbiza.txt
../written_2/travel_guides/berlitz1/WhereToIndia.txt
../written_2/travel_guides/berlitz1/WhereToIsrael.txt
../written_2/travel_guides/berlitz1/WhereToIstanbul.txt
../written_2/travel_guides/berlitz1/WhereToItaly.txt
../written_2/travel_guides/berlitz1/WhereToJapan.txt
../written_2/travel_guides/berlitz1/WhereToJerusalem.txt
../written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt
../written_2/travel_guides/berlitz1/WhereToLosAngeles.txt
../written_2/travel_guides/berlitz1/WhereToMadeira.txt
../written_2/travel_guides/berlitz1/WhereToMadrid.txt
../written_2/travel_guides/berlitz1/WhereToMalaysia.txt
../written_2/travel_guides/berlitz1/WhereToMallorca.txt
../written_2/travel_guides/berlitz2/Algarve-History.txt
../written_2/travel_guides/berlitz2/Algarve-Intro.txt
../written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt
../written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt
../written_2/travel_guides/berlitz2/Amsterdam-History.txt
../written_2/travel_guides/berlitz2/Amsterdam-Intro.txt
../written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt
../written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt
../written_2/travel_guides/berlitz2/Athens-History.txt
../written_2/travel_guides/berlitz2/Athens-Intro.txt
../written_2/travel_guides/berlitz2/Athens-WhatToDo.txt
../written_2/travel_guides/berlitz2/Athens-WhereToGo.txt
../written_2/travel_guides/berlitz2/Bahamas-History.txt
../written_2/travel_guides/berlitz2/Bahamas-Intro.txt
../written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
../written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
../written_2/travel_guides/berlitz2/Bali-History.txt
../written_2/travel_guides/berlitz2/Bali-WhatToDo.txt
../written_2/travel_guides/berlitz2/Bali-WhereToGo.txt
../written_2/travel_guides/berlitz2/Barcelona-History.txt
../written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt
../written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt
../written_2/travel_guides/berlitz2/Beijing-History.txt
../written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt
../written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt
../written_2/travel_guides/berlitz2/Berlin-History.txt
../written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt
../written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt
../written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt
../written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt
../written_2/travel_guides/berlitz2/Bermuda-history.txt
../written_2/travel_guides/berlitz2/Boston-WhereToGo.txt
../written_2/travel_guides/berlitz2/Budapest-History.txt
../written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt
../written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt
../written_2/travel_guides/berlitz2/California-History.txt
../written_2/travel_guides/berlitz2/California-WhatToDo.txt
../written_2/travel_guides/berlitz2/California-WhereToGo.txt
../written_2/travel_guides/berlitz2/Canada-History.txt
../written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
../written_2/travel_guides/berlitz2/CanaryIslands-History.txt
../written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt
../written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
../written_2/travel_guides/berlitz2/Cancun-History.txt
../written_2/travel_guides/berlitz2/Cancun-WhatToDo.txt
../written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt
../written_2/travel_guides/berlitz2/China-History.txt
../written_2/travel_guides/berlitz2/China-WhatToDo.txt
../written_2/travel_guides/berlitz2/China-WhereToGo.txt
../written_2/travel_guides/berlitz2/Costa-History.txt
../written_2/travel_guides/berlitz2/Costa-WhatToDo.txt
../written_2/travel_guides/berlitz2/Costa-WhereToGo.txt
../written_2/travel_guides/berlitz2/CostaBlanca-History.txt
../written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt
../written_2/travel_guides/berlitz2/Crete-History.txt
../written_2/travel_guides/berlitz2/Crete-WhatToDo.txt
../written_2/travel_guides/berlitz2/Crete-WhereToGo.txt
../written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt
../written_2/travel_guides/berlitz2/Cuba-History.txt
../written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt
../written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt
../written_2/travel_guides/berlitz2/Nepal-History.txt
../written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt
../written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt
../written_2/travel_guides/berlitz2/NewOrleans-History.txt
../written_2/travel_guides/berlitz2/Paris-WhatToDo.txt
../written_2/travel_guides/berlitz2/Paris-WhereToGo.txt
../written_2/travel_guides/berlitz2/Poland-History.txt
../written_2/travel_guides/berlitz2/Poland-WhatToDo.txt
../written_2/travel_guides/berlitz2/Portugal-History.txt
../written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt
../written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
../written_2/travel_guides/berlitz2/PuertoRico-History.txt
../written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
../written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
../written_2/travel_guides/berlitz2/Vallarta-History.txt
../written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
../written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
``

## The -size expression

-size finds a file based on its size 

Syntax: find [path] -size [size]
The -size option specifies the size of file find should search for. 
* Example 1: The -size option can be useful to locate files that meet a specific size criteria. Maybe we're running low on storage and want to find files that are taking up the most space. In the example below we find files over 100 kilobytes. "k" represents kilobytes and the "+" indicates find should look for files above this threshold.
  
  Command: `find -size +100k`
  
  Output:
``
./non-fiction/OUP/Berk/CH4.txt
./non-fiction/OUP/Berk/ch2.txt
./travel_guides/berlitz1/WhereToFrance.txt
./travel_guides/berlitz1/WhereToIndia.txt
./travel_guides/berlitz1/WhereToItaly.txt
./travel_guides/berlitz1/WhereToJapan.txt
./travel_guides/berlitz1/WhereToMalaysia.txt
./travel_guides/berlitz2/Canada-WhereToGo.txt
./travel_guides/berlitz2/China-WhereToGo.txt
./travel_guides/berlitz2/Portugal-WhereToGo.txt
``


* Example 2:  Similiarly, we can use -size to find files below a certain threshold. Maybe we also want to check if our computer's low storage is because of several unnoticed tiny files taking up space. In the example below we find files that are under 2 kilobytes. "k" represents kilobytes and the "-" indicates find should look for files below this threshold.
  
  Command: `find -size -2k`
 
  Output:
``
./travel_guides/berlitz1/HandRIbiza.txt
./travel_guides/berlitz1/HandRIstanbul.txt
``


## The -and expression
-and combines two expressions used with find, where the criteria of both expressions have to be met
The -and option allows us to use a combination of some of the commands we've learned, where find will search for files based on two or more criteria. 
Syntax: find [path] \( [expression1] -and [expression2] \)

* Example 1: The -and option is very useful when we want to meet multiple conditions simultaneously and make it easier to locate specific files that meet that specific criteria. For example, if we wanted to look for large files to delete to free up storage, but are only willing to delete txt files, we could accomplish this with the -and option. Below, find searched for .txt files using -name, and files above 100k with -size, joined together by -and. 
  
  Command: `find \( -name W*.txt -and -size +100k  \)`
  
  Output:
``
./travel_guides/berlitz1/WhereToFrance.txt
./travel_guides/berlitz1/WhereToIndia.txt
./travel_guides/berlitz1/WhereToItaly.txt
./travel_guides/berlitz1/WhereToJapan.txt
./travel_guides/berlitz1/WhereToMalaysia.txt``

* Example 2: The -and option helps us avoid sifting through a large number of search results that don't meet all of the criteria. In the example below, we have find search for directories that are above 100k. We could use this if we wanted to check if any directories are taking up that amount of space, without having to scroll through all the search results generated by simply using the command -size +100k. Below, find searched for directory files using -type, and files above 100k with -size, joined together by -and. 
  
  Command: `find \( -type d  -and -size +100k  \)`
  
  Output:
``
``
(No Output)

*All commands were found using chatGBT [click here for a link to the copy of the chat](https://docs.google.com/document/d/1hYW7CyUJ-t4eKVQHVktVMLhEMzHA57P4zT7Q97ptr8o/edit?usp=sharing)
