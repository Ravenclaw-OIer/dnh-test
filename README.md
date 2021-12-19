# dnh-test

This project contains prototypes for *Fantastical Physical World*, a Touhou Project fangame currently under development.

## Dependencies
This project depends on ph3sx, a modified version of Danmakufu ph3. 

## Dialogues
The dialogues are automatically generated from `*-dialogue.txt` files. Which is a plain text file formatted below:

```
[character] [sprite_name] : "[text]"
![nonspell/spell]
```

A line prefixed by `!` and followed by either `ns$x` or `s$x`, where $x is an integer, denotes a nonspell or a spell, where output would be separated.

For example:

```
sanae normal : "Example text"
chun normal : "Another example"
!ns1
sanae sad : "We are past nonspell 1"
!s1
!ns2
!s2

```

Sprite images are defined at the beginning of the dialogue file in the following format:

```
@[character name] [sprite name]: "location"
```

For example:

```
@sanae happy: "img/sanae/happy.png"
```
Everything after a `#` and not within a string is ignored.

Note that the intepreter is not happy with bad formats: it merely uses some regex and you won't know why it vomited, so double-check your script before running it.



## Licensing

- All source code (`.dnh` files), excluding dialogue texts, are licensed under the GNU General Public License, version 3 or later.
- All stories (`.txt` files) and dialogues are licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License
- All character-related work, including but not limited to spritepacks, designs, are properties of their respective owners and **are not** subject to the GPL. You **may not** use them unless you get permission from their respective owners. Neither this project nor its contributors may be held liable for any consequences of your use.
- In addition, you should follow Team Shanghai Alice's IP Guidelines