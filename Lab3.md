# The -find Command
#### Below we will explore four different ways we can use the "-find" terminal command which uses the syntax:
`find [path] [expression]`

#### In all examples we will be working within the skill-demo1-data directory of written_2 within the ssh server 

*All commands were found using chatGBT [click here for a link to the copy of the chat](https://docs.google.com/document/d/1hYW7CyUJ-t4eKVQHVktVMLhEMzHA57P4zT7Q97ptr8o/edit?usp=sharing)

## The -type expression 
-type finds files of a certain type

Syntax: find [path] -type [type]

* Example 1: Finding directories only

  Command: `find -type d`

  Output:
``
.
./.git
./.git/info
./.git/hooks
./.git/branches
./.git/refs
./.git/refs/heads
./.git/refs/tags
./.git/refs/remotes
./.git/refs/remotes/origin
./.git/objects
./.git/objects/pack
./.git/objects/info
./.git/logs
./.git/logs/refs
./.git/logs/refs/remotes
./.git/logs/refs/remotes/origin
./.git/logs/refs/heads
./written_2
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Abernathy
./written_2/non-fiction/OUP/Berk
./written_2/non-fiction/OUP/Castro
./written_2/non-fiction/OUP/Fletcher
./written_2/non-fiction/OUP/Kauffman
./written_2/non-fiction/OUP/Rybczynski
./written_2/travel_guides
./written_2/travel_guides/berlitz1
./written_2/travel_guides/berlitz2[cs15lwi23ajw@ieng6-201]:skill-demo1-data:140$ find -type d             
.
./.git
./.git/info
./.git/hooks
./.git/branches
./.git/refs
./.git/refs/heads
./.git/refs/tags
./.git/refs/remotes
./.git/refs/remotes/origin
./.git/objects
./.git/objects/pack
./.git/objects/info
./.git/logs
./.git/logs/refs
./.git/logs/refs/remotes
./.git/logs/refs/remotes/origin
./.git/logs/refs/heads
./written_2
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Abernathy
./written_2/non-fiction/OUP/Berk
./written_2/non-fiction/OUP/Castro
./written_2/non-fiction/OUP/Fletcher
./written_2/non-fiction/OUP/Kauffman
./written_2/non-fiction/OUP/Rybczynski
./written_2/travel_guides
./written_2/travel_guides/berlitz1
./written_2/travel_guides/berlitz2 ``

* Example 2: Finding files only
  
  Command: `find -type f`
  
  Output:
``
./.git/info/exclude
./.git/hooks/commit-msg.sample
./.git/hooks/prepare-commit-msg.sample
./.git/hooks/update.sample
./.git/hooks/pre-rebase.sample
./.git/hooks/pre-merge-commit.sample
./.git/hooks/push-to-checkout.sample
./.git/hooks/pre-push.sample
./.git/hooks/pre-commit.sample
./.git/hooks/post-update.sample
./.git/hooks/pre-receive.sample
./.git/hooks/applypatch-msg.sample
./.git/hooks/fsmonitor-watchman.sample
./.git/hooks/pre-applypatch.sample
./.git/description
./.git/refs/heads/main
./.git/refs/remotes/origin/HEAD
./.git/objects/pack/pack-b98cb6a4ca64cc7b2944f0fa07d3e03927d66064.pack
./.git/objects/pack/pack-b98cb6a4ca64cc7b2944f0fa07d3e03927d66064.idx
./.git/HEAD
./.git/config
./.git/logs/refs/remotes/origin/HEAD
./.git/logs/refs/heads/main
./.git/logs/HEAD
./.git/packed-refs
./.git/index
./written_2/non-fiction/OUP/Abernathy/ch1.txt
./written_2/non-fiction/OUP/Abernathy/ch14.txt
./written_2/non-fiction/OUP/Abernathy/ch15.txt
./written_2/non-fiction/OUP/Abernathy/ch2.txt
./written_2/non-fiction/OUP/Abernathy/ch3.txt
./written_2/non-fiction/OUP/Abernathy/ch6.txt
./written_2/non-fiction/OUP/Abernathy/ch7.txt
./written_2/non-fiction/OUP/Abernathy/ch8.txt
./written_2/non-fiction/OUP/Abernathy/ch9.txt
./written_2/non-fiction/OUP/Berk/CH4.txt
./written_2/non-fiction/OUP/Berk/ch1.txt
./written_2/non-fiction/OUP/Berk/ch2.txt
./written_2/non-fiction/OUP/Berk/ch7.txt
./written_2/non-fiction/OUP/Castro/chA.txt
./written_2/non-fiction/OUP/Castro/chB.txt
./written_2/non-fiction/OUP/Castro/chC.txt
./written_2/non-fiction/OUP/Castro/chL.txt
./written_2/non-fiction/OUP/Castro/chM.txt
./written_2/non-fiction/OUP/Castro/chN.txt
./written_2/non-fiction/OUP/Castro/chO.txt
./written_2/non-fiction/OUP/Castro/chP.txt
./written_2/non-fiction/OUP/Castro/chQ.txt
./written_2/non-fiction/OUP/Castro/chR.txt
./written_2/non-fiction/OUP/Castro/chV.txt
./written_2/non-fiction/OUP/Castro/chW.txt
./written_2/non-fiction/OUP/Castro/chY.txt
./written_2/non-fiction/OUP/Castro/chZ.txt
./written_2/non-fiction/OUP/Fletcher/ch1.txt
./written_2/non-fiction/OUP/Fletcher/ch10.txt
./written_2/non-fiction/OUP/Fletcher/ch2.txt
./written_2/non-fiction/OUP/Fletcher/ch5.txt
./written_2/non-fiction/OUP/Fletcher/ch6.txt
./written_2/non-fiction/OUP/Fletcher/ch9.txt
./written_2/non-fiction/OUP/Kauffman/ch1.txt
./written_2/non-fiction/OUP/Kauffman/ch10.txt
./written_2/non-fiction/OUP/Kauffman/ch3.txt
./written_2/non-fiction/OUP/Kauffman/ch4.txt
./written_2/non-fiction/OUP/Kauffman/ch5.txt
./written_2/non-fiction/OUP/Kauffman/ch6.txt
./written_2/non-fiction/OUP/Kauffman/ch7.txt
./written_2/non-fiction/OUP/Kauffman/ch8.txt
./written_2/non-fiction/OUP/Kauffman/ch9.txt
./written_2/non-fiction/OUP/Rybczynski/ch1.txt
./written_2/non-fiction/OUP/Rybczynski/ch2.txt
./written_2/non-fiction/OUP/Rybczynski/ch3.txt
./written_2/travel_guides/berlitz1/HandRHawaii.txt
./written_2/travel_guides/berlitz1/HandRHongKong.txt
./written_2/travel_guides/berlitz1/HandRIbiza.txt
./written_2/travel_guides/berlitz1/HandRIsrael.txt
./written_2/travel_guides/berlitz1/HandRIstanbul.txt
./written_2/travel_guides/berlitz1/HandRJamaica.txt
./written_2/travel_guides/berlitz1/HandRJerusalem.txt
./written_2/travel_guides/berlitz1/HandRLakeDistrict.txt
./written_2/travel_guides/berlitz1/HandRLasVegas.txt
./written_2/travel_guides/berlitz1/HandRLisbon.txt
./written_2/travel_guides/berlitz1/HandRLosAngeles.txt
./written_2/travel_guides/berlitz1/HandRMadeira.txt
./written_2/travel_guides/berlitz1/HandRMadrid.txt
./written_2/travel_guides/berlitz1/HandRMallorca.txt
./written_2/travel_guides/berlitz1/HistoryDublin.txt
./written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
./written_2/travel_guides/berlitz1/HistoryEgypt.txt
./written_2/travel_guides/berlitz1/HistoryFWI.txt
./written_2/travel_guides/berlitz1/HistoryFrance.txt
./written_2/travel_guides/berlitz1/HistoryGreek.txt
./written_2/travel_guides/berlitz1/HistoryHawaii.txt
./written_2/travel_guides/berlitz1/HistoryHongKong.txt
./written_2/travel_guides/berlitz1/HistoryIbiza.txt
./written_2/travel_guides/berlitz1/HistoryIndia.txt
./written_2/travel_guides/berlitz1/HistoryIsrael.txt
./written_2/travel_guides/berlitz1/HistoryIstanbul.txt
./written_2/travel_guides/berlitz1/HistoryItaly.txt
./written_2/travel_guides/berlitz1/HistoryJamaica.txt
./written_2/travel_guides/berlitz1/HistoryJapan.txt
./written_2/travel_guides/berlitz1/HistoryJerusalem.txt
./written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt
./written_2/travel_guides/berlitz1/HistoryLasVegas.txt
./written_2/travel_guides/berlitz1/HistoryMadeira.txt
./written_2/travel_guides/berlitz1/HistoryMadrid.txt
./written_2/travel_guides/berlitz1/HistoryMalaysia.txt
./written_2/travel_guides/berlitz1/HistoryMallorca.txt
./written_2/travel_guides/berlitz1/IntroDublin.txt
./written_2/travel_guides/berlitz1/IntroEdinburgh.txt
./written_2/travel_guides/berlitz1/IntroEgypt.txt
./written_2/travel_guides/berlitz1/IntroFWI.txt
./written_2/travel_guides/berlitz1/IntroFrance.txt
./written_2/travel_guides/berlitz1/IntroGreek.txt
./written_2/travel_guides/berlitz1/IntroHongKong.txt
./written_2/travel_guides/berlitz1/IntroIbiza.txt
./written_2/travel_guides/berlitz1/IntroIndia.txt
./written_2/travel_guides/berlitz1/IntroIsrael.txt
./written_2/travel_guides/berlitz1/IntroIstanbul.txt
./written_2/travel_guides/berlitz1/IntroItaly.txt
./written_2/travel_guides/berlitz1/IntroJamaica.txt
./written_2/travel_guides/berlitz1/IntroJapan.txt
./written_2/travel_guides/berlitz1/IntroJerusalem.txt
./written_2/travel_guides/berlitz1/IntroLakeDistrict.txt
./written_2/travel_guides/berlitz1/IntroLasVegas.txt
./written_2/travel_guides/berlitz1/IntroLosAngeles.txt
./written_2/travel_guides/berlitz1/IntroMadeira.txt
./written_2/travel_guides/berlitz1/IntroMadrid.txt
./written_2/travel_guides/berlitz1/IntroMalaysia.txt
./written_2/travel_guides/berlitz1/IntroMallorca.txt
./written_2/travel_guides/berlitz1/JungleMalaysia.txt
./written_2/travel_guides/berlitz1/WhatToDublin.txt
./written_2/travel_guides/berlitz1/WhatToEdinburgh.txt
./written_2/travel_guides/berlitz1/WhatToEgypt.txt
./written_2/travel_guides/berlitz1/WhatToFWI.txt
./written_2/travel_guides/berlitz1/WhatToFrance.txt
./written_2/travel_guides/berlitz1/WhatToGreek.txt
./written_2/travel_guides/berlitz1/WhatToHawaii.txt
./written_2/travel_guides/berlitz1/WhatToHongKong.txt
./written_2/travel_guides/berlitz1/WhatToIbiza.txt
./written_2/travel_guides/berlitz1/WhatToIndia.txt
./written_2/travel_guides/berlitz1/WhatToIsrael.txt
./written_2/travel_guides/berlitz1/WhatToIstanbul.txt
./written_2/travel_guides/berlitz1/WhatToItaly.txt
./written_2/travel_guides/berlitz1/WhatToJamaica.txt
./written_2/travel_guides/berlitz1/WhatToJapan.txt
./written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt
./written_2/travel_guides/berlitz1/WhatToLasVegas.txt
./written_2/travel_guides/berlitz1/WhatToLosAngeles.txt
./written_2/travel_guides/berlitz1/WhatToMadeira.txt
./written_2/travel_guides/berlitz1/WhatToMalaysia.txt
./written_2/travel_guides/berlitz1/WhatToMallorca.txt
./written_2/travel_guides/berlitz1/WhereToDublin.txt
./written_2/travel_guides/berlitz1/WhereToEdinburgh.txt
./written_2/travel_guides/berlitz1/WhereToEgypt.txt
./written_2/travel_guides/berlitz1/WhereToFWI.txt
./written_2/travel_guides/berlitz1/WhereToFrance.txt
./written_2/travel_guides/berlitz1/WhereToGreek.txt
./written_2/travel_guides/berlitz1/WhereToHawaii.txt
./written_2/travel_guides/berlitz1/WhereToHongKong.txt
./written_2/travel_guides/berlitz1/WhereToIbiza.txt
./written_2/travel_guides/berlitz1/WhereToIndia.txt
./written_2/travel_guides/berlitz1/WhereToIsrael.txt
./written_2/travel_guides/berlitz1/WhereToIstanbul.txt
./written_2/travel_guides/berlitz1/WhereToItaly.txt
./written_2/travel_guides/berlitz1/WhereToJapan.txt
./written_2/travel_guides/berlitz1/WhereToJerusalem.txt
./written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt
./written_2/travel_guides/berlitz1/WhereToLosAngeles.txt
./written_2/travel_guides/berlitz1/WhereToMadeira.txt
./written_2/travel_guides/berlitz1/WhereToMadrid.txt
./written_2/travel_guides/berlitz1/WhereToMalaysia.txt
./written_2/travel_guides/berlitz1/WhereToMallorca.txt
./written_2/travel_guides/berlitz2/Algarve-History.txt
./written_2/travel_guides/berlitz2/Algarve-Intro.txt
./written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt
./written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt
./written_2/travel_guides/berlitz2/Amsterdam-History.txt
./written_2/travel_guides/berlitz2/Amsterdam-Intro.txt
./written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt
./written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt
./written_2/travel_guides/berlitz2/Athens-History.txt
./written_2/travel_guides/berlitz2/Athens-Intro.txt
./written_2/travel_guides/berlitz2/Athens-WhatToDo.txt
./written_2/travel_guides/berlitz2/Athens-WhereToGo.txt
./written_2/travel_guides/berlitz2/Bahamas-History.txt
./written_2/travel_guides/berlitz2/Bahamas-Intro.txt
./written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
./written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
./written_2/travel_guides/berlitz2/Bali-History.txt
./written_2/travel_guides/berlitz2/Bali-WhatToDo.txt
./written_2/travel_guides/berlitz2/Bali-WhereToGo.txt
./written_2/travel_guides/berlitz2/Barcelona-History.txt
./written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt
./written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt
./written_2/travel_guides/berlitz2/Beijing-History.txt
./written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt
./written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt
./written_2/travel_guides/berlitz2/Berlin-History.txt
./written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt
./written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt
./written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt
./written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt
./written_2/travel_guides/berlitz2/Bermuda-history.txt
./written_2/travel_guides/berlitz2/Boston-WhereToGo.txt
./written_2/travel_guides/berlitz2/Budapest-History.txt
./written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt
./written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt
./written_2/travel_guides/berlitz2/California-History.txt
./written_2/travel_guides/berlitz2/California-WhatToDo.txt
./written_2/travel_guides/berlitz2/California-WhereToGo.txt
./written_2/travel_guides/berlitz2/Canada-History.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
./written_2/travel_guides/berlitz2/CanaryIslands-History.txt
./written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt
./written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
./written_2/travel_guides/berlitz2/Cancun-History.txt
./written_2/travel_guides/berlitz2/Cancun-WhatToDo.txt
./written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt
./written_2/travel_guides/berlitz2/China-History.txt
./written_2/travel_guides/berlitz2/China-WhatToDo.txt
./written_2/travel_guides/berlitz2/China-WhereToGo.txt
./written_2/travel_guides/berlitz2/Costa-History.txt
./written_2/travel_guides/berlitz2/Costa-WhatToDo.txt
./written_2/travel_guides/berlitz2/Costa-WhereToGo.txt
./written_2/travel_guides/berlitz2/CostaBlanca-History.txt
./written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt
./written_2/travel_guides/berlitz2/Crete-History.txt
./written_2/travel_guides/berlitz2/Crete-WhatToDo.txt
./written_2/travel_guides/berlitz2/Crete-WhereToGo.txt
./written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt
./written_2/travel_guides/berlitz2/Cuba-History.txt
./written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt
./written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt
./written_2/travel_guides/berlitz2/Nepal-History.txt
./written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt
./written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt
./written_2/travel_guides/berlitz2/NewOrleans-History.txt
./written_2/travel_guides/berlitz2/Paris-WhatToDo.txt
./written_2/travel_guides/berlitz2/Paris-WhereToGo.txt
./written_2/travel_guides/berlitz2/Poland-History.txt
./written_2/travel_guides/berlitz2/Poland-WhatToDo.txt
./written_2/travel_guides/berlitz2/Portugal-History.txt
./written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt
./written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
./written_2/travel_guides/berlitz2/PuertoRico-History.txt
./written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
./written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
./written_2/travel_guides/berlitz2/Vallarta-History.txt
./written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
./written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
``

## The -size expression

-size finds a file based on its size 

Syntax: find [path] -size [size]

* Example 1: Finding files over 100 kilobytes 
  
  Command: `find -size +100k`
  
  Output:
``
./.git/objects/pack/pack-b98cb6a4ca64cc7b2944f0fa07d3e03927d66064.pack
./written_2/non-fiction/OUP/Berk/CH4.txt
./written_2/non-fiction/OUP/Berk/ch2.txt
./written_2/travel_guides/berlitz1/WhereToFrance.txt
./written_2/travel_guides/berlitz1/WhereToIndia.txt
./written_2/travel_guides/berlitz1/WhereToItaly.txt
./written_2/travel_guides/berlitz1/WhereToJapan.txt
./written_2/travel_guides/berlitz1/WhereToMalaysia.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
./written_2/travel_guides/berlitz2/China-WhereToGo.txt
./written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
``
* Example 2: Finding files under 2 kilobytes
  
  Command: `find -size -2k`
 
  Output:
``
./.git/info/exclude
./.git/hooks/commit-msg.sample
./.git/hooks/pre-merge-commit.sample
./.git/hooks/post-update.sample
./.git/hooks/pre-receive.sample
./.git/hooks/applypatch-msg.sample
./.git/hooks/pre-applypatch.sample
./.git/description
./.git/refs/heads/main
./.git/refs/remotes/origin/HEAD
./.git/HEAD
./.git/config
./.git/logs/refs/remotes/origin/HEAD
./.git/logs/refs/heads/main
./.git/logs/HEAD
./.git/packed-refs
./written_2/travel_guides/berlitz1/HandRIbiza.txt
./written_2/travel_guides/berlitz1/HandRIstanbul.txt
``

## The -name expression
-name finds files based on their names.

Syntax: find [path] -name [pattern]

* Example 1: Finding txt files with the name "IntroEgypt"
  
  Command: `find -name IntroEgypt.txt`
  
  Output: 
``
./written_2/travel_guides/berlitz1/IntroEgypt.txt``

* Example 2: Finding txt files that start with capital H
 
  Command: `find -name H*.txt`
  
  Output:
``
./written_2/travel_guides/berlitz1/HandRHawaii.txt
./written_2/travel_guides/berlitz1/HandRHongKong.txt
./written_2/travel_guides/berlitz1/HandRIbiza.txt
./written_2/travel_guides/berlitz1/HandRIsrael.txt
./written_2/travel_guides/berlitz1/HandRIstanbul.txt
./written_2/travel_guides/berlitz1/HandRJamaica.txt
./written_2/travel_guides/berlitz1/HandRJerusalem.txt
./written_2/travel_guides/berlitz1/HandRLakeDistrict.txt
./written_2/travel_guides/berlitz1/HandRLasVegas.txt
./written_2/travel_guides/berlitz1/HandRLisbon.txt
./written_2/travel_guides/berlitz1/HandRLosAngeles.txt
./written_2/travel_guides/berlitz1/HandRMadeira.txt
./written_2/travel_guides/berlitz1/HandRMadrid.txt
./written_2/travel_guides/berlitz1/HandRMallorca.txt
./written_2/travel_guides/berlitz1/HistoryDublin.txt
./written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
./written_2/travel_guides/berlitz1/HistoryEgypt.txt
./written_2/travel_guides/berlitz1/HistoryFWI.txt
./written_2/travel_guides/berlitz1/HistoryFrance.txt
./written_2/travel_guides/berlitz1/HistoryGreek.txt
./written_2/travel_guides/berlitz1/HistoryHawaii.txt
./written_2/travel_guides/berlitz1/HistoryHongKong.txt
./written_2/travel_guides/berlitz1/HistoryIbiza.txt
./written_2/travel_guides/berlitz1/HistoryIndia.txt
./written_2/travel_guides/berlitz1/HistoryIsrael.txt
./written_2/travel_guides/berlitz1/HistoryIstanbul.txt
./written_2/travel_guides/berlitz1/HistoryItaly.txt
./written_2/travel_guides/berlitz1/HistoryJamaica.txt
./written_2/travel_guides/berlitz1/HistoryJapan.txt
./written_2/travel_guides/berlitz1/HistoryJerusalem.txt
./written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt
./written_2/travel_guides/berlitz1/HistoryLasVegas.txt
./written_2/travel_guides/berlitz1/HistoryMadeira.txt
./written_2/travel_guides/berlitz1/HistoryMadrid.txt
./written_2/travel_guides/berlitz1/HistoryMalaysia.txt
./written_2/travel_guides/berlitz1/HistoryMallorca.txt``

## The -and expression
-and combines two expressions used with find, where the criteria of both expressions have to be met

Syntax: find [path] \( [expression1] -and [expression2] \)
* Example 1: Finding only files and ones that are less than 2 kilobytes 
  
  Command: `find \( -size -2k  -and -type f \)`
  
  Output:
``
./.git/info/exclude
./.git/hooks/commit-msg.sample
./.git/hooks/pre-merge-commit.sample
./.git/hooks/post-update.sample
./.git/hooks/pre-receive.sample
./.git/hooks/applypatch-msg.sample
./.git/hooks/pre-applypatch.sample
./.git/description
./.git/refs/heads/main
./.git/refs/remotes/origin/HEAD
./.git/HEAD
./.git/config
./.git/logs/refs/remotes/origin/HEAD
./.git/logs/refs/heads/main
./.git/logs/HEAD
./.git/packed-refs
./written_2/travel_guides/berlitz1/HandRIbiza.txt
./written_2/travel_guides/berlitz1/HandRIstanbul.txt``
* Example 2: Finding txt files that start with W and are more than 100 kilobytes
  
  Command: `find \( -name W*.txt -and -size +100k  \)`
  
  Output:
``
./written_2/travel_guides/berlitz1/WhereToFrance.txt
./written_2/travel_guides/berlitz1/WhereToIndia.txt
./written_2/travel_guides/berlitz1/WhereToItaly.txt
./written_2/travel_guides/berlitz1/WhereToJapan.txt
./written_2/travel_guides/berlitz1/WhereToMalaysia.txt``

*All commands were found using chatGBT [click here for a link to the copy of the chat](https://docs.google.com/document/d/1hYW7CyUJ-t4eKVQHVktVMLhEMzHA57P4zT7Q97ptr8o/edit?usp=sharing)
