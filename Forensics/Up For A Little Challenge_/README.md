## Up For A Little Challenge?
The main idea finding the flag is to consecutively use Forensics commands.

#### Step-1:
After we download `Begin Hack.jpg` from the cloud, we try to understand what is the content. <br>

<img src="Begin Hack.jpg">


#### Step-2:
Then I tried `strings Begin hack.jpg` and got the following output:


```
JFIF
Exif
8Photoshop 3.0
8BIM
8BIM
...
...
`- https://mega.nz/#!z8hACJbb!vQB569ptyQjNEoxIwHrUhwWu5WCj1JWmU-OFjf90Prg -N17hGnFBfJliykJxXu8 -
...
Mp real_unlock_key: Nothing Is As It SeemsU
... 
password: Really? Again
...
flag{Not_So_Simple...}
```

#### Step-3:
This output has opened a lot of gateways for us to explore. So let's try to visit the URL given to us:
https://mega.nz/file/z8hACJbb#vQB569ptyQjNEoxIwHrUhwWu5WCj1JWmU-OFjf90Prg

We get a new zip file there named `Up For A Little Challenge.zip`. 
 
#### Step-4:
After we unzip and try to find content (including all hidden files, by `ls -al`), I found the directory `Did I Forget Again?` and in that I found an image and another compressed file called `.Processing.cerb4`.

#### Step-5:

When I tried to unzip it, I found an image `skycoder.jpg` which was encrypted.

This is the time you have to be little smart and try the password from given things only. I tried to search above strings search and found password there: `Nothing Is As It Seems`. 

#### Step-6:
Finally we get this image. Flag is right bottom corner.

<a href="https://ibb.co/3pb7kpN"><img src="https://i.ibb.co/HtyVXtz/skycoder.jpg" alt="skycoder" border="0"></a>

#### Step-7:
Finally the flag becomes:
`flag{hack_complete}`
