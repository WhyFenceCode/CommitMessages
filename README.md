# Writing proper commit messages
Commit messages make up an important part of what we do as software developers. Commit messages are a great way to communicate what changes were made, and are essential in projects where multiple people will collaborate. Commit messages must serve a functional purpose of communicating information in a clear and concise way.

## Overview of a commit message
The key to writing a good commit message is structure. Structure helps developers quickly find information in a repeatable manner. Basic commit structure is as follows:

```
<subject>:
<description>

<chores>
```
This commit message contains 3 very important things:
- It contains a subject line, which will tell you about the commit and what it contains.
- The description dives into the details about what the commit will do to the code, and what the expected outcome is.
- Chores are a small part of the commit, made to help with issue tracking.

## The subject line
```
<type>:<section>:<tags>:
```

The subject line contains 3 things, 2 of which are required.

### Type
The type tells us what the commit does:
- `feat` - new feature
- `fix` - a bug fix
- `chore` - dependencies
- `mod` - modifies data while being neither a `feat` or a `fix`
- `refactor` - make changes without changing content
- `revert` - revert to a previous commit
- `initial` - the first commit in a repo

### Section
The section tells us where in the code base changes were made. It can be one of the following:
- `head` - the root of the repository, or changes across the whole repo
- A file name - Changes were only made to that file
- A directory name or 2 - Changes were made underneath that directory

### Tags
Tags tell us quick tidbits of information, helping us find problems faster. Tags are one of the following:

- `NIBC` - No Intended Behavior Change - Use when there is not supposed to be a change to user end behavior in this commit.
- `MBC` - Major Behavior Change - Use when there are known major changes
- `FF` - For Future - Changes do not make sense now, but will make sense a couple of commits down the line

## The description

The description contains the details of the commit, what was changed and why. Each file in the description gets its own block, which looks like this:

```
-<file>
\-<reason>
\-<changes summary>

```

There can be as many blocks as need be in a commit, just leave a line between each.

### File
This is just the name and path to the file.

### Reason
This is the reason why a change was made. There are 2 ways to structure this:

**Fix:** `problem because therefore`, with the problem being the issue that was reported, because being the root cause, and therefor being the reason for addressing this now. This bit can sometimes be paragraphs in length.

**Other:** in all other cases, you just need to write a quick sentence about why a change was made.

### Changes Summary
A short 1-2 sentence summary of what changes were made in the file.

## Chores
Chores have one use: To close issues. Chores is a bullet point list that looks like this:
```
- Closes #<issue number>
```

## Final remarks
We know this is a lot of work, but it is one of the most essential skills that you will learn. A wise programmer one said the following:

>If you do not document your work you will be trapped in a trap of your own making.

This also applies to commit messages. If you keep a good log of what you were doing when you made any changes, then it is easy to come back and edit them.
