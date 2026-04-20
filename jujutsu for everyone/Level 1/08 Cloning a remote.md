---
title: Cloning a remote - Jujutsu for everyone
source: https://jj-for-everyone.github.io/clone.html
created: 2026-04-20
description: A Jujutsu tutorial that requires no previous experience with Git or other version control systems.
tags:
  - clippings
---
## Cloning a remote

Reset your progress

To reset your progress to the start of this chapter, run the following command:

```sh
curl https://jj-for-everyone.github.io/reset.sh | bash -s clone
cd ~/jj-tutorial/repo
```

At the beginning of the tutorial, we started our journey by initializing a completely new project using `jj git init`. We then added a remote later, as a backup solution. In reality, it's often the other way around: You need to work on a repository that already exists.

Let's simulate that situation by deleting our main repository:

```sh
cd ~
rm -rf ~/jj-tutorial/repo
```

Now, we only have the remote repository left. How can we get a "local" copy of it so we can continue working? The jargon for getting a copy of a repo is to **clone** it. The relevant Jujutsu command is named accordingly:

```sh
jj git clone ~/jj-tutorial/remote ~/jj-tutorial/repo
```

The last two arguments are (1) the **source** from which to clone and (2) the **destination** - where to store the cloned repo. When you clone from a remote, you're automatically connected to it with the default name `origin`.

For the tutorial, we also need to recreate our repo-specific authorship configuration:

```sh
cd ~/jj-tutorial/repo
jj config set --repo user.name "Alice"
jj config set --repo user.email "alice@local"
jj metaedit --update-author
```

Let's run `jj log` in our fresh clone to see if everything was restored successfully:

```js
@  upopmymm alice@local 2025-09-06 20:42:45 25716c6f
│  (empty) (no description set)
◆  ytwonzvp alice@local 2025-09-06 20:42:20 main 0a518bdd
│  Add project description to readme
~
```

The most recent commit we made is visible, but its ancestors are hidden. In their place is a tilde **`~`** symbol. Jujutsu uses some rule to determine which commits are probably not interesting to you. These commits are hidden by default in the output of `jj log`. We can tell Jujutsu to show us *all* commits with `jj log --revision 'all()'`:

```js
@  upopmymm alice@local 2025-09-06 20:42:45 25716c6f
│  (empty) (no description set)
◆  ytwonzvp alice@local 2025-09-06 20:42:20 main 0a518bdd
│  Add project description to readme
◆  psnzzpwy alice@local 2025-09-06 20:41:56 02181db9
│  Add readme with project title
◆  zzzzzzzz root() 00000000
```

Both of our commits are here, so our repository was successfully restored from the remote.

You've completed Level 1! 🎉

You made it! At this point, you have all the skills needed for simple solo projects with proper backup. If you're planning to use GitHub, the next chapter is an optional one with tips for that.

Let's summarize the workflow again:

1. make changes
2. create a new commit
3. move the bookmark
4. push to the remote

Ideally, you can take a little break now and practice what you've learned. Once you feel comfortable with the above, come back quickly for level 2. We're just scratching the surface.

If you need to collaborate with other people, level 2 is just as essential as this one. I encourage you keep going right away!