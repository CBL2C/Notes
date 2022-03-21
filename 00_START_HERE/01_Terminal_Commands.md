# Terminal Commands
**List files in the current directory**

```js
ls                     // show every file and folder in the directory
```
**Flags:** a dash - signifies a flag

Flags come after commands

```js
-a                     // Flag to show hidden files
ls -a                  // shows hidden files as well in the directory
```

<br>

**Change directiories**
```js
cd                     // change dirctory eg cd C:\
cd C:/

cd ..                  // go up one directory
cd ../..               // go up two directories etc
```

<br>

**Make a new directory**
```js
mkdir                  // make a new directory in the current directory you are in

mkdir test_directory   // make new directory test_directory in the current directory

mkdir test_directory2/nested_directory
                       // make a new directory in the current directory you are in
```

<br>

**Make a new file**
```js
touch                  // make a new file inside your current directory
touch test.js          // make new file test.js inside your current directory
```

<br>

**Show where you currently are**
```js
pwd                    // show the current directory you are in
                       // stands for "present working directory"
```

<br>

**Print out a file**
```js
cat                    // print out a file
cat test.js            // print out the contents of test.js
```

<br>

**Remove a file or directory**
**DESTRUCTIVE. BE CAREFUL. THERE AIN'T NO UNDO HERE**
```js
rm                     // removes a file / directory
rm test.js
rm -i                  // asks for verification (proceed? y/n)
rm -r                  // recursive
```