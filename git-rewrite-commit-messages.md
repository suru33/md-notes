```shell script
git rebase --interactive commit_hash^
```
Using Vim you change the words `pick` to `reword` for the commits you want to change, save and `quit(:wq)`.

Then git will prompt you with each commit that you marked as reword so you can change the commit message.

Each commit message you have to save and `quit(:wq)` to go to the next commit message
