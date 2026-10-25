# The Occasional

A free, public blog for GitHub Pages where posts go live on the date you choose.

**Start here:** [HOW-TO-POST.md](HOW-TO-POST.md) explains how to put it online and how to write, schedule and edit posts.

## How it works

- Built with Jekyll, which GitHub Pages supports out of the box. You don't need to install anything.
- Posts are Markdown files in `_posts/`. A post dated in the future is left out of the site (`future: false` in `_config.yml`).
- `.github/workflows/publish.yml` rebuilds and deploys the site on every change and every hour, so scheduled posts appear on their own.
