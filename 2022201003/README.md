<h4>
This file contains descriptions of the logic used in solving questions 1 and 2 in SSD Lab Activity 2, dated 11th August, 2022.
</h4>



<h6>
For Question 1 :-
</h6>
  
Initially, the number of lines contained in the input file is checked. The input file is given as a command-line argument to the script (i.e., accessed by the script through "$1").<br>
Now, the modulus of number of lines in the file with 2 is determined.<br>
If odd number of lines is detected, then the line having line number ceil(numLines / 2) is printed out.<br>
Else if even number of lines is detected, then the line having line number floor(numLines / 2) is printed out.<br>
"tail -n +N" -> This displays the last (n / 2) lines of the intput file.<br>
"tail -n +N | ... | head -n 1" -> This displays the 1st line of the last (n / 2) lines of the input file.<br> 
Here, its assumed that line numbers start with 1 in each input file.<br>
The input files against which "q1.sh" has been tested are :- "fileOdd.txt" and "fileEven.txt".<br>
In order to test for edge cases, "q1.sh" has also been tested with 2 other files, "file0.txt" and "file1.txt", containing 0 and 1 line espectively.<br>


<h6>
For Question 2 :- 
</h6>
  
"cat /etc/shells" -> This lists out all the shells available in the system.<br>
"cat /etc/shells | grep -w 'usr' " -> This lists out all those shells that belong to 'usr', or that have the substring '/usr/' in them.<br>
"cat /etc/shells | grep -w 'usr' | awk -F'/' '{print $NF}' " -> Here, awk splits a string condiering '/' as the delimiter and $NF basically prints out the last component of the above split.

