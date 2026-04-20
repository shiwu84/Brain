---
title: "Updating bookmarks - Jujutsu for everyone"
source: "https://jj-for-everyone.github.io/update_bookmark.html"
author:
published:
created: 2026-04-20
description: "A Jujutsu tutorial that requires no previous experience with Git or other version control systems."
tags:
  - "clippings"
---
Reset your progress

To reset your progress to the start of this chapter, run the following command:

```sh
curl https://jj-for-everyone.github.io/reset.sh | bash -s update_bookmark
cd ~/jj-tutorial/repo
```

We have learned how to push a new bookmark to a remote for the first time. We *could* do that for every single commit we create and want to push to the remote. However, that would lead to a lot of unnecessary bookmarks lying around. A real mess!

Thankfully, there's a better way. Instead of creating a new bookmark every time, we can **move** an existing bookmark so it points to another commit.

To try it out, we first need to create a new commit. You can just copy these commands:

```sh
printf "\nThis is a toy repository for learning Jujutsu.\n" >> README.md
jj commit -m "Add project description to readme"
```

The above command uses a neat trick. If you already have a short description in mind, you can pass it directly to `jj commit` with the `-m` flag (short for `--message`). This can be faster than opening a separate text editor.

`jj log` shows us a new commit on top of the one we pushed to the remote:

```js
@  zzywylnt alice@local 2025-07-22 20:36:38 48708b9f
│  (empty) (no description set)
○  kxqyrwux alice@local 2025-07-22 20:36:38 6ca38e90
│  Add project description to readme
◆  mkmqlnox alice@local 2025-07-22 20:25:40 main 7939d4cf
│  Add readme with project title
~
```

Now we can send this new commit to the remote by first pointing the bookmark at it and then pushing the bookmark again. Let's start by moving the bookmark:

```sh
jj bookmark move main --to @-
```

We could've told Jujutsu where to move the bookmark using the change ID, i.e. `--to kxqyrwux`. Alternatively, we can use `@-`, which is a neat way to refer to the **parent of the working copy commit**. There are many such clever ways to refer to commits, but that's a topic for later. For now, just remember `@-`, because that's by far the most useful one.

Let's see what `jj log` has to say:

```js
@  zzywylnt alice@local 2025-07-22 20:36:38 48708b9f
│  (empty) (no description set)
○  kxqyrwux alice@local 2025-07-22 20:36:38 main* 6ca38e90
│  Add project description to readme
◆  mkmqlnox alice@local 2025-07-22 20:25:40 main@origin 7939d4cf
│  Add readme with project title
~
```

The important thing to notice here is that Jujutsu shows us the discrepancy between the local bookmark `main` and its remote counterpart. `main*` is the local bookmark and the star next to the name means it's out-of-sync with the remote. `main@origin` is the location of the bookmark on the remote.

We can fix the situation by pushing the bookmark again:

```sh
jj git push
```

This time, we didn't specify `--bookmark main` explicitly. If you omit the `--bookmark` flag on the `push` command, Jujutsu tries to be smart about which bookmarks you actually want to push. That usually works quite well. If you think it didn't work, just try again with the `--bookmark` flag.

You might be wondering: Since the remote requires a bookmark to receive commits and the `main` bookmark is **not** pointing to the first commit anymore... is that commit now lost or deleted? Luckily it is not. Commits store a reference to their parent commit, which is why Jujutsu knows the order in which to draw the commits in the output of `jj log`. These references form a chain that protects all ancestors of a bookmarked commit from being lost.