# Git



@[TOC]
#  1.  操作命令

## 1.1 下载代码
github代码下载到本地。

	git clone https://github.com/huzhengxing/spring-cloud-demo.git

## 1.2 拉取代码
远程仓库代码，更新到本地。

	git pull


## 1.3 上传代码
本地已经git commit文件上传的远程仓库。(先git pull,再git push)

	git push



## 1.4 提交代码本地

	git commit -m "备注"


## 1.5 查看本地提交的代码
	git status


## 1.6 删除本地仓库代码
已经git commit 的文件

	git rm -r --cached fileName


## 1.7  查看分支 

	git branch

## 1.8  创建分支

	git branch branchName




## 1.9  添加远程仓库
远程已经创建仓库,本地代码同步到远程仓库。

	git remote add origin [远程地址]


## 1.10  添加远程分支
本地代码同步到远程仓库，添加分支，才能提交上传代码。

	 git pull origin master