## Rubber Duck
The main idea finding the flag using easiest forensics techniques.


#### Step-1:
After we download `RubberDuck.jpg`, we try to open and see the flag and check if we find any.

<img src="RubberDuck.jpg">

#### Step-2:
I tried simple techniques and easily found answer when we send the command:

`strings RubberDuck.jpg | grep {`

Note: Although some general techniques also include `strings RubberDuck.jpg | grep flag`  & `strings RubberDuck.jpg | grep ctf`.

#### Step-3:
We get the following output:
```
CTFlearn{ILoveJakarta}
...
```

#### Step-4:

Finally the flag becomes:

[comment]: <> (`CTFlearn{ILoveJakarta}`)
