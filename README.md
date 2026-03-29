# Text Editor with Undo/Redo 

A menu-driven C application. It simulates a simple text editor that loads text from a file, supports word-level insertions and deletions, and tracks every change using an undo/redo system.

## How It Was Made

Written in C using two linked-list stacks and one linked-list queue. The text is stored as a 2D array of words in memory. Every insert or remove operation is recorded word by word into the Undo Stack. Undone operations are pushed to the Redo Stack, and any new edit clears the Redo Stack. The queue is used as a buffer to stage words before inserting them into the text and the Undo Stack.

## Features

- Load text from an input file (`input.txt`) into memory
- Insert words at the beginning, end, or after a specific word
- Remove a word or sequence of words from the text
- Undo and Redo operations, each tracked per word with its position and operation type
- Print the current state of both the Undo and Redo stacks without modifying them
- Save the current text to an output file (`output.txt`)

