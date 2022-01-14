\#Git

# Git

## General

Use snapshots to keep track of the state of the folders and files
metadata with information about timestamps when things changed and author.

Use graph tree model. 

tree = folder

files = blob

Snapshots is referring to parent snapshots.

pseudo-code of git : 
\``
type blob : array<byte>
type tree : map\<string , tree | blob>

type commit : struct  {
parents : array of commits
author : string
message : string
snapshot: tree
}

type object : blob | tree | commit

objects : map \<string,object>

def store(o)
id = sha1(o)
object(id) = o

def load(id)

````
return object(id)
````

\``
everything is a reference to sha1 id in snapshots, so snapshot is a reference to the hash of the other snapshot in the commit. Same with parents. 

git is immutable 

The Head is pointing to the last snapshot

## Commands

git ...

### commit

`-a`
Will add all files that are modified to the commit instead of using the `add` command to add files manually that should be used in the commit.

### log

Can visualize the commit history of the repo. 

### reset

Use this if you haven't pushed the repo to the remote, modify the history. So it will be out of sync if you have pushed the changed remote and try using it locally then try to push it remote again.  Use [revert](Git.md#revert) instead of in this case. 

#### HEAD

`git reset HEAD <file>` to unstage the file that you have added with `git add <file>` before commit

git reset HEAD^ = reset one head
git reset HEAD~1 = reset one head as well. But can change 1 to 2 to jump 2 steps.

### revert

Use this if you have pushed your change remote, doesn't modify the history.

### rebase

### branch

`git branch` will show all the branches 

`git branch <name>` will create a branch with that name

### checkout

Move around between the commits in the history. 

`git checkout <file>` will undo the changes to the last state in the HEAD snapshot of that `<file>`. 

`git checkout <hash> -- <file>` will revert the file to that commit state.

### merge

If the branch is based on the branch we are going to merge it in, then it will just fast-forward and no conflict should happen if no commit has happened to the branch you are going to merge it into. 

### diff

`git diff <file>` Showing what has been changed to that file. 

### status

Just tell what is happening right now in the repo.

## Resource

[MIT git lecture](https://www.youtube.com/watch?v=2sjqTHE0zok&list=PLyzOVJj3bHQuloKGG59rS43e29ro7I57J)
