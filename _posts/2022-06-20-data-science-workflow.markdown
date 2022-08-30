---
layout: post
title:  "Data science development environment: pip, jupyter, virtualenv, pycharm, and AWS"
date:   2022-06-20 00:00:00 -0700
categories: data science
---

I have pinned down my data science/machine learning workflow and wanted to share it.  It is based on using `pip`, `virtualenv`, and `pycharm` and is good for simultaneously writing python packages and doing data analyses in `jupyter`.  My preferred infrastructure solution is AWS.  Disclaimer: I work for Amazon AWS.

### EC2 setup

I consolidate my EC2 setup using `.ssh/Config`, this greatly reduces my setup time.  First, I fire up an EC2 instance, using an AMI such as one of the Deep Learning community images.  I generate or use an existing key-pair `pem` file, and add it to my `~/.ssh` folder.  I copy my Public IP, it looks like `ec2-[IP].compute.1.amazonaws.com`, but may differ.  Then I add this to my `~/.ssh/Config`:

```
Host EC2dev
     HostName ec2-[IP].compute-1.amazonaws.com
     User ubuntu
     IdentityFile ~/.ssh/[MY-PEM-FILE].pem
```

Now my EC2 server has the alias `EC2dev` which I use for the rest of my setup.  This way every time I fire up a new instance, or stop and start this one, I just have to change this IP.

### Python packages and virtualenv on server

Now I am ready to set up my python package, which I usually will host on github.  For example, if I am working on [AutoGluon](https://github.com/awslabs/autogluon) then I will clone the repo on both my server and my local machine.  I use SSH keys for authentication so I need to [add my rsa public keys for both machines to my github settings](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

```
$ cd ~
$ git clone git@github.com:awslabs/autogluon.git
```

Alternatively, I can just scp over my repo on my local machine, which will be what we are effectively doing with pycharm deployment anyway.
On my EC2 server, I will create and activate a virtualenv,

```
$ python3 -m pip install --upgrade pip
$ python3 -m pip install virtualenv
$ python3 -m virtualenv env
$ source env/bin/activate
```

This way I can install my development packages in a contained environment.  I go into the package that I am writing (e.g. `cd autogluon/shift`) and install with `pip install -e .`.  The `-e` flag means that my install updates as I make changes.

### Pycharm

You should start by [installing pycharm](https://www.jetbrains.com/pycharm/).  

To set up pycharm to work with your remote installation you have to set up the
1. Remote interpreter
2. Deployment

To set up the remote interpreter, you need to go to `File > Preferences > Python Interpreter`.  In the settings, add a new interpreter and select SSH Interpreter.  In Host put `EC2dev` and in Username put `ubuntu`.  Then for the interpreter find the location of your virtualenv, i.e. `/home/ubuntu/env/bin/python`.  I will also deploy my project to `/home/ubuntu/autogluon` so I add that mapping to the Sync folders.

To set up my deployment, I go to `Tools > Deployment > Configuration` and either find the SSH connection or add it.  I make sure that the mapping from local path to deployment path matches my project folder in both: `~/autogluon` -> `/home/ubuntu/autogluon`.  You can test the connection.

With this set up you should be able to debug with breakpoints, unittest, and deploy your edits.  If you turn on automatic upload then this should be done for you, but you can manually upload individual files as well.

### Jupyter

First you need to have remote forwarding set up on your local machine.  In your `~/.ssh/Config` file add
```
RemoteForward 8888 EC2dev:22
```

On the remote instance you can launch jupyter and then access it via port forwarding.  The way to do this is to launch a new screen or tmux on the remote server.  Then activate the environment, install and run jupyter.

```
$ ssh EC2dev
$ tmux
$ source env/bin/activate
$ pip install jupyter
$ jupyter notebook
```

The jupyter notebook server should start and you should see an link with a token such as
`http://localhost:8888/?token=...`
Then I turn on ssh forwarding on my local machine with

```
$ ssh -N -f -L localhost:8888:localhost:8888 EC2dev
```

Then copy and paste the link into your browser, and you should see your jupyter instance.

### Other AWS services

There are a host of AWS services, but the ones that I have used the most are the following.

- Sagemaker: this is expecially useful for its [python SDK](https://sagemaker.readthedocs.io/en/stable/) with pyspark support, pretrained models, etc.
- Athena: this is for making serverless SQL queries.  I often find that Athena is faster than using pyspark on a Sagemaker instance (depending on the query).  One common use is to generate a subsample of entries from a database and then load it in jupyter on my EC2 instance.  Then I can do quick data analyses using Pandas, Sklearn, etc. 
- S3: put your data here.
