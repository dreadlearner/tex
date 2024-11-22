# connor's tex stuff

this repository contains files that I use to ensure consistent structure across my tex documents.

in particular, it does some nice things for me:

- it's easy for me to move between two important categories of tex documents:

   1. minimalist black and white documents for printing
   2. colorful documents for sharing digitally

- i'm able to keep a consistent set of macros and environments across all my projects

- i'm able to easily move _all_ of my quality of life stuff from one class to another using a simple sh script.

## notes

if you'd like to see some demo material or use my notes/exercises files, they can be found in `demofiles/`.

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

if you want your counters to be just a single number, pass the option `singlecounter` to `structure`. if you do not pass this, by default boxes will be numbered within each section.

if you'd like your counters numbered within some other counter, pass the option `counterwithin=<YOURCOUNTER>`.

the way this is implemented sucks, it literally just appends `YOURCOUNTER.` to the front of the counter, and ensures that the counter reindexes after every iteration of `YOURCOUNTER`.

## todo
- some way of making TODOs apparent

- ToC

- fix issue with boxes taking first letter as title

- "UNFINISHED" boxes passed as option to box

- allow counters to index within whatever other counter

- fix hypertarget for each box

- there may be some testing remnants in `exercises` and `notes`. fix those.

- maybe all boxes should be breakable by default?