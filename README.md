#multiproject-git-gradle

##Overview

This is gradle script for multi-project git-based setup, configuration and build. It supports automated cloning/pulling 
git-repositories (from any locations, supported by JGit) and typical gradle tasks ("build", "install", etc) that can be
run against some or all projects. Projects can be supplied with inter-project dependencies, so that particular order 
of assembly/testing/etc is guaranteed.

Many thanks to the creators of gradle-git plugin ( https://github.com/ajoberstar/gradle-git ) for their excellent work,
which made is multiproject-git-gradle possible and which is used by it.

##Required files

To start using multiproject-git-gradle, you need two files: 

"build.gradle"  - taken from this repository, this is gradle script. 

"config.gradle" - you write it yourself, according to your needs. You can use "config.gradle" from this repository 
as an example/starting-point for editing. See more information on this in chapter
[Configuration syntax](#configuration-syntax).

##Command line syntax

Like with any other gradle script:

```shell
gradle [some task names specified here]
```

See [Supported Tasks](#supported-tasks) for more information on concrete tasks and their semantics.

It is possible to start gradle without task:

```shell
gradle
```

then the default task [build](#build-task] is executed.

##Supported tasks

###Build task

Iterates all projects described in [configuration](#configuring-projects], performs the following for each project:

Checks whether project exists in the file system. If not, the project will be [updated](#update-task) 
(actually, cloned) from [git-location](#configuring-git-locations).

##Configuration syntax

###Configuring projects

###Configuring git-locations

**More information is coming soon.**
