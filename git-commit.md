# Step 1 - Git commit

## Configuration and repo initialisation

Configure your name,email & editor:
```bash
git config --global user.name "Tom Cruise"
```
```bash
git config --global user.email "tom.cruise@example.com"
```

```bash
git config --global core.editor vim
```


Do a cleaning:
```bash
rm -rf exercise/
```

Initialise the git repository (after cleaning):
```bash
git init exercise && cd exercise
```    

Create a file:
```bash
echo "Hello" > hello.code
```



add the file to the staging area:
```bash
git add hello.code
```

Use **git status** to see the file being staged:
```bash
git status
```

commit the file to the repository:
```bash
git commit -m "Helo Volrd feature"
```


We missed the word "World" in last file:
```bash
echo "World" >> hello.code
```

Use again **git status** to see the status of the file:
```bash
git status
```


Use **git commit --amend** to add this to last commit we made and update the title to:
"Hello World feature".
```bash
git commit --amend hello.code
```
exit the "vi" editor with esc+"wq!"

Add "Hello everybody" to this file:
```bash
echo "Hello" >> hello.code
```

Check the difference:
```bash
git diff
```

Commit this change in another commit:
```bash
git commit -am "Hello Everybody feature"
```

Add a new alias to stage and commit in same time:
git config --global alias.your-alias '!git add -A && git commit'

Create another file and commit :
```bash
echo "Bye" >> bye.code
```
commit it:
```bash
git add 
git commit -am "Bye feature"
```

Check your commits and branchs: 
```bash
git log --oneline --decorate
```

Go back to the commit before:
```bash
git checkout HEAD~1
```

Create a new branch:
```bash
git checkout -b mybranch
```

Add this line to the file:
```bash
echo "Hello World" >> hello.code
```
```bash
git commit -am "Really made the thing done"
```

Go to the principal branch "master branch":
```bash
git checkout master
```

Merge mybranch branch to master branch: 
```bash
git merge mybranch
```

You got a conflict: 
```bash
git status
```

Fix the hello.code:
```bash
vi hello.code
```

Fix the hello.code:
```bash
vi hello.code
```


Commit the hello.code:
```bash
git commit -am "new feature"
```