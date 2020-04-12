# GitWithoutGit

[TOC]

This project wants to do what its' name indicated.

## Git basics

### Generated from `git init`

```shell
$ git --version
git version 2.26.0
$ tree -a
.
└── .git
    ├── branches
    ├── config
    ├── description
    ├── HEAD
    ├── hooks
    │   ├── (12 hook samples)
    ├── info
    │   └── exclude
    ├── objects
    │   ├── info
    │   └── pack
    └── refs
        ├── heads
        └── tags
```
### Generated after `git commit -m`
```shell
.
├── .git
│   ├── branches
│   ├── COMMIT_EDITMSG
│   ├── config
│   ├── description
│   ├── HEAD
│   ├── hooks
│   │   ├── (12 hook samples)
│   ├── index
│   ├── info
│   │   └── exclude
│   ├── logs
│   │   ├── HEAD
│   │   └── refs
│   │       └── heads
│   │           └── master
│   ├── objects
│   │   ├── 73
│   │   │   └── 7af8c86a0c4c1828dc96df4c8f485e4c125413
│   │   ├── 8d
│   │   │   └── ecb9c24f33a06a6d0cde94ca08dd3604bc6516
│   │   ├── ec
│   │   │   └── 11914afef14b19ee159e41f724708724b0a453
│   │   ├── info
│   │   └── pack
│   └── refs
│       ├── heads
│       │   └── master
│       └── tags
└── README.md
```
### How do we get what we want
```shell
$ cat .git/HEAD
ref: refs/heads/master
$ cat .git/refs/heads/master
737af8c86a0c4c1828dc96df4c8f485e4c125413
$ git cat-file -p 737af8c86a0c4c1828dc96df4c8f485e4c125413
tree 8decb9c24f33a06a6d0cde94ca08dd3604bc6516
author Y. Z. Chen <754097987@qq.com> 1586656891 +0800
committer Y. Z. Chen <754097987@qq.com> 1586656891 +0800

{INIT} this repository.
$ git cat-file -p 8decb9c24f33a06a6d0cde94ca08dd3604bc6516
100644 blob ec11914afef14b19ee159e41f724708724b0a453	README.md
$ git cat-file -p ec11914afef14b19ee159e41f724708724b0a453
# GitWithoutGit

[TOC]

This project wants to do what its' name indicated.

## Git basics

### Generated from `git init`

```shell
$ git --version
git version 2.26.0
$ tree -a
.
└── .git
    ├── branches
    ├── config
    ├── description
    ├── HEAD
    ├── hooks
    │   ├── (12 hook samples)
    ├── info
    │   └── exclude
    ├── objects
    │   ├── info
    │   └── pack
    └── refs
        ├── heads
        └── tags
```

### What about the next commit?