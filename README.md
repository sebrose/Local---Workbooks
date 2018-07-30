# Workbooks

This repo contains the LaTeX source of our training workbooks.

The GitHub repo is linked to (and syncs with) our [ShareLaTeX](https://www.sharelatex.com) account.

It's recommended that you use the online ShareLaTeX editor for editing, but you can also work locally/offline with a bit of setup effort.

## Local setup / offline document rendering

To set up the build tooling locally on a Mac, you can follow the instructions here:

https://thetechsolo.wordpress.com/2016/01/28/latex-on-mac-the-easy-way/

That gives you a GUI app, [TexMaker](http://www.xm1math.net/texmaker/) that's similar to the ShareLaTeX online editor. You'll also find all the binary commands like `pdflatex` and `latexmk` in `/Library/TeX/Distributions/.DefaultTeX/Contents/Programs/texbin`.

## Learning LaTeX

Here is an [excellent introduction](https://www.sharelatex.com/learn/Learn_LaTeX_in_30_minutes) by the makers of ShareLaTeX.

# Code

Each workbook has a folder, and code related to the workbook should be in a
`code/<programming-language>` folder underneath
that folder. For example:

* `testable-architecture/code/java`
* `testable-architecture/code/cpp`

Each of the language subtrees also have a standalone public git repo, which
is intended to be cloned by delegates during the training. This is to avoid
that delegates get a big tree with lots of unrelated files.

The main reason we're using a monorepo is to keep workbooks and code in sync.

Syncing contents between this monorepo and those subtree repos is currently
a manual process, involving copying files. We're looking into using
[git subrepo](https://github.com/ingydotnet/git-subrepo) later to simplify this
process.

*ALL UPDATES SHOULD BE MADE TO THE MONOREPO FIRST*.

## Starting points and worked examples

The starting points for each workbook should always be the `HEAD` of the `master`
branch.

Worked examples are for the benefit of trainers (so they have something to look
at before a training), but also for delegates who wish to see "the solution".

For these reasons, worked examples may exist in both monorepo and subrepo.

Worked examples should be made on a branch in the monorepo. Each branch should
be named `<workbook-name>/<programming-language>/worked-example`, for example:

* `testable-architecture/java/worked-example`
* `testable-architecture/cpp/worked-example`

If a worked example needs to be present in a subrepo as well, name the branch
simply `worked-example`.

## Cyber-dojo versions

Cyber dojo requires all files to be stored in the same folder. Just like worked
examples, these live on separate branches named `<workbook-name>/<programming-language>/cyber-dojo`, for example:

* `testable-architecture/java/cyber-dojo`
* `testable-architecture/cpp/cyber-dojo`

### Importing into cyber-dojo.org

TODO: Document how to do this
