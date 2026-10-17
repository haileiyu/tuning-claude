# Too much detail

**Question:** How do I undo my last git commit but keep the changes?

## Before

> Great question! There are several ways to approach this depending on your needs.
>
> The most common approach is to use `git reset --soft HEAD~1`. This will undo the commit while keeping your changes staged.
>
> A few other things worth considering:
>
> 1. If you've already pushed, you may want to use `git revert` instead to avoid rewriting shared history.
> 2. You can use `git reflog` to recover commits if something goes wrong.
> 3. Consider setting up a git alias like `git undo` to streamline this workflow.
>
> Let me know if you'd like me to elaborate on any of these options!

## After

> `git reset --soft HEAD~1`
>
> If you already pushed, use `git revert HEAD` instead.
>
> <details>
> <summary>More</summary>
>
> - If something goes wrong, `git reflog` finds the old commit.
> - To make a shortcut: `git config --global alias.undo 'reset --soft HEAD~1'`
>
> </details>

The pushed case stays in the main answer because it prevents a real mistake. Reflog and the alias go into the zippy.
