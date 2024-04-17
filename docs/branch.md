# Branching

## Local Branches:

1. Create a new branch:
   ```shell
   git branch <branch-name>
   ```

2. Switch to an existing branch:
   ```shell
   git checkout <branch-name>
   ```

3. Create a new branch and switch to it:
   ```shell
   git checkout -b <branch-name>
   ```

4. List all local branches:
   ```shell
   git branch
   ```

5. Delete a local branch:
   ```shell
   git branch -d <branch-name>
   ```

## Remote Branches

1. Push a local branch to a remote repository:
   ```shell
   git push <remote-name> <local-branch-name>
   ```

2. Fetch the latest changes from the remote repository:
   ```shell
   git fetch
   ```

3. Pull the latest changes from a remote branch to the current local branch:
   ```shell
   git pull <remote-name> <branch-name>
   ```

4. Delete a remote branch:
   ```shell
   git push <remote-name> --delete <branch-name>
   ```

5. Track a remote branch and create a corresponding local branch:
   ```shell
   git checkout --track <remote-name>/<branch-name>
   ```

6. Push changes to a remote branch:
   ```shell
   git push <remote-name> <branch-name>
   ```

7. Rename a local branch:
   ```shell
   git branch -m <old-branch-name> <new-branch-name>
   ```

## Synchronizing Local and Remote Branches:

1. Push local branch and set it to track a remote branch:

```terminal
git push -u <remote name> <local-branch-name>
```

2. Fetch the latest changes from all remote branches
```
git fetch --all
```

3. Pull the latest changes from the remote and then merge
```
git pull <remote-name> <branch-name>
```

4. Pull the latest changes and automatically rebase changes on top
```
git pull --rebase <remote-name> <branch-name>
```

## Branch Management

1. rename a remote branch
```
git branch -m <old-branch-name> <new-branch-name>
git push -u <remote-name> :<old-branch-name><new-branch-name>
```

2. set up tracking for an existing remote branch
```
git branch -u <remote-name>/<remote-branch>
```

3. list remote branches
```
git branch -r
```