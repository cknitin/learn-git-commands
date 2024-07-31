Sure, let's go through some common Git commands with examples.

### Create Branch

Creating a branch allows you to diverge from the main line of development and continue to do work without messing with that main line.

**Command:**

```sh
git branch <branch-name>
```

**Example:**

```sh
git branch feature-login
```

This creates a new branch named `feature-login`.

To switch to the new branch, you would use:

```sh
git checkout feature-login
```

Or, you can create and switch to the new branch in one command:

```sh
git checkout -b feature-login
```

### Merge Branch

Merging is used to integrate changes from one branch into another.

**Command:**

```sh
git merge <branch-name>
```

**Example:**

Assuming you are on the `main` branch and want to merge changes from `feature-login`:

```sh
git checkout main
git merge feature-login
```

This merges the `feature-login` branch into the `main` branch.

### Stash Changes

Stashing is used to save your changes temporarily without committing them.

**Command:**

```sh
git stash
```

**Example:**

If you have uncommitted changes and need to switch branches:

```sh
git stash
git checkout main
```

To apply the stashed changes later:

```sh
git stash pop
```

### Reset Changes

Resetting is used to undo changes in your working directory or commit history.

**Command:**

```sh
git reset <mode> <commit>
```

**Modes:**
- `--soft`: Moves the HEAD to the specified commit.
- `--mixed`: Moves the HEAD and resets the index, but not the working directory.
- `--hard`: Resets the HEAD, index, and working directory to the specified commit.

**Example:**

To move the HEAD back to a previous commit, keeping the changes in the working directory:

```sh
git reset --soft HEAD~1
```

To reset the index and working directory to the previous commit:

```sh
git reset --hard HEAD~1
```

This command will discard all changes in the working directory and index.

### Full Workflow Example

1. Create and switch to a new branch:

   ```sh
   git checkout -b feature-login
   ```

2. Make some changes and commit them:

   ```sh
   git add .
   git commit -m "Add login feature"
   ```

3. Switch back to the main branch:

   ```sh
   git checkout main
   ```

4. Merge the `feature-login` branch into `main`:

   ```sh
   git merge feature-login
   ```

5. If you have uncommitted changes you need to save temporarily:

   ```sh
   git stash
   ```

6. Later, apply the stashed changes:

   ```sh
   git stash pop
   ```

7. If you need to undo the last commit and keep changes in your working directory:

   ```sh
   git reset --soft HEAD~1
   ```

8. To discard all changes and reset to a previous commit:

   ```sh
   git reset --hard <commit-hash>
   ```

These are some of the fundamental Git commands used for branching, merging, stashing, and resetting. Let me know if you need more details or examples on any specific command!
