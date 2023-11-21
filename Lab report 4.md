# Vim

## Step 1: Start
**At the beginning I started at my home directory:** 

*(Image of my home directory)*


![Image](Screenshot 2023-11-19 at 7.31.25 PM.png)

## Step 2: Logging in Using SSH
**Then I logged in using SSH using `<up> <up> <up> <enter>` in order to find it in my search history (three away):**

*(Image of Login)*
![Image](Screenshot 2023-11-19 at 7.34.30 PM.png)

## Step 3: Git Cloning
**Then I typed `Git clone` and followed with the paste command `/+v/` (the SSH link for lab 7 was saved in my clipboard) making a clone:**

*(Image of the Git clone command)*
![Image](Screenshot 2023-11-20 at 2.12.09 PM.png)

## Step 4: Using Cd 
**Then I used `cd` then typed lab followed by`<tab>` (auto-filling it to lab7/)in order to change directories into lab7**

*(Image of me using cd)*
![Image](Screenshot 2023-11-20 at 2.46.08 PM.png)

## Step 5: Running the Tests
**Then I used `bash test.sh` in order to see how the tests ran and noticed the tests had a failure**

*(Image of the failed test cases)*
![Image](Screenshot 2023-11-20 at 4.00.19 PM.png)

## Step 6: Using Vim
**Then I typed `Vim ListExamples.java` in order to open the code on vim**

*(Image of the vim command and the vim page)*
![Image](Screenshot 2023-11-20 at 3.05.09 PM.png)
![Image](Screenshot 2023-11-20 at 3.05.22 PM.png)

## Step 7: Working in Command Mode
**While I was in Vim I checked to see what I needed to fix by scrolling using `<j>` in order to go down. After I located the need to change the code line that read** _index1 += 1_ **I proceeded to change it by hovering over the "1" (in "index1") then pressed `<x>` to delete the one then pressed `<i>` in order to enter insert mode where I would replace it will the correct number `<2>`. Finally, I made sure I exited insert mode by pressing `<esc>` followed by exiting and saving by typing `:wq` or rather `<:> <w> <q>`**

*(Image of the edited line)*
![Image](Screenshot 2023-11-20 at 3.54.34 PM.png)


*(Image of the `:wq` command)*


![Image](Screenshot 2023-11-20 at 3.54.52 PM.png)

## Step 8: Running the Newly Edited Code
**I pressed `<up> <up> <enter>` in order to locate the `Bash test.sh` that I used before and ran the tests again, in which they gave no test failures this time**

*(Image of the `Bash test.sh` working)*
![Image](Screenshot 2023-11-20 at 3.58.50 PM.png)

## Step 9: Wrapping up
**Lastly, I typed out `git add ListExamples.java` in the terminal in order to commit the changes then I typed out `git commit -m "Update"` to give an update message. Then I typed out `git push` in order to push.

*(Image of the git add command)*
![Image](Screenshot 2023-11-20 at 4.19.16 PM.png)


*(Image of the `git commit` message)*
![Image](Screenshot 2023-11-20 at 4.19.46 PM.png)


*(Image of the git push command)*
![Image](Screenshot 2023-11-20 at 4.23.06 PM.png)
