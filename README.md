# pmiab

pmiab (Poor Man's Internet Ad Blocker) is a simple bash script that blocks ads and other unwanted nasty stuff and makes surfing the ocean of internet faster, better and safer experience. pmiab does this with the help of hosts file. Using hosts file to block ads has several distinct advantages over other ad blocking methods.


### Advantages :
 - No need to install and run any other applications.
 - Saves CPU, RAM and bandwidth.
 - Blocks IP calls on any port.
 - Faster webpage loading.
 - Enhances your privacy & security.
 - Hosts file can be edited in any text editor.
 - Works with any and every browser.


### How does pmiab work?
pmiab downloads adblocking hosts files from the following four sources,

1. [winhelp2002.mvps.org]
2. [hosts-file.net]
3. [someonewhocares.org]
4. [pgl.yoyo.org]

Then pmiab does some bash magic,

 - Creates a backup of original hosts file and sets it to read-only.
 - Removes MS-DOS carriage returns.
 - Removes all lines that don't begin with 127.0.0.1.
 - Removes any lines containing the word localhost.
 - Replaces 127.0.0.1 with 0.0.0.0.
 - Scrunches extraneous spaces into a single tab.
 - Removes any comments on lines.
 - Cleans leftover trailing blanks.
 - Removes duplicate entries.
 - Creates an ultimate adblocking hosts file.


### Installation :

Installation is very simple. Download [pmiab-master] zip, extract it's contents and copy the file 'pmiab' to '/usr/local/bin/' directory,
```sh
$ sudo cp pmiab /usr/local/bin/
```
And make it executable,
```sh
$ sudo chmod a+x /usr/local/bin/pmiab
```


### Usage :

Open terminal and rum 'pmiab'. That's all you have to do for now. pmiab will create a backup of original hosts file on the first run and save it read-only in your home directory with the name '.hosts-system'. Next pmiab will download four adblocking hosts files from the sources mentioned earlier and after removing crufts-duplicates it will save the ultimate adblocking hosts file in your home directory as '.hosts-block'. Now you have to copy the adblocking hosts file with the following command,
```sh
$ sudo cp ~/.hosts-block /etc/hosts
```
That's it. Restart your browser if it's running, clean browser's cache and enjoy a smooth, ad-free browsing.


### Credits :
 - Steve Riley : This script originally was a brainchild of Steve. Incredibly this was the first bash script he wrote.
 - Stuart Hanzlik : Stuarts articles on hosts file and it's usage as ad blocker provided some valuable information.


### License :

[![Public Domain Mark](http://i.creativecommons.org/p/mark/1.0/88x31.png)](http://creativecommons.org/publicdomain/mark/1.0/)  
This work (<span property="dct:title">pmiab</span>, by [<span property="dct:title">hakerdefo</span>](https://github.com/hakerdefo/pmiab)), identified by [<span property="dct:title">hakerdefo</span>](https://hakerdefo.blogspot.com), is free of known copyright restrictions.


[winhelp2002.mvps.org]:http://winhelp2002.mvps.org
[hosts-file.net]:http://hosts-file.net
[someonewhocares.org]:http://someonewhocares.org/hosts/
[pgl.yoyo.org]:http://pgl.yoyo.org/adservers/
[pmiab-master]:https://github.com/hakerdefo/pmiab/archive/master.zip
