# **Lab Report 4: Vim**
---
## **Step 4 - Log into `ieng6`**
- Key pressed: `ssh xiz189@ieng6.ucsd.edu<enter>`
- It permits me to log into the `ieng6` server without asking for a password, this is because I have previously generated a ssh key that gets stores into my public ssh key on the server. Which allows me to save up the time that are needed for typing in the password, and log in immediately.
- ![Image](ieng6.png)


## **Step 5 - Clone your fork of the repository from your Github account (using the SSH URL)**
- Key pressed: `git clone git@github.com:Xwinner7/lab7.git<enter>`
- It allows me to clone the repository into my terminal with the ssh key that I have generated for GitHub, where I could just use clone from the `SSH` instead of from the normal `HTTPS`. The ssh key generated on the server of `ieng6` has been added as my public key into my GitHub account.
- ![Image](clonelab7.png)
- Key Pressed: `cd lab7<enter>`
- Which permits me to enter into the directory of the cloned repository, with the directory named `lab7`.
- ![Image](cdlab7.png)


## **Step 6 - Run the tests, demonstrating that they fail**
- Key pressed: `ls<enter>`
- Which allows me to see what contents are contained within the `lab7` directory
- ![Image](lslab7.png)
- Key pressed: `bash test.sh<enter>`
- This key runs the script of the JUnit tests
- ![Image](testlab7.png)
  - Where it indicates 1 test failed.


## **Step 7 - Edit the code file to fix the failing test**
- Key pressed: `vim ListExamples.java<enter>` or it could be `vim Li<tab>.java<enter>`
- This command would open the file in vim, the second way to write this command with the `<tab>` fills in the file name to be `ListExamples`, saved a few second to type.
- ![Image](vimlab7.png)
- Key pressed to find and fix the buggy code is: `/index1<enter>`, `n`(9 times), `l`(5 times), `r`, `2`
- This command would search and leads me directly to the word that first appeared that are named as `index1` in the file. And press the `n` key for it to jump to the next search of `index1` and finally stops after pressing it 9 times to where the buggy code is. Next, the `l` key are being pressed 5 times to get to position of the number 1 in the variable name, which is the error to fix. Then press the `r` key to be in insert mode and selected the current index, follow by pressing the `2` key to change the variable name from `index1` to be `index2`
- ![Image](bugfixlab7.png)
- Key pressed: `<esc>`
- This command would exit out of the insert mode
- Key pressed: `:wq<enter>`
- This command allows the change that we made to be saved and exit out of vim.
- ![Image](exitvimlab7.png)

  
## **Step 8 - Run the tests, demonstrating that they now succeed**


## **Step 9 - Commit and push the resulting change to your Github account (you can pick any commit message!)**




take a screenshot, and write down exactly which keys you pressed to get to that step. For special characters like <enter> or <tab>, write them in angle brackets with code formatting. Then, summarize the commands you ran and what the effect of those keypresses were.
