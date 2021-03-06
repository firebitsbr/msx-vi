# MSX-vi

A vi text editor clone for the MSX 8-bit home computer.

## Description

MSX-vi is a clone of the vi text editor for the MSX computer.

MSX is a 8-bit computer system created in 1983 by Microsoft and ASCII
Corporation. It was very popular in Japan, some European countries, Korea and
Brazil. Although it's not widely used nowadays, it still has a great number of
enthusiasts creating hardware and software for the platform.

Vi is a text editor originally created for the Unix operating system. It became
very popular and today there are many different clones available on multiple
platforms.

## Minimum requirements

* MSX2 computer (or emulator)
* MSX-DOS2

## History

My passion for technology started when my parents gave me as a present my first
computer. I was 9 years old and the computer was a MSX. At the beginning I was
using it just to play games, but I started learning programming by myself
(first Logo and Basic later). Nowadays I still enjoy playing with MSX and
trying to learn better how it works internally.

Thanks to Javi Lavandeira's tutorials
[Relearning MSX](https://www.lavandeira.net/relearning-msx/) on how to program
with C for the MSX, I started writing my first programs and tests, and I
started to have the idea on writing a vi clone. As far as I know there is
nothing similar on the MSX.

I started writing code, but a text editor is way more complex than it looks.
Memory management was very difficult for my limited C knowledge. At the end I
abandoned the project.

Few months later I discovered the
[Build Your Own Text Editor](https://viewsourcecode.org/snaptoken/kilo/index.html)
tutorial. It is a step by step guide on how to write Antirez's
[kilo](http://antirez.com/news/108) text editor. I started reading it and I
decided to try again writing the vi clone for MSX.

## Download

* [Current releases](https://github.com/fr3nd/msx-vi/releases)

## Online Emulator

Try it online:

* [MSX-vi on WebMSX](http://webmsx.org/?PRESETS=DOS2&DISKA_FILES_URL=https://github.com/fr3nd/msx-vi/releases/download/v0.1.0/vi.zip)

**Note**: In some keyboards, the ```:``` key doesn't work in WebMSX.

## Screenshots

![MSX-vi welcome screen](https://raw.githubusercontent.com/fr3nd/msx-vi/master/img/openmsx0001.png "MSX-vi welcome screen")

![MSX-vi editing large file](https://raw.githubusercontent.com/fr3nd/msx-vi/master/img/openmsx0002.png "MSX-vi editing large file")

## Supported commands

### Exiting and saving

* `:q`: Exit the editor as long there are no changes
* `:q!`: Exit the editor without saving any changes
* `:w`: Save changes to current file
* `:w filename`: Save changes to `filename`
* `:wq`: Save changes to current file and exit

### Movement

* `ESC`: Enter command mode
* `CONTROL d`: Move one page down
* `CONTROL u`: Move one page up
* `h`: Move left
* `j`: Move down
* `k`: Move up
* `l`: Move right
* `0`: Move to the begining of the line
* `$`: Move to the end of the line
* `H`: Go to top of the screen
* `M`: Go to middle of the screen
* `L`: Go to bottom of the screen
* `gg`: Go to the beginning of the file
* `G`: Go to the end of the file
* `w`: Move to next word
* `b`: Move to previous word
* `e`: Move to the end of the word
* `:N`: Go to line `N`

### Deleting text

* `dd`: Delete current line
* `d0`: Delete until the beginning of the line
* `d$`: Delete until the end of the line
* `dG`: Delete ultil the end of the file
* `x`: Delete a single character
* `X`: Delete a single character to the left of cursor

### Inserting text

* `r`: Replace current character
* `a`: Enter insert mode after the cursor
* `A`: Enter insert mode after the current line
* `i`: Enter insert mode at the cursor
* `I`: Enter insert mode before the current line
* `o`: Insert a new line after the current one
* `O`: Insert a new line before the current one

### Search

* `/string`: Search forward for string
* `?string`: Search backards for string
* `n`: Search next ocurrence (forward)
* `N`: Search next ocurrence (backards)


### Other commands

* `:color fg bg bd`: Changes the screen colors
* `CONTROL l`: Refresh screen

## Compile requirements

* SDCC 3.5.0 (it doesn't work with newer versions)
* GNU make
* openMSX (for testing)
