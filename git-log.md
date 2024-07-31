# Git Log

`git log` is a powerful command used to view the commit history of a repository. It can be customized and filtered in various ways to show specific information. Here are some commonly used `git log` commands:

### Basic Commands

1. **Basic Log**:
   ```bash
   git log
   ```
   Displays the commit history.

2. **Single Line Log**:
   ```bash
   git log --oneline
   ```
   Shows each commit on a single line.

3. **Graph Log**:
   ```bash
   git log --graph
   ```
   Displays the commit history as a graph of the branches.

4. **Decorated Log**:
   ```bash
   git log --decorate
   ```
   Shows the commit history with branch and tag names.

### Filtering Commands

1. **Limit Number of Commits**:
   ```bash
   git log -n <number>
   ```
   Limits the output to the specified number of commits.

2. **Commits by Author**:
   ```bash
   git log --author="<author_name>"
   ```
   Filters the commits by a specific author.

3. **Commits Containing a String**:
   ```bash
   git log --grep="<string>"
   ```
   Searches for commits containing a specific string in their messages.

4. **Commits in a Date Range**:
   ```bash
   git log --since="yyyy-mm-dd" --until="yyyy-mm-dd"
   ```
   Filters commits within a date range.

### Formatting Commands
1. **Pretty Format**:
   ```bash
   git log --pretty=format:"%h - %an, %ar : %s"
   ```
   Customizes the log output. Example format includes abbreviated commit hash, author name, relative date, and commit message.

2. **Full Commit Details**:
   ```bash
   git log --pretty=full
   ```
   Shows full commit details including commit and author information.

3. **Fuller Commit Details**:
   ```bash
   git log --pretty=fuller
   ```
   Provides even more details including author and committer information with dates.

### Showing Differences
1. **Show Changes in Each Commit**:
   ```bash
   git log -p
   ```
   Displays the changes made in each commit.

2. **Name-Only Changes**:
   ```bash
   git log --name-only
   ```
   Shows only the names of the files that were changed.

3. **Stat Summary**:
   ```bash
   git log --stat
   ```
   Provides a summary of changes including the number of insertions and deletions.

### Combining Options
1. **Oneline with Graph and Decorate**:
   ```bash
   git log --oneline --graph --decorate
   ```
   Combines a compact view with a graph and decorations.

2. **Changes by Author in Date Range**:
   ```bash
   git log --author="<author_name>" --since="yyyy-mm-dd" --until="yyyy-mm-dd"
   ```
   Filters by author and date range.

3. **Pretty Format with Changes**:
   ```bash
   git log --pretty=format:"%h - %s" -p
   ```
   Customizes the output format and shows changes.

### Other Useful Options
1. **Exclude Merge Commits**:
   ```bash
   git log --no-merges
   ```
   Excludes merge commits from the log.

2. **Follow a Single File**:
   ```bash
   git log --follow <file_path>
   ```
   Displays the commit history for a single file, following renames.

3. **Log with Patch**:
   ```bash
   git log --patch
   ```
   Shows the changes introduced by each commit.

By combining these options, you can tailor the `git log` output to meet your specific needs and get a clear view of the project's history.
