# Changing your last commit

The `git commit --amend` command allows you to edit your most recent commit **before** pushing it to the remote repository. This is useful when:

* You need to edit your commit message, because of a typo or a formatting error
* You forgot to stage a file that you had meant to include in this commit

## Changing your most recent commit message

There are two ways of changing your most recent commit message. You can edit the existing message you entered previously, or you can enter an entirely new message.  

### Enter an entirely new commit message: 
Use the command `git commit --amend -m "new commit message."`
Enter your new commit message text within the quotation marks.

### Edit the text of the previous commit:  

Use the command `git commit --amend`. This opens the Vim editor and displays your previous commit message, which you can then edit as required. Press escape to return to command mode, then enter the :wq command to close the editor.

## Adding additional files to your commit
Use `git add` to stage the file that you want to add to your previous commit.  

Enter `git commit --amend --no-edit` to add the file to your previous commit without changing the commit message.

## Things to bear in mind

* If you need to edit multiple commits, you can do this using `git rebase`. For more information, see **Rewriting History**.  
* Don't edit a commit that you have already pushed to the remote repository. An edited commit is actually a new commit, and Git will reject your attempts to push it as it will see it as a conflict. You can use `--force` to push an amended commit to the remote repository, but only do this if you are completely sure that no-one has pulled your previous commit.
