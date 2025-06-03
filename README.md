# Tennis Canada Rankings and Stats Admin Documantation

The deployment documentation is written in markdown.
You use [MkDocs](https://mkdocs.org) to build a static doc
site complete with nice navigation.

MkDocs is written in Python, so you will need to install Python3 (and pip)
inorder to build the documentation. The installation process is
documented [here](https://www.mkdocs.org/user-guide/installation/);

I also use the mkdocs-material theme, so you will have to install that too.
See [here](https://squidfunk.github.io/mkdocs-material/getting-started/#with-pip)

## Deployment Documentation

Describes how to deploy a the software


## Development Practices

Just a record of how we generally approach development, which tools we use and 
so on.  It helps for remembering things like how to create a release or the 
general approach taken in writing automated tests.

## Building the documentation

The process is simple and the same for each document.
As an example, here is how you build the policies and procedures document.

```shell
# in some shell
# go the policies and procedures root
cd tc-deployment-docs

# build the site
mkdocs build
```
This generates (or overwrites) the /site subdirectory tc-deployment-docs
If you want to browse it before deploying it, just right-click the resulting 
index.html file and "run" it.

The /site directory is static HTLM, so it's super easy to deploy.

## Deploying the Documentation

I'll assume you have a server host with a functional web server like Apache.
Also, that you know how configure a site for your documentation pointing
to a root directory.
Set up one such site for each document you want to publish.

Then, for each document you want to publish, 
just copy the /site directory to the appropriate site directory on your server.

FWIW, I add a deployment configuration in WebStorm for each document so
that redeploying the site after updates is a breeze.
