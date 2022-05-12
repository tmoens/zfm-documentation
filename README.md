# Zebrafish Facility Manager Documentation

The deployment documentation is written in markdown.
You use [MkDocs](https://mkdocs.org) to build a static doc
site complete with nice navigation.

MkDocs is written in Python, so you will need to install Python3 (and pip)
inorder to build the documentation. The installation process is
documented [here](https://www.mkdocs.org/user-guide/installation/);

I also use the mkdocs-material theme, so you will have to install that too.
See [here](https://squidfunk.github.io/mkdocs-material/getting-started/#with-pip)

## Policies and Procedures

These are primarily in place to address the requirements of getting an Authorization to Operate
with the NIH.

## Deployment Documentation

Describes how to deploy a Zebrafish Facility Management system.

## Usage Documentation

Marketing and usage of the Zebrafish Facility Manager

## Building the documentation

The process is simple and the same for each document.
As an example, here is how you build the policies and procedures document.

```shell
# in some shell
# go the policies and procedures root
cd policies-and-procedures

# build the site
mkdocs build
```
This generates (or overwrites) the /site subdirectory in policies and 
procedures directory.
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