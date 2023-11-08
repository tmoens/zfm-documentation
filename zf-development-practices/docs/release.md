
## Release management

As of Release 7.0.0 I started using "release-please" which generates a PR 
based on your [conventional commits](https://www.conventionalcommits.org).

In a nutshell, when you do a commit the commit messages is formatted so that
the release-please tool can make a nice list of things that are going into a 
particular release.

In the base directory, if you look at the package.json file you will see that
there is a job called release which runs release please to create a new 
release PR.

It has a GitHub token in it. As I write this, I realize that that is a very 
bad idea.  I have to figure out how I am supposed to do that properly.
