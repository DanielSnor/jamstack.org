---
title: blog.sh
repo: DanielSnor/blog.sh
homepage: https://blogsh.app
language:
  - Ruby
license:
  - MIT
templates:
  - ERB
  - Markdown
description: A blog engine you run from a terminal, where posts are JSON files and comments live on the Fediverse.
---

./blog.sh is a static site generator for blogs, written in Ruby's standard library and bash -- no gems, no npm, no lockfile. One post is one JSON file of typed blocks, the site is a static build, and authoring happens in an interactive terminal wizard instead of a browser admin.

### Comments without a comment system

Every published post is announced on Mastodon or Bluesky, and the replies to that announcement are the post's comments, loaded by the reader's browser from the public API. There is no comment database to host, moderate or migrate.

### Bring your archive

Eight importers cover Tumblr, Twitter/X, WordPress, RSS/Atom, Mastodon, Pixelfed, Bluesky and Instagram exports. Media is downloaded and stored next to its post rather than hotlinked, so a dead CDN does not take the images with it.

### Deploy anywhere

Six backends -- Surfer, local copy, rsync, git/Pages, rclone and SFTP -- sit behind one manifest-driven diff with SHA-256 checksums, dry runs, opt-in pruning, and shrink and growth guards that refuse to publish a build that suddenly lost half its pages.
