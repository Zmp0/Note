# Note Terminal (nt)

`nt` is a simple note-taking script for the terminal. It allows you to add, get, list, and remove notes. The notes are stored in a text file in your home directory.

## Features

- Add notes
- Remove notes
- Copy to the clipboard
- Get specific notes by line number
- List all notes with colored line number

## Commands
```
  -a <note>        Add a new note
  -g <line-number> Get a specific note
  -r <line-number> Remove a specific note
  -c <line-number> Copy a specific note to clipboard
  -rr              Remove all the notes 
  -h               Display help message
```

## Installation

To install `nt`:

 ```

git clone https://github.com/Zmp0/Note.git && cd Note && sudo cp nt /usr/local/bin && nt -a 'Welcome to NoTerminal'

 ```


### Examples

- Add a Note:

```sh

nt -a This is a note
   ```
- Get a Specific Note:

```sh

nt -g 2
   ```
- Remove a Specific Note:

```sh

nt -r 3
   ```
- Copy a Specific Note to Clipboard: for this one you must install 'xclip'

```sh

nt -c 2
   ```
- List All Notes:

```sh

nt
   ```
- Add the output of ls:

```sh

ls | nta
   ```
Add the output of cat on a file:

```sh

cat somefile.txt | nta
   ```   
Add the output of grep:

```sh

cat somefile.txt | grep "pattern" | nta
   ```
- Display Help:

```bash

nt -h
   ```



Useful Alias:


 ```
   alias nta='nt -a'
   alias ntg='nt -g'
   alias ntr='nt -r'
   alias ntc='nt -c'
   alias ntrr='nt -rr'
 ```
