# 14 - Git Behind The Scenes: Hashing and Objects

# Overview of this section

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1.png)

## 14.1 What is in `.git`?

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%201.png)

### 14.1.1 Config file

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%202.png)

```bash
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
[remote "origin"]
	url = https://github.com/geor0014/ITP-Git-and-GitHub-Bootcamp.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master
[user]
	email = geor0014@hz.nl
	name = Daniel Georgiev
[branch "1-git-intro"]
	remote = origin
	merge = refs/heads/1-git-intro
[branch "2-basics"]
	remote = origin
	merge = refs/heads/2-basics
[branch "3-commits"]
	remote = origin
	merge = refs/heads/3-commits
[branch "4-branches"]
	remote = origin
	merge = refs/heads/4-branches
[branch "5-conflicts"]
	remote = origin
	merge = refs/heads/5-conflicts
```

### 14.1.2 The Refs Folder

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%203.png)

### 14.1.3 The HEAD file

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%204.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%205.png)

### 14.1.4 The Objects Folder

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%206.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%207.png)

## 14.2 Crash Course on Hashing

### 14.2.1 Hashing Functions

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%208.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%209.png)

### 14.2.2 SHA-1 Algorithm

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2010.png)

## 14.3 The Git Database

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2011.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2012.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2013.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2014.png)

## 14.4 Git hash

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2015.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2016.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2017.png)

## 14.5 Retrieving the hashed data

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2018.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2019.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2020.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2021.png)

## 14.6 Git Blobs

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2022.png)

## 14.7 Git Trees

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2023.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2024.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2025.png)

### 14.7.1 Viewing Trees

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2026.png)

## 14.8 Git Commits

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2027.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2028.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2029.png)

### 14.8.1 The Same, but from a different perspective

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2030.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2031.png)

![1.png](14%20-%20Git%20Behind%20The%20Scenes%20Hashing%20and%20Objects%2050e8dfab7dc0404fb0cc132126361aa6/1%2032.png)