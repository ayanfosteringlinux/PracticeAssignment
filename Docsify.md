![download](https://github.com/ayanfosteringlinux/StuFFs/assets/153751979/fa219eb8-f8b0-4b3f-843a-8f0ac588848b)

# **Docsify**

>**What it is**

Docsify generates your documentation website like hot knife on butter. It doesn't generate static html files. Instead, it smartly loads and parses your Markdown **(.md)** files and displays them as a website. To start using it, all you need to do is create an ```index.hmtl```

>**Features**

* No statically built html files
* Simple and lightweight
* Smart full-text search plugin
* Multiple themes
* Useful plugin API
* Emoji support
* Support server-side rendering

# **Setup & Installation**

> **My Environment**

PRETTY_NAME="Ubuntu 23.10"
NAME="Ubuntu"
VERSION_ID="23.10"
VERSION="23.10 (Mantic Minotaur)"
VERSION_CODENAME=mantic
ID=ubuntu
ID_LIKE=debian

> **Pre-Requisite**

* Internet connection. So that the packages can be downloaded


>**Step 1**

To install Docsify on your machine, open *Terminal* in your machine or you can use the shortcut```Ctrl+Alt+T``` and follow the commands below.

Prior to start, you have to install some important dependencies to run Docsify

```bash
sudo apt update
```
It will update package lists and synchronizes the packages to the latest

<br>

```bash
sudo apt install nodejs
```
As we know, ```Node.js``` is a ```JavaScript``` runtime environment. Therefore, it is essential to have ```Node.js``` installed on your machine before installing ```Docsify``` as because Docsify itself runs on ```Node.js``` and cannot run without Node.js because of dependencies & package management (```npm```)

<br>

```bash
sudo apt install npm
```
```Node.js``` comes with ```npm```(Node Package Manager), which is used to install and manage packages such as ```Docsify```. npm allows you to easily install Docsify globally or locally, manage its dependencies, and update it when necessary.

>**Step 2: Start**

It is recommended to install ```docsify-cli``` globally, which helps initializing and previewing the website locally.

Run the following command in *Terminal*

```bash
npm i docsify-cli -g
```
>Output :

```
ayan@Sudo:~$ sudo npm i docsify-cli -g
[sudo] password for ayan: 

changed 204 packages in 17s

16 packages are looking for funding
  run `npm fund` for details
  ```
  My output is different just because I've already installed Docsify.

>**Step 3: Initialize**

Now, Docsify has been succesfully installed in your machine. Lets move ahead to initialize Docsify.

Run the following commands in *Terminal*

```bash
docsify init ./docs
```
This will initiate a file named as ```docs``` containing ```index.html``` & ```README.md```

Now, installation is completed

# **Writing Content**

After ```init``` process is complete, you can find the file list in the ```./docs```
subdirectory.

* ```index.html``` is the entry file
* ```README.md``` is the homepage in which you can write your content
* ```.nojekyll``` prevents GitHub Pages from ignoring files that begin with underscore

# **Preview your site**

If you want to preview your written content, run the below commands

```bash
docsify serve
```
It will run the local server as Docsify. Now preview your site in your browser on
```bash
http://localhost:3000
```
<br>

# **Congrats** 

Now you have successfully installed ```Docsify``` and have initiated ```index.html``` & ```README.md```, you are ready to make a documentation site by writing your content in ```README.md```.

<br>

**Thanks & Regards <br>
Belal Ahmad Kureshi <br>
KeenAble Computers Pvt. Ltd.**
