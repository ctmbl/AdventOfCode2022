## 1st of December

### Challenge 1
#### Description
The [challenge](https://adventofcode.com/2022/day/1) is simple: simply find the elf that carry the most calories and give the total calories he is carrying.
Elf's stuff is packed in the [input](./input.txt) by group.

#### Solution 
*see the [code](./chall1.c)*  
*see the [answer](./answer1.txt)*  
I solved the challenge in C language, using `tcc` compiler.  
`tcc` has a `-run` flag which allow to run the binary right after the compilation.  
Then using a shebang like `#!/usr/bin/env tcc -run` allows to simply execute the source code.

Simply sum up every pack of calories into a total until you find an empty line.  
Then compare the current sum to the max you already had and update the max if current is greater.

### Challenge 2
#### Description
Same but now we want the total calories of the 3 most loaded elfs.

#### Solution 
*see [the code](./chall2.c)*  
*see the [answer](./answer2.txt)*  
As the first I used `tcc` compiler.

The only difference here is that we must store the 3 max so a bit of logic is needed to update the lower max (we ensure to always sort the list and replace first).
