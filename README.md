# My DIY Bathroom Renovation Project

See mdBook on [Github Pages](https://walquis.github.io/bathroom-reno/).

![](thebook/src/images/IMG_4740.jpg)

## Installing mdBook for building/running

https://rust-lang.github.io/mdBook/guide/installation.html

## Serving the book locally
Use this when authoring.
```
$ mdbook serve  # builds, watches for changes, refreshes local browser on change.
```

## Building and publishing the book
The .github/workflows/publish-mdbook.yml fires a github action that does the honors upon commit to `main`.

```
# Assuming your source code changes have already been added/committed...
$ cd thebook
$ mdbook build
$ cd ..
$ git add docs
$ git commit -m "mdbook build"
$ git push
```

The markdown source code lives in the `thebook/src` directory, which looks like a working website if you click around in it, but you'll notice that some links may not work, there is no table of contents, etc.  When mdBook-built changes in `docs/` are pushed, Github sees them and publishes them properly [here](https://walquis.github.io/git-basics-team-project).  See [Github Pages](https://pages.github.com) if curious how to publish pages from your repos (mdBook is only one of many ways to do this).
