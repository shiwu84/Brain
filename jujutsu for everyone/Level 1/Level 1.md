---
title: "Level 1 - Jujutsu for everyone"
source: "https://jj-for-everyone.github.io/level_1.html"
author:
published:
created: 2026-04-20
description: "A Jujutsu tutorial that requires no previous experience with Git or other version control systems."
tags:
  - "clippings"
---
## Level 1

This level will provide you with the bare minimum of skills you need to get work done. It's only enough for the simplest use cases and you're working on your own. For example, students who track and submit their homework with a Git repository won't need more than this.

The following "cheat sheet" contains the most important commands from level 1. Use it to prime your brain before getting started and remind yourself later when you forget something.

cheat sheet

Configure your authorship information

```sh
jj config set --user user.name "Alice"
jj config set --user user.email "alice@local"
```

Initialize a repository

```sh
jj git init <DESTINATION>
```

Clone an existing repository

```sh
jj git clone <PATH_OR_URL> <DESTINATION>
```

Commit the changes you made

```sh
jj commit
```

Push your latest commit to the "main" bookmark

```sh
jj bookmark move main --to @-
jj git push
```