# Berend Python2

## Why This Repo?

This exists because I'm attempting to compile Firefox on MacOS.

That needs python2 (for tests only?) but homebrew no longer ships
python2, and homebrew no longer supports installing from specific
commits.

So you need to install from a local tap (fine)

Firefox ./mach bootstrap fails if homebrew can't update using
git pull/fetch origin master; but a local tap doesn't have an
upstream called origin.  Hence this git repo.

That's also why the main branch is still called master.

From:
https://stackoverflow.com/questions/60298514/how-to-reinstall-python2-from-homebrew

* brew tap-new <user>/homebrew-python2
* brew extract python@2 <user>/homebrew-python2
* brew install /usr/local/Homebrew/Library/Taps/<user>/homebrew-python2/Formula/python@2.7.17.rb

## So Yes

Firefox doesn't need Python2 (it's happy with python3) but it's build
scripts still check for python2.

Python2 can no longer be installed using homebrew (deprecated, that's ok)
or from historic homebrew using a specific commit.

Firefox's build scripts force-update, which force-checks for git
upstream called origin/master

## How do I install these formulae?
`brew install berend/python2/<formula>`

Or `brew tap berend/python2` and then `brew install <formula>`.

## Documentation
`brew help`, `man brew` or check [Homebrew's documentation](https://docs.brew.sh).
