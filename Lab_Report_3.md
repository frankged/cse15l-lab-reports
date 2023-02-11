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

