# Website code for Why Not Live in Danville?

## Hugo Theme

```
https://themes.gohugo.io/dimension/
```

## Workflow

1. Clone Site

```
git clone --recurse-submodules https://github.com/chrismetz09/danville-live-site
```

Dimension is a submodule so `--recurse-submodules` must be included in git clone.

2. Add remote repo to local repo

```
christophermetz:danville-live-site $ git remote add smith https://github.com/chrismetz09/danville-live-site.git
christophermetz:danville-live-site $ git remote -v
origin	https://github.com/chrismetz09/danville-live-site (fetch)
origin	https://github.com/chrismetz09/danville-live-site (push)
smith	https://github.com/chrismetz09/danville-live-site.git (fetch)
smith	https://github.com/chrismetz09/danville-live-site.git (push)
```

`smith` is just any old name. It will be used later in the push. If remote add done correctly, `git remote -v` will show the results that should look something like the above.

3. Create Branch to do your work

```
christophermetz:danville-live-site $ git checkout -b 'your-branch-name'
M	readme.md
Switched to a new branch 'your-branch-name'
christophermetz:danville-live-site $ git branch
  master
* your-branch-name
```
Now you can do work in the `your-branch-name` branch. 

4. Hack code and verify locally

```
hugo server -D
```

Your changes will be updated in realtime. Console will explain and check your browser at `localhost:1313`

5. Check Status

```
christophermetz:danville-live-site $ git status
On branch your-branch-name
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   config.toml
	modified:   readme.md

no changes added to commit (use "git add" and/or "git commit -a")
christophermetz:danville-live-site $
```

I do this to visually confirm work so far. This shows 2 x modified files.

6. Move Desired Files to Staging Area

```
christophermetz:danville-live-site $ git add -A
christophermetz:danville-live-site $ git status
On branch your-branch-name
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   config.toml
	modified:   readme.md

christophermetz:danville-live-site $
```

Now we can commit our changes.

7. Commit Changes




