# Git-Branching-Project

1. Created Patronus Folder :

```
C:\Dev\Antwalk Training\Git Branching Project> mkdir Patronus

    Directory: C:\Dev\Antwalk Training\Git Branching Project

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        22-01-2023  01:56 AM                Patronus
```

2. Initialised empty Git Repo inside Patronus folder :

```
C:\Dev\Antwalk Training\Git Branching Project> cd Patronus
C:\Dev\Antwalk Training\Git Branching Project\Patronus> git init
```

3. Adding remote origin after creating repo on GitHub :

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [main]> git remote add origin git@github.com:swairik/Git-Branching-Project.git
```

4. Created empty patronus.txt file : 

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [main]> touch patronus.txt
```

5. Added & committed empty patronus file :

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [main +1 ~0 -0 !]> git add .
C:\Dev\Antwalk Training\Git Branching Project\Patronus [main +1 ~0 -0 ~]> git commit -m "add empty patronus file"
[main (root-commit) 367356e] add empty patronus file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 patronus.txt
```

6. Created "**harry**" & "**snape**" branch :

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [main]> git branch harry
C:\Dev\Antwalk Training\Git Branching Project\Patronus [main]> git branch snape
C:\Dev\Antwalk Training\Git Branching Project\Patronus [main]> git branch -a
  harry
* main
  snape
```

7. Moved to harry branch using "**git switch**"

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [main]> git switch harry
Switched to branch 'harry'
C:\Dev\Antwalk Training\Git Branching Project\Patronus [harry]> git branch -a
* harry
  main
  snape
```

8. Added harry's patronus and added and committed : 

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [harry +0 ~1 -0 ~]> git add .
C:\Dev\Antwalk Training\Git Branching Project\Patronus [harry +0 ~1 -0 ~]> git commit -m "add harry's stag patronus"
[harry 08efffe] add harry's stag patronus
 1 file changed, 26 insertions(+)
```

9. Moved to snape branch using "**git checkout**" : 

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [harry]> git checkout snape
```

10. Updated patronus.txt, added & committed in snape branch : 

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [snape +0 ~1 -0 ~]> git add .
C:\Dev\Antwalk Training\Git Branching Project\Patronus [snape +0 ~1 -0 ~]> git commit -m "add snape's doe patronus"
```

11. Created lily branch and moved to it

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [snape]> git branch lily
C:\Dev\Antwalk Training\Git Branching Project\Patronus [snape]> git switch lily
```

12. Modified patronus.txt, added and committed in lily branch :

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [lily]> git status
On branch lily
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   patronus.txt

no changes added to commit (use "git add" and/or "git commit -a")
C:\Dev\Antwalk Training\Git Branching Project\Patronus [lily +0 ~1 -0 !]> git add .
C:\Dev\Antwalk Training\Git Branching Project\Patronus [lily +0 ~1 -0 ~]> git commit -m "add lily's doe patronus"
[lily cc75c4e] add lily's doe patronus
```

13. Used "**git branch -a**" to show all branches : 

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [lily]> git branch -a
  harry
* lily
  main
  snape
```

14. Deleted snape branch using "**git branch --delete snape**" :

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [lily]> git branch --delete snape
Deleted branch snape (was 34024c8).
  harry
* lily
  main
```

15. Pushing all files to remote : 

```
C:\Dev\Antwalk Training\Git Branching Project\Patronus [lily]> git push --all origin
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 8 threads
Writing objects: 100% (12/12), 1.18 KiB | 301.00 KiB/s, done.
Total 12 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To github.com:swairik/Git-Branching-Project.git
 * [new branch]      harry -> harry
 * [new branch]      main -> main
```
