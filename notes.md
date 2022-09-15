## Week 1 Notes

- Arrays are made up of elements.
- Depending on the language used all array's will start from 0
    - Asume any more or online reports assum that they start 1 not 0

- RAM cell holds 1 Byte of data
- EG Interger = 32bit = 4 Cell of RAM

- Use Float instead of Double

- OS will keep the location of the data in RAM in the Memory Map

- PID = Process ID -  this is given to a any new programe that starts up.

Link List

- Made up of Link Nodes conisting of |Data|Address| the data is what is beeing sorted and the address linkes to the next not in the sequneces

- each note points to the next node, and you only need to know when the first one is allocated.

- Array's are declared as 1 large memory allocation. It will use a Link List to split this up across the memeory.

- Link list you can Add / Remove from it, where as from an array your not able too. as well your able to add into the middle of the link list.

- A looped linked list is where the end of the nodes licks back to the start and thier will not be a start/end of the programe.

- Linked Lists are ***One Way*

### Linear Search

- Can only look at one cell at a time

Example Code for a linear search

```c#

int[] n = new n[10] 

n[0] = 5;
n[1] = 49;
n[2] = 36;
n[3] = 11;
n[4] = 9;
n[5] = 24;
n[6] = 81;
n[7] = 79;
n[8] = 83;
n[9] = 50;

int search = 81;
int location = -1;

for(int i = 0; i <= 9; i++){
    if(n[i] == search){
        location = i;
    }
}
Console.Writeline("Number is located at : " + location);
```

Issuse with Linear Search

- Slow
- only good to use with Un-Sorted Data