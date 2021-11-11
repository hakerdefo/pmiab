# pmiab

**pmiab** (Poor Man's Internet Ad Blocker) is a simple bash script that blocks ads and other unwanted nasty stuff and makes surfing the ocean of Internet faster, better and safer experience. **pmiab** does this with the help of hosts file. Using hosts file to block ads has several distinct advantages over other ad-blocking methods.


### Advantages :

 - No need to install and run any other applications.
 - Saves CPU, RAM and bandwidth.
 - Blocks IP calls on any port.
 - Faster web-page loading.
 - Enhances your privacy & security.
 - Hosts file can be edited in any text editor.
 - Works with any and every browser.


### How does pmiab work?

**pmiab** downloads ad-blocking hosts files from the following sources,

1. [MPVS hosts file]
2. [Dan Pollock's hosts file]
3. [yoyo.org hosts file]
4. [Badd Boyz hosts file]
5. [Steven Black's hosts file]
6. [ABUSE.ch hosts file]
7. [AdAway hosts file]

Then **pmiab** does some bash magic,

 - Creates a backup of original hosts file and sets it to read-only.
 - Removes MS-DOS carriage returns.
 - Removes all lines that don't begin with 127.0.0.1.
 - Removes any lines containing the word localhost.
 - Replaces 127.0.0.1 with 0.0.0.0.
 - Scrunches extraneous spaces into a single tab.
 - Removes any comments on lines.
 - Cleans leftover trailing blanks.
 - Removes duplicate entries.
 - Creates an ultimate ad-blocking hosts file.


### Installation :

Installation is very simple. Download **[pmiab-master]** zip, extract its contents and copy the file **pmiab** to **/usr/local/bin/** directory,
```sh
sudo cp pmiab /usr/local/bin/
```
And make it executable,
```sh
sudo chmod 755 /usr/local/bin/pmiab
```


### Usage :

Since **pmiab** deals with the hosts file it needs to be run with **sudo**. Open terminal & run,
```sh
sudo pmiab
```
Or if you prefer **su** over **sudo**,
```sh
su -c pmiab
```
Then you can enable or disable advert blocking via a simple interactive menu of **pmiab**. To block the ads, select **Block Internet Adverts** option from the menu. Restart your browser if it is running, clean browser's cache and enjoy a smoother, safer and ad-free browsing. It is advised that you update the ad-blocking hosts file atleast once in a week. To update the ad-blocking hosts, you need to simply select **Block Internet Adverts** option from the menu.


### Support :

If you like **pmiab**, please consider supporting it, even the smallest contribution goes a long way. It is quick & easy via PayPal, Buy Me a Coffee or Liberapay:  

[![Support via PayPal](https://cdn.jsdelivr.net/gh/twolfson/paypal-github-button@1.0.0/dist/button.svg)](https://paypal.me/hakerdefo)  
[!["Buy Me A Coffee"](https://user-images.githubusercontent.com/1376749/120938564-50c59780-c6e1-11eb-814f-22a0399623c5.png)](https://www.buymeacoffee.com/hakerdefo)  
[![Support via Liberapay](https://liberapay.com/assets/widgets/donate.svg)](https://liberapay.com/hakerdefo/donate)  


### Credits :

 - _Steve Riley : This script originally was a brainchild of Steve. Incredibly this was the first bash script he wrote._
 - _Stuart Hanzlik : Stuarts articles on hosts file and its usage as ad blocker provided some valuable information._


### License :

[![Public Domain Mark](http://i.creativecommons.org/p/mark/1.0/88x31.png)](http://creativecommons.org/publicdomain/mark/1.0/)  
This work (<span property="dct:title">pmiab</span>, by [<span property="dct:title">hakerdefo</span>](https://github.com/hakerdefo/pmiab)), identified by [<span property="dct:title">hakerdefo</span>](https://hakerdefo.blogspot.com), is free of known copyright restrictions.

[MPVS hosts file]:http://winhelp2002.mvps.org/hosts.htm
[Dan Pollock's hosts file]:https://someonewhocares.org/hosts/
[yoyo.org hosts file]:https://pgl.yoyo.org/as/
[Badd Boyz hosts file]:https://github.com/mitchellkrogza/Badd-Boyz-Hosts
[Steven Black's hosts file]:https://raw.githubusercontent.com/StevenBlack/hosts/master/data/StevenBlack/hosts
[ABUSE.ch hosts file]:https://abuse.ch/
[AdAway hosts file]:https://github.com/AdAway/AdAway
[pmiab-master]:https://github.com/hakerdefo/pmiab/archive/master.zip
