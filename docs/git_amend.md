# Changing your last commit
--

The `git commit --amend` command allows you to edit your most recent unpushed commit. This is useful when:

* You need to edit your commit message, because of a typo or a formatting error
* You forgot to stage a file that you had meant to include in this commit

## Editing your most recent commit message

There are two ways of editing your most recent commit message.  

To enter an entirely new commit message, use `git commit --amend -m "this is the text of the new commit message."`

To edit the text of the previous commit:  

Enter `git commit --amend`. This opens the Vim editor and displays your previous commit message. Edit the message as required. Press escape to return to command mode, then enter the :wq command to close the editor.

## Adding additional files to your commit
Use `git add` to stage the file that you want to add to your previous commit.  
Enter `git commit --amend --no-edit` to add the file to your previous commit without changing the commit message.

You can now push your changes as normal.

## Things to bear in mind

If you need to edit multiple commits, you should instead use `git rebase`. For more information, see **Rewriting History**.
Don't edit a commit that you have already pushed. This
