# Website code for Why Not Live in Danville?

## Hugo Theme

modified3
<br/>
modified4
<br/>
modified5


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

```
christophermetz:danville-live-site $ git commit -s -a -m 'modified readme'
[your-branch-name e7d0de5] modified readme
 Committer: chrismetz09 <christophermetz@Christophers-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 2 files changed, 83 insertions(+), 1 deletion(-)
christophermetz:danville-live-site $
```

You can any comment in quote above.

Next step is push to the remote repo

8. Push

```
christophermetz:danville-live-site $ git push smith your-branch-name
Counting objects: 4, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 1.22 KiB | 1.22 MiB/s, done.
Total 4 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'your-branch-name' on GitHub by visiting:
remote:      https://github.com/chrismetz09/danville-live-site/pull/new/your-branch-name
remote:
To https://github.com/chrismetz09/danville-live-site.git
 * [new branch]      your-branch-name -> your-branch-name
christophermetz:danville-live-site $
```

Note the `smith` was used here. And the branch name is the one defined. You can verify

Before the push

```
christophermetz:danville-live-site $ git branch
  master
* your-branch-name
christophermetz:danville-live-site $
```

Asterik identifies branch you have been working with.

9. Pull Request

Go to `https://github.com/chrismetz09/danville-live-site` and you shoud see name of your branch and green `Compare & pull request` button. Press it.

10. Open Pull Request

You will see green `create pull request`. Press it. If you want to inspect changes prior to pressing green button, scroll down.

11. Merge Pull Request

Some tests may run so give it a minute or two. Then press green `merge pull request`.

12. Successful Merge

Success means purple merge message appears. Look closely and you can delete this branch if you so desire.

13. Update Master and Delete Branch in local repo

Return to command line on laptop.


## Splash Page

![fist splash](img/web-splash.png)

## Hello Square

![hello square](docs/images/hello-square.png)


