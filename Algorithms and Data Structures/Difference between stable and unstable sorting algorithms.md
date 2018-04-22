## What is stable and unstable sorting algorithms?
A sorting algorithm is stable if it maintains the relative order of numbers/records in the case of tie i.e. if you need to sort 1 1 2 3 then if you don’t change order of those first two ones than your algorithm is stable, but if you swap them then it becomes unstable, despite overall result or sorting order remain same.

This difference becomes more obvious when you sort objects e.g. sorting key value pairs by keys. In the case of a stable algorithm, the original order of key value pair is retained as shown in the following example.

`INPUT: (4,5), (3, 2) (4, 3) (5,4) (6,4)`

Stable algorithm:  
`OUTPUT1: (3, 2), (4, 5), (4,3), (5,4), (6,4)`  
Unstable algorithm:  
`OUTPUT2: (3, 2), (4, 3), (4,5), (5,4), (6,4)`

