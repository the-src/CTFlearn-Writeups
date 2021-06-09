## 07601
The main idea finding the flag using basic forensics techniques.

#### Step-1:
After we download the given image `AGT.png` from the cloud, we just try simple techniques.

<img src="AGT.png">

#### Step-2:
I first tried a very basic `strings AGT.png` &  `strings AGT.png | grep {`.

I got the following output, through which I came to know about existing hidden directories.
```
...
ABCTF{fooled_ya_dustin}
...
*e
```
#### Step-3:
I tried this `ABCTF{fooled_ya_dustin}` flag, but it showed incorrect. So let's explore the hidden folders.

#### Step-4:
I tried `binwalk -e AGT.png`. I get a new directory called `_AGT.png.extracted`. Let's get into this.

#### Step-5:
The contents of which are some of the images and directory. I directly, tried
`strings I Warned You.jpeg | grep {`

#### Step-6:

I got this output:
```
...
ABCTF{fooled_ya_dustin}
...
*e
```

Luckily, here the flag worked.
#### Step-7:
Finally the flag becomes:
`ABCTF{Du$t1nS_D0jo}1r`
