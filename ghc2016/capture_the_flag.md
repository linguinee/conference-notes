# Hacking Like a Champ: Introduction to Capture the Flag Competitions

Lizzy Alonzi, elizabeth.alonzi@jhvapl.edu
Kaitlin Farr, katilin.farr@jhvapl.edu

* [What is a CTF?](#what-is-a-ctf)
  * [Typical CTF Topics](#typical-ctf-topics)
  * [Cool Things You'll Learn](#cool-things-youll-learn)
  * [Well-Known CTFs](#well-known-ctfs)
  * [Where Can I Start?](#where-can-i-start)
* [Before You Start](#before-you-start)
  * [Isolated Environment](#isolated-environment)
  * [Environment](#environment)
  * [Some Useful Tools](#some-useful-tools)
* [Tips](#tips)
  * [Some Classic CTF Problems](#some-classic-ctf-problems)
    * [Steganography](#steganography)
    * [Broken Image](#broken-image)
    * [Mystery String](#mystery-string)
    * [What's the Password?](#whats-the-password)
    * [Reversing](#reversing)
    * [Recon](#recon)
    * [Final Tips](#final-tips)

## What is a CTF?

**C**apture **T**he **F**lag

* Solve puzzles to get flags
* Puzzles relate to:
  * Computer security
  * Hacking
  * Programming
* The harder the puzzle, the more points the flag is worth

### Typical CTF Topics

* Reconnaissance
* Forensics
* Exploitation
* Reversing
* Cryptography
* Web Hacking
* Miscellaneous

### Cool Things You'll Learn

* Password cracking
  * Hashing algorithms
  * Open source tools
* Web hacking
  * Cross Site Scripting
  * SQL injection
* Binary exploition
  * Reverse engineering
  * Debuggers and analysis tools
* Programming
  * Python, C/C++
* …and much more

### Well-Known CTFs

* Universities
  * CSAW (hosted by NYU)
  * Pico CTF (hosted by CMU)
* Conferences
  * DEFCON CTF
  * Ghost in the Shellcode (ShmooCon)
* Some companies offer internal ones
* Many others!

### Where Can I Start?

* Reading writeups
  * ctftime.org
  * github.com/ctfs
* Practice CTFs
  * PicoCTF
    * Always online, entry level
  * HSCTF
    * Made for and by high schoolers
    * Old problems still up
* Other
  * overthewire.com/wargames
  * hackthissite.org
  * CTF Field Guide

## Before You Start

### Isolated Environment

* You'll be downloading problem files and software tools
* Problems may require different OSes
* Virtual machines
  * Virtual Box (free)
  * VMWare (sometimes free)

### Environment

* Kali Linux
  * Linux command line
  * Based on Debian
    * Uses `apt-get`
  * Common security tools pre-installed
    * John the Ripper
    * Wireshark
    * Metasploit Framework

### Some Useful Tools

* Hex editor
  * e.g. Bless hex editor
* Python or other scripting languages
  * Brute forcing something
  * Parsing a lot of data
  * Automation
* Linux utilities
  * `sed` – substitution
  * `awk` – good for on-the-fly scripting
  * `sort` – sorts things
  * `uniq` – removes duplicates

## Tips

* Everything is a clue
  * Title
  * Filenames
  * Very unlikely that any part of the question is irrelevant
* Take advantage of the flag format
  * Typically "flag(…)"
  * `grep`
  * Ctrl + F
* You won't know how to do everything
  * That's OK!
  * Google

### Some Classic CTF Problems

#### Steganography

* Concealing other messages with nonsecret data
* Could be embedded in the image
  * There's a tool for this! Steghide
* What is the image of? Is it a clue?
  * Reverse image search

#### Broken Image

* Is it really an image?
  * `file` command
* Every file type has a signature
  * Could be header and/or footer
  * Is your file signature correct? Use your hex editor!
* Does your file have a checksum?

| Extension | Magic Number                  |
|-----------|-------------------------------|
| .jpg      | FF D8                         |
| .gif      | 47 49 46 38                   |
| .png      | 89 50 4E 47                   |
| .mp3      | 49 44 33                      |
| .mp4      | 00 00 00 18 66 74 79 70 34 32 |
| .zip      | 50 4B 03 04                   |
| .exe      | 4D 5A                         |
| .pdf      | 25 50 44 46                   |
| .ppt      | D0 CF 11 E0 A1 B1 1A E1       |

#### Mystery String

* Hex
  * Is the string only 0-9 and A-F?
  * Online converters
* Base64 encoded string
  * Uses characters 0-9, A-Z, a-z
  * Usually ends in '='
  * Online converters
* Hashes
  * Kali's hashidentifier
* Might be layered (e.g. Hex + Base64)
* Might be done multiple times (e.g. Base64 + Base64)

#### What's the Password?

* Can you view the source?
* If not, what strings can you find?
  * `strings`
* Figure out the language
  * Can you read it? e.g. Python
  * Can you decompile it? e.g. Java
  * Do you need to reverse it? e.g. C++

#### Reversing

* Learn assembly :)
* Lots of tools available
  * Ollydbg (free)
  * IDA Pro (not)

#### Recon

* "Given limited information about a person, find the flag"
* Pay attention to handles
  * Twitter, email, etc.
* Username search sites
  * namechk.com
* Google everything
* Be persistent
* The sky's the limit

#### Final Tips

* Do you see any phrases/words you might be able to Google to try to get the answer?
* Is the wording/phrasing/story of the challenge hinting at something?
* Is there a tool I can find to do what I think I need to do?
* Go over what you know about the problem in your head – you might come up with an answer to one of the above
