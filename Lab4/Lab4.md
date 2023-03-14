# 'exec' within the -find Command

### The exec option is a powerful addition to using the -find command. It is used to perform an action on the files that are found by the find command, allowing you to execute a command on each file found. 

## Syntax
The basic syntax for exec is as follows:
``find [path] [expression] -exec [command] {} \; ``
The [path] specifies the directory or path in which to search for files, while [expression] specifies the search criteria. [command] is the command to be executed on each file found and {} is a placeholder that represents the file name.

### Below are some examples of using the exec option
#### In all examples we will be working within the ../skill-demo1-data/written_2 directory within the ssh server 

## Example 1
Let's say we want to plan a trip, want to utilize out travel_guides directory in written_2. We're still deciding on a location, but want to know the word count of each file to take into account how long its going to take to read. 
THe command below will print the number of words in each file. {} is a placeholder for the file name that find finds, and \; indicates the end of the command to be executed by -exec. The {} placeholder is replaced by the file name for each file that find finds, and the -exec option executes the wc -w command for each file. 

Command:
``
find . -name '*.txt' -type f -exec wc -w {} \;
``

Output:
6973 ./non-fiction/OUP/Abernathy/ch1.txt
5918 ./non-fiction/OUP/Abernathy/ch14.txt
6544 ./non-fiction/OUP/Abernathy/ch15.txt
6707 ./non-fiction/OUP/Abernathy/ch2.txt
5273 ./non-fiction/OUP/Abernathy/ch3.txt
6680 ./non-fiction/OUP/Abernathy/ch6.txt
6718 ./non-fiction/OUP/Abernathy/ch7.txt
8618 ./non-fiction/OUP/Abernathy/ch8.txt
5331 ./non-fiction/OUP/Abernathy/ch9.txt
15671 ./non-fiction/OUP/Berk/CH4.txt
13720 ./non-fiction/OUP/Berk/ch1.txt
15516 ./non-fiction/OUP/Berk/ch2.txt
10158 ./non-fiction/OUP/Berk/ch7.txt
5852 ./non-fiction/OUP/Castro/chA.txt
5432 ./non-fiction/OUP/Castro/chB.txt
3857 ./non-fiction/OUP/Castro/chC.txt
4068 ./non-fiction/OUP/Castro/chL.txt
9207 ./non-fiction/OUP/Castro/chM.txt
1513 ./non-fiction/OUP/Castro/chN.txt
1451 ./non-fiction/OUP/Castro/chO.txt
6687 ./non-fiction/OUP/Castro/chP.txt
1368 ./non-fiction/OUP/Castro/chQ.txt
5310 ./non-fiction/OUP/Castro/chR.txt
3399 ./non-fiction/OUP/Castro/chV.txt
1125 ./non-fiction/OUP/Castro/chW.txt
911 ./non-fiction/OUP/Castro/chY.txt
900 ./non-fiction/OUP/Castro/chZ.txt
7608 ./non-fiction/OUP/Fletcher/ch1.txt
5240 ./non-fiction/OUP/Fletcher/ch10.txt
8418 ./non-fiction/OUP/Fletcher/ch2.txt
7899 ./non-fiction/OUP/Fletcher/ch5.txt
10801 ./non-fiction/OUP/Fletcher/ch6.txt
8600 ./non-fiction/OUP/Fletcher/ch9.txt
10497 ./non-fiction/OUP/Kauffman/ch1.txt
10295 ./non-fiction/OUP/Kauffman/ch10.txt
13258 ./non-fiction/OUP/Kauffman/ch3.txt
12075 ./non-fiction/OUP/Kauffman/ch4.txt
4405 ./non-fiction/OUP/Kauffman/ch5.txt
9922 ./non-fiction/OUP/Kauffman/ch6.txt
8039 ./non-fiction/OUP/Kauffman/ch7.txt
16799 ./non-fiction/OUP/Kauffman/ch8.txt
14023 ./non-fiction/OUP/Kauffman/ch9.txt
5356 ./non-fiction/OUP/Rybczynski/ch1.txt
5887 ./non-fiction/OUP/Rybczynski/ch2.txt
8062 ./non-fiction/OUP/Rybczynski/ch3.txt
2163 ./travel_guides/berlitz1/HandRHawaii.txt
152 ./travel_guides/berlitz1/HandRHongKong.txt
86 ./travel_guides/berlitz1/HandRIbiza.txt
3532 ./travel_guides/berlitz1/HandRIsrael.txt
121 ./travel_guides/berlitz1/HandRIstanbul.txt
3124 ./travel_guides/berlitz1/HandRJamaica.txt
179 ./travel_guides/berlitz1/HandRJerusalem.txt
202 ./travel_guides/berlitz1/HandRLakeDistrict.txt
201 ./travel_guides/berlitz1/HandRLasVegas.txt
129 ./travel_guides/berlitz1/HandRLisbon.txt
159 ./travel_guides/berlitz1/HandRLosAngeles.txt
188 ./travel_guides/berlitz1/HandRMadeira.txt
2014 ./travel_guides/berlitz1/HandRMadrid.txt
191 ./travel_guides/berlitz1/HandRMallorca.txt
2294 ./travel_guides/berlitz1/HistoryDublin.txt
3029 ./travel_guides/berlitz1/HistoryEdinburgh.txt
2646 ./travel_guides/berlitz1/HistoryEgypt.txt
2049 ./travel_guides/berlitz1/HistoryFWI.txt
5270 ./travel_guides/berlitz1/HistoryFrance.txt
2712 ./travel_guides/berlitz1/HistoryGreek.txt
2400 ./travel_guides/berlitz1/HistoryHawaii.txt
2102 ./travel_guides/berlitz1/HistoryHongKong.txt
1759 ./travel_guides/berlitz1/HistoryIbiza.txt
7762 ./travel_guides/berlitz1/HistoryIndia.txt
2390 ./travel_guides/berlitz1/HistoryIsrael.txt
3887 ./travel_guides/berlitz1/HistoryIstanbul.txt
6396 ./travel_guides/berlitz1/HistoryItaly.txt
2476 ./travel_guides/berlitz1/HistoryJamaica.txt
5651 ./travel_guides/berlitz1/HistoryJapan.txt
2661 ./travel_guides/berlitz1/HistoryJerusalem.txt
1959 ./travel_guides/berlitz1/HistoryLakeDistrict.txt
2711 ./travel_guides/berlitz1/HistoryLasVegas.txt
1672 ./travel_guides/berlitz1/HistoryMadeira.txt
1748 ./travel_guides/berlitz1/HistoryMadrid.txt
4921 ./travel_guides/berlitz1/HistoryMalaysia.txt
1937 ./travel_guides/berlitz1/HistoryMallorca.txt
1128 ./travel_guides/berlitz1/IntroDublin.txt
1362 ./travel_guides/berlitz1/IntroEdinburgh.txt
1113 ./travel_guides/berlitz1/IntroEgypt.txt
1070 ./travel_guides/berlitz1/IntroFWI.txt
1555 ./travel_guides/berlitz1/IntroFrance.txt
1203 ./travel_guides/berlitz1/IntroGreek.txt
824 ./travel_guides/berlitz1/IntroHongKong.txt
897 ./travel_guides/berlitz1/IntroIbiza.txt
3755 ./travel_guides/berlitz1/IntroIndia.txt
731 ./travel_guides/berlitz1/IntroIsrael.txt
1029 ./travel_guides/berlitz1/IntroIstanbul.txt
1684 ./travel_guides/berlitz1/IntroItaly.txt
1511 ./travel_guides/berlitz1/IntroJamaica.txt
2575 ./travel_guides/berlitz1/IntroJapan.txt
1427 ./travel_guides/berlitz1/IntroJerusalem.txt
1712 ./travel_guides/berlitz1/IntroLakeDistrict.txt
1659 ./travel_guides/berlitz1/IntroLasVegas.txt
896 ./travel_guides/berlitz1/IntroLosAngeles.txt
1420 ./travel_guides/berlitz1/IntroMadeira.txt
1611 ./travel_guides/berlitz1/IntroMadrid.txt
1180 ./travel_guides/berlitz1/IntroMalaysia.txt
1268 ./travel_guides/berlitz1/IntroMallorca.txt
990 ./travel_guides/berlitz1/JungleMalaysia.txt
2968 ./travel_guides/berlitz1/WhatToDublin.txt
3012 ./travel_guides/berlitz1/WhatToEdinburgh.txt
3142 ./travel_guides/berlitz1/WhatToEgypt.txt
3679 ./travel_guides/berlitz1/WhatToFWI.txt
248 ./travel_guides/berlitz1/WhatToFrance.txt
2733 ./travel_guides/berlitz1/WhatToGreek.txt
351 ./travel_guides/berlitz1/WhatToHawaii.txt
3602 ./travel_guides/berlitz1/WhatToHongKong.txt
5414 ./travel_guides/berlitz1/WhatToIbiza.txt
2759 ./travel_guides/berlitz1/WhatToIndia.txt
3066 ./travel_guides/berlitz1/WhatToIsrael.txt
3921 ./travel_guides/berlitz1/WhatToIstanbul.txt
3046 ./travel_guides/berlitz1/WhatToItaly.txt
13090 ./travel_guides/berlitz1/WhatToJamaica.txt
4973 ./travel_guides/berlitz1/WhatToJapan.txt
3045 ./travel_guides/berlitz1/WhatToLakeDistrict.txt
6872 ./travel_guides/berlitz1/WhatToLasVegas.txt
3383 ./travel_guides/berlitz1/WhatToLosAngeles.txt
4038 ./travel_guides/berlitz1/WhatToMadeira.txt
3325 ./travel_guides/berlitz1/WhatToMalaysia.txt
2550 ./travel_guides/berlitz1/WhatToMallorca.txt
12424 ./travel_guides/berlitz1/WhereToDublin.txt
11660 ./travel_guides/berlitz1/WhereToEdinburgh.txt
12823 ./travel_guides/berlitz1/WhereToEgypt.txt
9122 ./travel_guides/berlitz1/WhereToFWI.txt
35591 ./travel_guides/berlitz1/WhereToFrance.txt
11963 ./travel_guides/berlitz1/WhereToGreek.txt
309 ./travel_guides/berlitz1/WhereToHawaii.txt
9808 ./travel_guides/berlitz1/WhereToHongKong.txt
6153 ./travel_guides/berlitz1/WhereToIbiza.txt
25321 ./travel_guides/berlitz1/WhereToIndia.txt
12556 ./travel_guides/berlitz1/WhereToIsrael.txt
13060 ./travel_guides/berlitz1/WhereToIstanbul.txt
41331 ./travel_guides/berlitz1/WhereToItaly.txt
26776 ./travel_guides/berlitz1/WhereToJapan.txt
11402 ./travel_guides/berlitz1/WhereToJerusalem.txt
12714 ./travel_guides/berlitz1/WhereToLakeDistrict.txt
11010 ./travel_guides/berlitz1/WhereToLosAngeles.txt
9688 ./travel_guides/berlitz1/WhereToMadeira.txt
11088 ./travel_guides/berlitz1/WhereToMadrid.txt
26296 ./travel_guides/berlitz1/WhereToMalaysia.txt
10927 ./travel_guides/berlitz1/WhereToMallorca.txt
2476 ./travel_guides/berlitz2/Algarve-History.txt
1240 ./travel_guides/berlitz2/Algarve-Intro.txt
2667 ./travel_guides/berlitz2/Algarve-WhatToDo.txt
11555 ./travel_guides/berlitz2/Algarve-WhereToGo.txt
2615 ./travel_guides/berlitz2/Amsterdam-History.txt
1470 ./travel_guides/berlitz2/Amsterdam-Intro.txt
2667 ./travel_guides/berlitz2/Amsterdam-WhatToDo.txt
9940 ./travel_guides/berlitz2/Amsterdam-WhereToGo.txt
3221 ./travel_guides/berlitz2/Athens-History.txt
1453 ./travel_guides/berlitz2/Athens-Intro.txt
2788 ./travel_guides/berlitz2/Athens-WhatToDo.txt
11781 ./travel_guides/berlitz2/Athens-WhereToGo.txt
2658 ./travel_guides/berlitz2/Bahamas-History.txt
1492 ./travel_guides/berlitz2/Bahamas-Intro.txt
3275 ./travel_guides/berlitz2/Bahamas-WhatToDo.txt
12406 ./travel_guides/berlitz2/Bahamas-WhereToGo.txt
2628 ./travel_guides/berlitz2/Bali-History.txt
2997 ./travel_guides/berlitz2/Bali-WhatToDo.txt
13174 ./travel_guides/berlitz2/Bali-WhereToGo.txt
2011 ./travel_guides/berlitz2/Barcelona-History.txt
3070 ./travel_guides/berlitz2/Barcelona-WhatToDo.txt
11857 ./travel_guides/berlitz2/Barcelona-WhereToGo.txt
2037 ./travel_guides/berlitz2/Beijing-History.txt
3454 ./travel_guides/berlitz2/Beijing-WhatToDo.txt
10418 ./travel_guides/berlitz2/Beijing-WhereToGo.txt
3466 ./travel_guides/berlitz2/Berlin-History.txt
2260 ./travel_guides/berlitz2/Berlin-WhatToDo.txt
10873 ./travel_guides/berlitz2/Berlin-WhereToGo.txt
3636 ./travel_guides/berlitz2/Bermuda-WhatToDo.txt
10207 ./travel_guides/berlitz2/Bermuda-WhereToGo.txt
2415 ./travel_guides/berlitz2/Bermuda-history.txt
11846 ./travel_guides/berlitz2/Boston-WhereToGo.txt
2087 ./travel_guides/berlitz2/Budapest-History.txt
2758 ./travel_guides/berlitz2/Budapest-WhatToDo.txt
11983 ./travel_guides/berlitz2/Budapest-WhereoGo.txt
3047 ./travel_guides/berlitz2/California-History.txt
2609 ./travel_guides/berlitz2/California-WhatToDo.txt
11961 ./travel_guides/berlitz2/California-WhereToGo.txt
7145 ./travel_guides/berlitz2/Canada-History.txt
37664 ./travel_guides/berlitz2/Canada-WhereToGo.txt
2283 ./travel_guides/berlitz2/CanaryIslands-History.txt
2509 ./travel_guides/berlitz2/CanaryIslands-WhatToDo.txt
12926 ./travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
2503 ./travel_guides/berlitz2/Cancun-History.txt
3066 ./travel_guides/berlitz2/Cancun-WhatToDo.txt
11342 ./travel_guides/berlitz2/Cancun-WhereToGo.txt
4615 ./travel_guides/berlitz2/China-History.txt
2023 ./travel_guides/berlitz2/China-WhatToDo.txt
32211 ./travel_guides/berlitz2/China-WhereToGo.txt
2576 ./travel_guides/berlitz2/Costa-History.txt
2397 ./travel_guides/berlitz2/Costa-WhatToDo.txt
12263 ./travel_guides/berlitz2/Costa-WhereToGo.txt
1897 ./travel_guides/berlitz2/CostaBlanca-History.txt
4906 ./travel_guides/berlitz2/CostaBlanca-WhatToDo.txt
2492 ./travel_guides/berlitz2/Crete-History.txt
2706 ./travel_guides/berlitz2/Crete-WhatToDo.txt
13629 ./travel_guides/berlitz2/Crete-WhereToGo.txt
7973 ./travel_guides/berlitz2/CstaBlanca-WhereToGo.txt
1841 ./travel_guides/berlitz2/Cuba-History.txt
2751 ./travel_guides/berlitz2/Cuba-WhatToDo.txt
12312 ./travel_guides/berlitz2/Cuba-WhereToGo.txt
3125 ./travel_guides/berlitz2/Nepal-History.txt
6805 ./travel_guides/berlitz2/Nepal-WhatToDo.txt
8996 ./travel_guides/berlitz2/Nepal-WhereToGo.txt
3338 ./travel_guides/berlitz2/NewOrleans-History.txt
2210 ./travel_guides/berlitz2/Paris-WhatToDo.txt
11955 ./travel_guides/berlitz2/Paris-WhereToGo.txt
3175 ./travel_guides/berlitz2/Poland-History.txt
3162 ./travel_guides/berlitz2/Poland-WhatToDo.txt
2298 ./travel_guides/berlitz2/Portugal-History.txt
2718 ./travel_guides/berlitz2/Portugal-WhatToDo.txt
19618 ./travel_guides/berlitz2/Portugal-WhereToGo.txt
2208 ./travel_guides/berlitz2/PuertoRico-History.txt
3338 ./travel_guides/berlitz2/PuertoRico-WhatToDo.txt
11341 ./travel_guides/berlitz2/PuertoRico-WhereToGo.txt
2278 ./travel_guides/berlitz2/Vallarta-History.txt
5781 ./travel_guides/berlitz2/Vallarta-WhatToDo.txt
8398 ./travel_guides/berlitz2/Vallarta-WhereToGo.txt

## Example 2
Let's say we've now decided on a place: Italy. We want to know more about restaurants and cafes there. In the command below {} is a placeholder for the file name that find finds, and \; indicates the end of the command to be executed by -exec. The {} placeholder is replaced by the file name for each file that find finds, and the -exec option executes the grep command for each file. The -i option makes the search case-insensitive, and the -E option enables extended regular expressions to allow for the | character to be used for alternation.

Command: 
``find . -name '*.txt' -type f -exec grep -iE 'restaurant|cafe' {} \;``

Output:  
``simplest trattoria or most elegant of restaurants, the experience of
        wonders when entering or leaving a shop or restaurant. In a land where
        restaurant Da Pancrazio, whose cellar shelters ruins of Pompeii’s
        restaurants and boutiques, a vibrant local pride nurtured by economic
        people-watcher’s delight lined with smart cafés and fine restaurants,
        paths lead to farmhouses and rustic mountain-restaurants where you can
        prestigious museums, excellent restaurants and shopping, and
        restaurants, bookshops, and boutiques are showcased in its unabashed
        attractive, modern town full of shops, hotels, and restaurants known
        to spend hours in the restaurants. Naples is where pizza began (the
        Santa Lucia is now lined with elegant hotels and restaurants, many
        cafés and restaurants until the cool wee hours, and restore some of the
        restaurants that stay open until all hours. In the little church of
        ``
