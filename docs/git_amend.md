# How to change your last commit

The `git commit --amend` command allows you to edit your most recent commit **before** pushing it to a remote repository. This is useful when:

* You need to edit your commit message, because of a text or formatting error.
* You forgot to stage a file that you had meant to include in the commit.

**Note:** If you need to edit multiple commits, you can do this using `git rebase`. For more information on `git rebase`, see **Rebase**.  

## Change your last commit message

There are two ways you can use `git commit --amend` to change your last commit message. You can edit the commit message you entered previously, or you can enter an entirely new message.  

### Edit the text of your last commit message  

Enter the command `git commit --amend`. This opens the vim editor and displays your previous commit message, which you can edit as required. Press escape to return to command mode, then enter the `:wq` command to save and close the editor.

### Enter a new commit message 
Enter the command `git commit --amend -m "<new commit message>"`, with your new commit message text within the quotation marks.

## Add additional files to your commit
Use `git add` to stage the file that you want to add to your previous commit.  

Enter `git commit --amend --no-edit` to add the file to your previous commit without changing the commit message.  
<br>
<br>
<br>
## Can you change commits that you've already pushed?
 
Use the `git commit --amend` command carefully if you are pushing to a remote repository. If you use the command on a commit you've already pushed, you risk losing data or disrupting your team's work.

An edited commit is actually a new commit. If you use `git commit --amend` to change a commit that you have already pushed, Git will reject it if you try to push it again because it will see it as a conflict. In this scenario, you can use the `--force` option to push the amended commit to a remote repository, but only do this if you are completely sure that no-one has pulled your previous commit.
