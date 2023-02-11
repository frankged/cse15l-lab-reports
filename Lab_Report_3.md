# Lab Report 3
## `grep -r`
From `man grep` found:
```
-r, --recursive
             Recursively search subdirectories listed.  (i.e., force grep
             to behave as rgrep).
```
### Examples:  
`grep -r "cabbage" ./written_2`  
**Result:**  
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt:Stop off at Shannon Falls, a short walk away from the road on an easy gravel path over footbridges into the forest. You can picnic at the bottom of the cliff over which the water cascades. Famous for its August log-rolling contests, the town of Squamish makes a useful base for hiking tours into Garibaldi Provincial Park. The winter sports resort of Whistler offers excellent summer facilities, too: bicycles, kayak and river-rafting or more sedate swimming, golf, and tennis. Take the ski-lift for views across the Coastal Mountains or stroll around Lost Lake — good trout-fishing — but beware of a pretty yellow flower known as skunk cabbage that smells like its name when you pick it.
./written_2/travel_guides/berlitz2/China-WhereToGo.txt:The sightseeing you remember best might be the lively free market lining the hundreds of steps that descend higgledy-piggledy from the hills of central Chongqing to the river. Hustling, bustling peasants hawk the rich harvest of the surrounding farming country: cabbages and oranges, eggs and live chickens (they are weighed while flapping), river fish and squirming eels, and table after table of the most fragrant spices, while stalls and hole-in-the-wall cafés heat up the city’s number-one dish, the Sichuan hotpot.  
`grep -r "higgledy-piggledy" ./written_2`  
**Result:**  
./written_2/travel_guides/berlitz2/China-WhereToGo.txt:The sightseeing you remember best might be the lively free market lining the hundreds of steps that descend higgledy-piggledy from the hills of central Chongqing to the river. Hustling, bustling peasants hawk the rich harvest of the surrounding farming country: cabbages and oranges, eggs and live chickens (they are weighed while flapping), river fish and squirming eels, and table after table of the most fragrant spices, while stalls and hole-in-the-wall cafés heat up the city’s number-one dish, the Sichuan hotpot.

### Utility
* This command is useful because it removes the need for the user to use `find ./ > someFile.txt` and then `grep <string> someFile.txt`, rather it searches recursively from the single command.
* Note for utilizing this is that since it utilizes recursion, running `grep -r` far upstream may be unadvisable due to the vast numbers of sub-directories that may exist.  



## `grep -A [num]`
From `man grep`:
```
-A num, --after-context=num
             Print num lines of trailing context after each match.  See also the -B and -C options.
```
### Examples:
`grep -A 0 "higgledy-piggledy" ./written_2/travel_guides/berlitz2/China-WhereToGo.txt`  
**Result:**  
The sightseeing you remember best might be the lively free market lining the hundreds of steps that descend higgledy-piggledy from the hills of central Chongqing to the river. Hustling, bustling peasants hawk the rich harvest of the surrounding farming country: cabbages and oranges, eggs and live chickens (they are weighed while flapping), river fish and squirming eels, and table after table of the most fragrant spices, while stalls and hole-in-the-wall cafés heat up the city’s number-one dish, the Sichuan hotpot.

`grep -A 1 "higgledy-piggledy" ./written_2/travel_guides/berlitz2/China-WhereToGo.txt`  
**Result:**  
The sightseeing you remember best might be the lively free market lining the hundreds of steps that descend higgledy-piggledy from the hills of central Chongqing to the river. Hustling, bustling peasants hawk the rich harvest of the surrounding farming country: cabbages and oranges, eggs and live chickens (they are weighed while flapping), river fish and squirming eels, and table after table of the most fragrant spices, while stalls and hole-in-the-wall cafés heat up the city’s number-one dish, the Sichuan hotpot.
<mark style="color: blue; background: white">Leading down to the river’s edge, the steep stone stairway known as the Gate to the Sky (Chaotianmen), which appears not to have been cleaned since the Ming Dynasty, is treacherously overlaid with mud and muck, so wear your safest shoes and walk with care. Happily, at the bottom of this long descent there is a terminal for the funicular that returns you to the top of this town, which is so hilly bicycles are almost unknown.</mark>  
- The extra line printed(<mark style="color: blue;background: white">in blue</mark>), is due to the change in our input `[num]` from 0 to 1.
### Utility
* The main utility of this command is to give the user control over the amount of "context" that he/she gets after the instance of the found pattern.



## `grep -l`, `grep --files-with-matches`
```
  -l, --files-with-matches
             Only the names of files containing selected lines are written to standard output.  grep
             will only search a file until a match has been found, making searches potentially less
             expensive.  Pathnames are listed once per file searched.  If the standard input is
             searched, the string “(standard input)” is written unless a --label is specified.
```  
### Examples  
`grep -r -l "cabbage" ./written_2`
**Result:**  
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
./written_2/travel_guides/berlitz2/China-WhereToGo.txt  
`grep -r -l "boom" ./written_2`  
<m style=font-size:8>./written_2/non-fiction/OUP/Berk/ch1.txt
./written_2/non-fiction/OUP/Abernathy/ch3.txt
./written_2/non-fiction/OUP/Abernathy/ch1.txt
./written_2/non-fiction/OUP/Abernathy/ch6.txt
./written_2/travel_guides/berlitz1/HistoryJapan.txt
./written_2/travel_guides/berlitz1/HandRIstanbul.txt
./written_2/travel_guides/berlitz1/IntroEdinburgh.txt
./written_2/travel_guides/berlitz1/IntroIbiza.txt
./written_2/travel_guides/berlitz1/HistoryItaly.txt
./written_2/travel_guides/berlitz1/WhereToGreek.txt
./written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt
./written_2/travel_guides/berlitz1/HistoryMallorca.txt
./written_2/travel_guides/berlitz1/WhereToIndia.txt
./written_2/travel_guides/berlitz1/HistoryLasVegas.txt
./written_2/travel_guides/berlitz1/WhereToMalaysia.txt
./written_2/travel_guides/berlitz1/WhereToJapan.txt
./written_2/travel_guides/berlitz1/WhereToEgypt.txt
./written_2/travel_guides/berlitz1/WhereToIsrael.txt
./written_2/travel_guides/berlitz1/WhereToMallorca.txt
./written_2/travel_guides/berlitz1/IntroHongKong.txt
./written_2/travel_guides/berlitz1/IntroJamaica.txt
./written_2/travel_guides/berlitz1/WhereToIbiza.txt
./written_2/travel_guides/berlitz1/HistoryMalaysia.txt
./written_2/travel_guides/berlitz1/WhereToLosAngeles.txt
./written_2/travel_guides/berlitz1/HistoryFWI.txt
./written_2/travel_guides/berlitz1/WhatToJamaica.txt
./written_2/travel_guides/berlitz1/WhereToHongKong.txt
./written_2/travel_guides/berlitz1/WhereToFWI.txt
./written_2/travel_guides/berlitz1/WhatToLasVegas.txt
./written_2/travel_guides/berlitz2/Costa-WhereToGo.txt
./written_2/travel_guides/berlitz2/Barcelona-History.txt
./written_2/travel_guides/berlitz2/Berlin-History.txt
./written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
./written_2/travel_guides/berlitz2/Bali-History.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
./written_2/travel_guides/berlitz2/Bali-WhereToGo.txt
./written_2/travel_guides/berlitz2/China-WhereToGo.txt
./written_2/travel_guides/berlitz2/California-History.txt
./written_2/travel_guides/berlitz2/Cancun-History.txt
./written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
./written_2/travel_guides/berlitz2/Canada-History.txt
./written_2/travel_guides/berlitz2/Bermuda-history.txt
./written_2/travel_guides/berlitz2/CanaryIslands-History.txt
./written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt
./written_2/travel_guides/berlitz2/Bahamas-History.txt
./written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt
./written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt</m>



### Utility
