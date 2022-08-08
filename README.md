# python-for-devops-aug-2022
From Zero Repo for doing devops work

## Status

[![Test Multiple Python Versions](https://github.com/tim-webster-7D/python-for-devops-aug-2022/actions/workflows/main.yml/badge.svg)](https://github.com/tim-webster-7D/python-for-devops-aug-2022/actions/workflows/main.yml)

## Create a project scafford

Create dev enviroments that are cloud based: 

### Colab Notebook

this is some documentation of how to use [colab](https://github.com/tim-webster-7D/python-for-devops-aug-2022/blob/main/getting_started_pthyon.ipynb)
[colab url](https://colab.research.google.com/)

### Github Codespaces

Build out pythin scaffold
* Makefile (i.e think cookbook) keeps track of complex things
  * touch Makefile - `touch` command great for building out an empty file
  * mkdir -- create a directory
  * *[init].py* tells the python interpreter where there will be some source code
* requirements.txt - for python
* test - test_library.py
* python library
* Dockerfile - build out containers
* Commandline tooling
* Microservice

1. Create virtualenv - virtual environment `virtualenv ~/.venv`
   1. This creates a virtual environment inside the home dir as an invisable directory
2. edit my `~.bashrc`
   1. it will load it everytime I open an interprteur
   2. vim `~/.bashrc` scroll to bottom shift + g, o for new line
   3. add source ./venv/activate


### AWS Cloudshell
### AWS Cloud9

*Tip*
. Show hidden files
. To get out of python virtual enviroment type `deactivate`
. 'which ipython' to see where you are running python i.e. from venv or local

Things to note when using the cloud based environments. There could be modules installed you don reall need check:
1. `pip freeze | less` or `pip freeeze | wc -l` to see how many modules libraries that are installed ![image](https://user-images.githubusercontent.com/32961611/183281416-29ee4163-d530-4b08-b57a-7b668a9bbd04.png)
2. this is why virtual invironments are important us control what is installed ![image](https://user-images.githubusercontent.com/32961611/183281385-ed76b440-e485-41b7-bf63-860c3bcb3db1.png)
3. Good practise would be to create a virtual enironment `python3 -m venv ~/.venv` *remember bashrc*
   1.`## sourcing virtual env
     source ~/.venv/bin/activate`
4. Open new terminal to launch a new virtual eniroment - you can now build out the libraries your need
5. Check libaries they are now zero ![image](https://user-images.githubusercontent.com/32961611/183282363-1c7ff259-3d2c-46ea-9197-ed9dc3401c70.png)

*requirements.txt*
1. used to explicitly say what you want installed in your project no guessing here
2. Library and version listed
3. Make installation part of your makefile

*Makefile*
1. Makefile should alway be tabs could cause problems.
2. Example below REMEBER to save file

`install:
	pip install --upgrade pip &&\
		pip install -r requirements.txt`

3. then browse to directory and execute `make install`
4. you can then list you libaries for versions and pick the copy the verions to your makefile
5. This way you know that this verison will always be correct going forward ![image](https://user-images.githubusercontent.com/32961611/183282908-cde137c4-5ad1-4b19-8e1b-dade93104144.png)
6. This is best practise for reusable code

## Coninious integration

There are many ways to automat. Many ways to do continuous intregration 
	GitHub actions
	AWS Build system
	
### GitHub Actions

Designed for you to do devops. Build, test, and deploy your code. 

You can find tons of deployment recipes. 
As long as you have `.github/workflows/` it will run the file in yml/style format in there it will run

Nice idea to add status badges to your README from github actions.

yml file failing because we dont have any steps for make lint, test or format

Build out some python commands i.e. random fruit call it in hello.py

Add to make file pylint commands 
	pylint commad is 'make lint'

## Command-Line Tools

## Microservices

## Containerized Continuous Delievery
