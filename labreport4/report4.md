# __Lab Report 4__  
November 19, 2023  
Nicholas Hubbard  

------------
## Step 4: Log into ieng6
To log into my remote machine, I just run 'ssh cs15lfa23pt@ieng6.ucsd.edu and because of the keygen from weeks ago, I don't need to input my password to login anymore.

## Step 5: Clone your fork of thhe repository from your Github account (using the SSH URL)
\'git clone git@github.com:nhubbard5/lab7.git

## Step 6: Run the tests, demonstrating that they fail
\'cd lab7  
\'bash test.sh  

## Step 7: Edit the code file ListExamples.java to fix the failing test
\'Open the file with \'vim ListExamples.java
Use the following commands:
- \<?>: search in reverse for the following pattern
- \<i>: using 'i' as the pattern highlights the final i, which is in the last repetitition of index1
- \<Enter>: closes the search
- \<e>: goes to the end of the highlighted word, which in this case highlights the '1'
- \<x>: deletes the 1
- \<i>: enter Insert mode
- \<2>: insert the character, 2, which finally makes the change from index1 to index2
- \<Esc>: leave Insert mode
- Type in <:wq> to prepare to save and quit
- \<Enter>: saves and quits

## Step 8: Run the tests, demonstrating that they now succeed
\'bash test.sh

## Step 9: Commit and push the resulting change to your Github account
\'git commit -a  
\<i> to enter insert mode   
Type in the commit message "fixed index1 -> index2"  
\<Esc> to leave insert mode  
\'git push origin
