# connor's tex stuff

this repository contains files that I use to ensure consistent structure across my tex documents.

in particular, it does some nice things for me:

- it's easy for me to move between two important categories of tex documents:

   1. minimalist black and white documents for printing
   2. colorful documents for sharing digitally

- i'm able to keep a consistent set of macros and environments across all my projects

- i'm able to easily move _all_ of my quality of life stuff from one class to another using a simple `git clone`.

## notes

each box environment is breakable, but it won't happen automatically. if you want your box to break just specify it in the options:

`\begin{boxDef}[breakable]{Definition} ....`

this is part of a broader theme which is that the options for any box environment just get shot through straight to the tcolorbox options, so you can just throw stuff there to customize the boxes

if you'd like to see some demo material or use my notes/exercises file, they can be found in `demofiles/`.
## todo
- some way of making TODOs apparent

- ToC

- fix issue with boxes taking first letter as title

- "UNFINISHED" boxes in header of problems available as package option?

- make the setup process nice: script to put notes and exercises file in the right place, only structure file in this repo, this repo as submodule of each class