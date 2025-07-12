# Reverse Engineering C++ Program 

Challenge site: [CTFLearn](https://ctflearn.com/challenge/379)<br>
Tools used =
**Ghidra**<br>

## Methods

1. Open Ghidra, then make a new project<br>
![Ghidra](Screenshot_20250713_001448.png)
2. Put the rev1 file into the project folder<br>
![Project Folder](Screenshot_20250713_002005.png)
3. Double click on the file, and when it ask to analyze the file, click yes.<br>
![Analyze](Screenshot_20250713_002153.png)
4. Choose analyze too in here<br>
![Analyze2](Screenshot_20250713_002249.png)
5. Find the function that handles the pin check, which in this case is cek(). Here, Ghidra already gives us the answer in a comment. The letter H in the end of the numbers means that its a hex code. <br>
![Analyze3](Screenshot_20250713_002616.png)
6. Decode that hex code back to decimal.
7. Try inputting it in the program. If succeeds, then thats the flag.



