# Note Terminal (nt)

`nt` is a simple note-taking script for the terminal. It allows you to add, get, list, and remove notes. The notes are stored in a text file in your home directory.

## Features

- Add notes
- Get specific notes by line number
- List all notes with colored line numbers
- Remove specific notes by line number
- Copy to the clipboard

## Commands
```
  -a <note>        Add a new note
  -g <line-number> Get a specific note
  -r <line-number> Remove a specific note
  -c <line-number> Copy a specific note to clipboard
  -rr OPTIONS       Remove notes with filtering options:
     -x <numbers>       Remove all notes except specified line numbers
     -tail <count>      Remove the last 'n' notes
     -head <count>      Remove the first 'n' notes
  -h               Display help message
```

## Installation

To install `nt`:

 ```

git clone https://github.com/Zmp0/Note.git && cd Note && sudo cp nt /usr/local/bin 

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
- Copy a Specific Note to Clipboard:

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

grep "pattern" somefile.txt | nta
   ```
- Remove Notes with Filters:

    Remove all notes except specified line numbers:

     ```bash
  nt -rr -x 1 3 5 6
   ```
- Remove notes excluding specific numbers (using / notation):
      
  ```bash
      nt -rr -x 10/20
  ```
- Remove the last 'n' notes (tail):
      
  ```bash
      nt -rr -tail 10
  ```
- Remove the first 'n' notes (head):
      
  ```bash
      nt -rr -head 5
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
