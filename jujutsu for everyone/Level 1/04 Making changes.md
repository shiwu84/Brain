---
title: "Making changes - Jujutsu for everyone"
source: "https://jj-for-everyone.github.io/make_changes.html"
author:
published:
created: 2026-04-20
description: "A Jujutsu tutorial that requires no previous experience with Git or other version control systems."
tags:
  - "clippings"
---
## Making changes

Reset your progress

To reset your progress to the start of this chapter, run the following command:

```sh
curl https://jj-for-everyone.github.io/reset.sh | bash -s make_changes
cd ~/jj-tutorial/repo
```

Your primary goal is always to work on a project, Jujutsu just helps you manage your work. So let's pretend we're doing some actual work by putting stuff in a file:

```sh
echo "# jj-tutorial" > README.md
```

When you change files in a directory tracked by Jujutsu, what you're conceptually doing is modifying the working copy commit. Let's see what `jj log` has to say now:

```js
@  mkmqlnox alice@local 2025-07-22 20:19:25 e21958c2
│  (no description set)
◆  zzzzzzzz root() 00000000
```

A couple of things have changed:

- The timestamp of the commit was updated.
- The commit hash changed. That's one of the reasons the commit hash is less interesting, it changes every time anything else in the commit changes.
- The commit is not "(empty)" anymore!

The last point means that our new file was successfully recorded in the working copy commit.

If you want to check the list of changed files, you can do so with `jj status`. The output should include the following, where "A" stands for "added":

```js
Working copy changes:
A README.md
```