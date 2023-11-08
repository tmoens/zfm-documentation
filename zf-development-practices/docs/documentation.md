## ZFM Documentation

This whole repo contains all the different documentation aspects of the system.
The individual directories are self-explanatory.  On to the mechanics.

### Tools

All the documentation is written in markdown.
You use [MkDocs](https://mkdocs.org) to build a static doc
site complete with nice navigation.

MkDocs is written in Python, so you will need to install Python3 (and pip)
inorder to build the documentation. The installation process is
documented [here](https://www.mkdocs.org/user-guide/installation/);

I also use the mkdocs-material theme, so you will have to install that too.
See [here](https://squidfunk.github.io/mkdocs-material/getting-started/#with-pip)

Each directory has a **docs** subdirectory which holds the raw markdown. It 
also has a **mkdocs.yml** file that tells mkdocs how to assemble an html site 
from those mkdocs documents.

When you build the document, you will get a **site** directory.

### Automated Build and View

In a terminal, just go to a base directory of one of the documents and
```shell
mkdocs serve
```
It will watch for changes and compile on the fly. It also tells you what
port it is serving on.  Just click it, and you will have see the website
update every time you save an edit.

The **mkdocs serve** command has lots of options which might be useful. If you
are building and viewing multiple documents, you will need to use 
```shell
# use whatever port you want - this one uses 8001
mkdocs serve --dev-addr localhost:8001
```

### Building the documentation

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

### Viewing a site

If you want to browse it before deploying it, just right-click the resulting
index.html file in the site directory and "run" it (assuming you are in 
WebStorm).


## Deploying the Documentation

The /site directory is static HTLM, so it's super easy to deploy.

I'll assume you have a server host with a functional web server like Apache.
Also, that you know how configure a site for your documentation pointing
to a root directory.
Set up one such site for each document you want to publish.

Then, for each document you want to publish,
just copy the /site directory to the appropriate site directory on your server.

FWIW, I add a deployment configuration in WebStorm for each document so
that redeploying the site after updates is a breeze.
