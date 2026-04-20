---
title: "Creating a new commit - Jujutsu for everyone"
source: "https://jj-for-everyone.github.io/commit.html"
author:
published:
created: 2026-04-20
description: "A Jujutsu tutorial that requires no previous experience with Git or other version control systems."
tags:
  - "clippings"
---
## Creating a new commit

Reset your progress

To reset your progress to the start of this chapter, run the following command:

```sh
curl https://jj-for-everyone.github.io/reset.sh | bash -s commit
cd ~/jj-tutorial/repo
```

Once we are done with a set of changes, we should create a new commit. If we don't do that, the next changes we make will be recorded into the same commit as the previous ones. That would make it harder to understand the evolution of a project later.

Before we create a new commit, we also need to give a description to the one we've been working on so far. Every commit needs to have a description, even if it's a short one.

So, there are conceptually two things we need to do now:

1. Give a description to the changes we just finished making, the ones that were recorded in the existing working-copy (`@`) commit.
2. Start working on a completely new commit, which is the child of the one we just finished.

A source of confusion if you know Git

This tutorial assumes that you have no experience with Git. However, if you *have* used Git before, it might actually be more difficult for you to understand this. The reason is that both Git and Jujutsu have a subcommand called `commit`, but they work differently.

In Git, changes you make are not recorded automatically into commits. Instead, they exist outside of any commit, until you add them to one manually. The command `git commit` creates a commit containing the new changes as well as the new commit message.

In Jujutsu, there is always a commit already and any changes you make are automatically recorded into it. So, the description you type during `jj commit` will be applied to a commit that has already existed for some time. The *new* commit that's being created is completely empty and has no description. It's ready for auto-recording of the upcoming changes you will be making.

The command to complete both of these tasks at once is:

```sh
jj commit
```

This will open a text editor so you can write a description for the commit. If you followed my instructions during [installation and setup](https://jj-for-everyone.github.io/install.html#installing-a-simple-text-editor), the text editor will be `edit`. When you're done writing the description, click on "File", then "Exit", in the menu bar or press Ctrl+Q to exit the text editor. Confirm that you want to save the file by pressing Enter.

You may notice that the text file doesn't start empty. It already contains a few lines:

```js
JJ: This commit contains the following changes:
JJ:     A README.md
JJ:
JJ: Lines starting with "JJ:" (like this one) will be removed.
```

These lines starting with `JJ:` are *comments*, similar to lines starting with a pound `#` in the terminal. They will not be part of the final commit description, so you don't need to delete them. Jujutsu uses these comments to remind you which files you modified when working on this commit. That can be helpful inspiration for a good commit description.

Here's an example description you could type (or copy-paste) into the text editor:

```js
Add readme with project title

It's common practice for software projects to include a file called
README.md in the root directory of their source code repository. As the
file extension indicates, the content is usually written in markdown,
where the title of the document is written on the first line with a
prefixed \`#\` symbol.
```

There is a little bit of structure here that you should follow. The first line of the description is called the **subject**. Sometimes the subject line is all you need, but to describe your changes in more detail, you can follow it up with a **body**. Subject and body are **separated by an empty line**. Both of them should **not exceed 72 characters** per line.

Commit messages are important, because they make it easier for you and others to understand the changes and their motivation later on. This importance lies on a spectrum: The more people work on a project and the longer-lived it is, the more important good commit messages become. For example, the Linux kernel is a multi-decade project with thousands of people working on it together. Linux developers put a lot of thought and effort into good commit messages. On the other extreme of the spectrum may be a student's repository for storing the homework of a single lecture. The project is over within a couple of months and there is little chance of the student ever digging into the history, let alone anyone else. That student probably won't invest much time into good commit messages.

Let's see the result of running `jj commit` with `jj log`:

```js
@  pwpuwyto alice@local 2025-07-22 20:22:36 35de496a
│  (empty) (no description set)
○  mkmqlnox alice@local 2025-07-22 20:20:34 5b79353a
│  Add readme with project title
◆  zzzzzzzz root() 00000000
```

There are a few things to observe here:

- The new commit is a child of our previous working copy commit.
- The previous commit shows the subject line of the description we gave it.
- The new commit became our working copy, meaning any further file changes will be recorded into the new commit. This marker is not important and you can ignore it.
- The previous commit has a different symbol (circle `○`) than the root commit (diamond `◆`). This is related to an important feature, which we'll learn about later.

We now have the tools for the most basic version control workflow:

1. make some changes
2. create a new commit

Repeating these two steps is what you'll do the most, when working on a version-controlled project.