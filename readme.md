# connor's tex stuff

this repository contains files that I use to ensure consistent structure across my tex documents.

in particular, it does some nice things for me:

- it's easy for me to move between two important categories of tex documents:

   1. minimalist black and white documents for printing
   2. colorful documents for sharing digitally

- i'm able to keep a consistent set of macros and environments across all my projects

- i'm able to easily move my quality of life stuff from one place to another using a simple sh script.

## notes

if you'd like to see some demo material or use my notes/exercises files, they can be found in `demofiles`.

### minimal files

if you specify `minimal=true` as an option in the usepackage line for structure.sty your file will compile not with colorful boxes, but greyscale boxes of a slightly different design.

this is so you can easily switch between economical, minimalist files for printing and colorful, pretty files for digital viewing. 

### box options

each box environment is breakable, but it won't happen automatically. if you want your box to break just specify it in the options:

`\begin{boxDef}[breakable]{Definition} ....`

this is part of a broader theme which is that the options for any box environment just get shot through straight to the tcolorbox options, so you can just throw stuff there to customize the boxes

### tagging boxes as unfinished

if you want to tag things as "unfinished" with a red box, use
`\begin{boxDef}[after title=\unfinished]{}...`

i'd like to have it so that you can just pass `unfinished` as the box option, but that's still a work in progress

### counters

right now counters are numbered independently of anything. you can pass `sectioncounter=true` as an option to have counters numbered within sections. the implementation of this is actually revolting and I want to have it be able to number within any counter, but that's hard.

## todo
- some way of making TODOs apparent

- ToC

- fix issue with boxes taking first letter as title

- "UNFINISHED" boxes passed as option to box

- fix hypertarget for each box

- maybe all boxes should be breakable by default?

- it would be nice if you could just pass a counter itself as an option for boxes to be numbered with. `tcolorbox` has a mechanism for this using the `use counter=` option, but i can't get it to work