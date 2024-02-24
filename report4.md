# Report #4
## Log into ieng6
<img width="566" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/2418aab5-dcf0-4532-b1c0-605fab795ae6">


Keys pressed: `<s> <s> <h> <space> <g> <c> <a> <r> <d> <e> <n> <a> <s> <o> <r> <t> <i> <z> <@> <i> <e> <n> <g> <6> <.> <u> <c> <s> <d> <.> <e> <d> <u> <enter>`

The command ran was `ssh` which allows me to remotely access a server, in this case allowing me to login to my `ieng6` account so I can proceed with the rest of the steps.

## Clone your fork of the repository from your Github account (using the SSH URL)
<img width="566" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/3e0565de-94c0-4e11-9db1-b0f73f28c5f6">


Keys pressed:  `<command + c> <g> <i> <t> <space> <c> <l> <o> <n> <e> <space> <command + v> <enter>`

First, I used `<command + c>` to copy the `ssh` key from github then `<command + v>` to paste the key to use with the `git clone` command. This command clones the repository to my machine for my use.

## Run the tests, demonstrating that they fail
<img width="598" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/c0d9efb4-1bfc-4e14-9c03-778e61ba5ad0">


Keys pressed: `<c> <d> <space> <l> <a> <b> <7> <enter> <b> <a> <s> <h> <space> <t> <e> <s> <t> <.> <s> <h> <enter>`

The command `cd` allows me to switch into the repository that we cloned. Once I was in the `lab7` directory, I run the command `bash` which runs the shell script that contains the commands to run the tests. However, the test fails due to a bug.

## Edit the code file to fix the failing test
<img width="564" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/60be6ea0-124d-4723-9ea6-1fd849fe5e02">
<img width="564" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/c576efca-0e1f-4f41-b904-cbb0213f90ae">


Keys pressed: `<v> <i> <m> <space> <L> <i> <s> <t> <E> <x> <a> <m> <p> <l> <e> <s> <.> <j> <a> <v> <a> <enter> <?> <i> <n> <d> <e> <x> <1> <enter> <i> <delete> <2> <esc> <:> <w> <q>` 

The command `vim` opens up the text editor so once I use that command on the file I want to modify, it will open it and I will be able to modify it. Once I am in the `vim` editor, I use the `<?>` `vim` command which searches the document from back to front since the word I am looking for `index1` is in the back of the code. Once I press enter, it takes me straight to the word where I use the `<i>` `vim` command to enter insert mode which allows me to modify the file directly, then I delete the character and change it. I press `<esc>` to exit insert mode. Then I use the `vim` command `<:wq>` in order to save and quit the file.

## Run the tests, demonstrating that they now succeed
<img width="564" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/9a56607d-293b-4e40-b99c-1ca373824c68">

Keys pressed: `<b> <a> <s> <h> <space> <t> <e> <s> <t> <.> <s> <h> <enter>`

Now that I am out of the file, I use the `bash` command in order to run my shell script. This time all my tests pass.

## Commit and push the resulting change to your Github account (you can pick any commit message!)
<img width="564" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/3a6a62b1-f87a-4bf3-99de-6f855f7c6d20">
<img width="564" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/802988c9-9942-47e3-a6bc-a139c75765da">
<img width="910" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/67ffc238-b1f8-4811-9e9c-4d3e82efdd33">

Keys pressed: <g> <i> <t> <space> <c> <o> <m> <m> <i> <t> <space> <L> <i> <s> <t> <E> <x> <a> <m> <p> <l> <e> <s> <.> <j> <a> <v> <a> <enter> <i> <F> <i> <x> <e> <d> <space> <a> <space> <b> <u> <g> <esc> <:> <w> <q> <enter> <g> <i> <t> <space> <p> <u> <s> <h> <enter>

I use the command `git commit` to commit my changes which opens up the text editor which allows me to input a commit message. Then I use the `<i>` `vim` command to enter insert mode so I can type out my message. After that, I save and quit which commits my changes. Then after that I use the `git push` command to push my changes to the repository.

