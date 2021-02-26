Add the "upstream" to your cloned repository ("origin"):
```bsh
git remote add upstream git@github.com:original_author/project_name.git
```
Fetch the commits (and branches) from the "upstream":
```bsh
git fetch upstream
```
Switch to the "master" branch of your fork ("origin"):
```bsh
git checkout master
```
Stash the changes of your "master" branch:
```bsh
git stash
```
Merge the changes from the "master" branch of the "upstream" into your the "master" branch of your "origin":
```bsh
git merge upstream/master
```
Resolve merge conflicts if any and commit your merge
```bsh
git commit -am "Merged from upstream"
```
Push the changes to your fork
```bsh
git push
```
Get back your stashed changes (if any)
```bsh
git stash pop
```
You're done! Congratulations!
