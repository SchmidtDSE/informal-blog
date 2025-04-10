# DSE informal blog

A place for DSE folks to informally share knowledge.

**Incomplete work is encouraged!**
Please open a PR even if you're not ready to post; sometimes getting a second or third
pair of eyes on your work can help get it ready faster and with higher quality!


## Our Static Site Generator choice

We started with Quarto because running inline code is likely important for our authors.

We considered MyST, but it currently lacks support for a blogging user experience.
We will switch to MyST once it ticks all our boxes!

- [ ] Blogging / listing pages.
- [ ] RSS feed!
- [ ] Support for commenting.


## Quality checks

We use [pre-commit](https://pre-commit.com) for quality checks.
Please run `pre-commit install` after cloning this repo to configure pre-commit.

To autofix a pull request, comment `pre-commit.ci autofix` in the pull request, and a
bot will apply fixes.
