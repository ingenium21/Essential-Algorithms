1.  The section "Rule 4" described a ContainsDuplicates algorithm that has runtime O(N^2) Consider the following improved version of that algorithm:
```
Boolean: ContainsDuplicates(Integer: array[])
        //Loop over all the array's items except the last one.
        For i = 0 to <Largest index> - 1
            //Loop over the items after item 1
            For j = i + 1 To <Largest index>
                // See if these two items are duplicates
                If (array[i] == array[j]) Then Return True
            Next J
        Next i
        // If we get to this point, there are no duplicates
        Return False
    End ContainsDuplicates
```
What is the runtime of this new version?
Answer: It is still O(N^2) because it has a nested loop inside another loop

2. Table 1-1 shows the relationship between problem size N and various runtime functions.  Another way to study that relationship is to look at the largest problem size that a computer with a certain speed could execute within a given amount of time.

For example, suppose a computer can execute 1 million algorithm steps per second.  Consider an algorithm that runs in O(N^2) time.  In 1 hour the computer could solve a problem where N = 60,000 (because 60,000^2 = 3,600,000,000, which is the number of steps the computer can execute in one hour).  Make a table showing the largest problem size N that this computer could execute for each of the functions listed in Table 1-1 in one second, minute, hour, day, week, and year.

    Answer: 
   Computer can run 1,000,000 steps per second.  This means that it can run 60,000,000 steps per minute, and 3,600,000,000
   N = 60,000, then it takes an hour as N^2 = 3,600,000,000