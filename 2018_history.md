# 2018 Ideas - history (of them)

... about some things that could be changed in this repository.

Sub-headings of ideas have `vN,#M` at the start:  
 \- "N" is version number of the code that the section is about  
 \- "M" is number of the section in its group of ones that have its "N".  
The following version numbers have section(s) that  
are a part of a milestone, next to that number:  
 \- v1.0, [milestone 1](https://github.com/user-e/Melody-motion-search-code/milestone/1)


## v1.0,#1 The original "interesting idea I thought up"
 \- to add as a personal project on GitHub (a few HTML/markdown files), with these options,  
a similar structure and formatting as below, monospace font for text-based diagrams:

I've thought up a music melody search pattern/format idea, based on Parsons Code  
but including how wide each gap between notes is estimated to be and using positions  
relative to the first note (with a symbol to change this when a new phrase starts).

This new notation detail should make search results for a piece more accurate. A similar  
method to mine is the "Numeric scale" used by some choirs but it uses key scale notes.
```
    *                        0.2)             *
  /   \                      0.1)          *
*      *     * - * - *        0 )== * = * =/\=/\=  [...]
        \   /               -0.1)
          *                 -0.2)
*uddurr                    daah daah do   de    di    da   duh    doo duh deh de duh di
                            @0,  0,  0.1, 0.2, 0.3, -0.1, -0.3,  -0.56@0 , ...
```
Parsons Code for melodic contours: start at unknown note ("*"), each note following  
has a higher/lower/the same (repeated) pitch which is represented as "u" / "d" / "r"  
to show the relationship of its pitch to the previous note.  
This simple notation system, used to identify a piece of music by melodic motion (pitch movements),  
was developed by Denys Parsons in 1975 for his book "The Directory of Tunes and Musical Themes".

Relative Melodic Motion Code (experimental idea): the code contains sections marking phrases  
of music where notes are near to a starting pitch. Each section starts with an unknown position setting  
note (@0) then is followed by a series of relative note values (positive or negative decimals separated  
by commas) and ends with a special relative note value joined to the position note of the next section.

### Relative note values:
Represents a note in the melody section as a pitch change gap between it and the  
starting (position setting) note (of that section). If it is higher pitch, the decimal is  
positive or else it is negative unless it repeats the starting note, making it zero.

All values have an upper and lower limit of the chosen number range, and must change  
in regular steps (of a chosen size fitting the scale set by the number range) so they can be  
compared to real musical intervals. The search service could allow a small error difference  
for each value (e.g. 0.005) if possible to check but users need to be accurate.

### Special relative note value:
A relative note value that ends a section and sets the pitch value of the position setting note  
starting the next section, relative to the pitch of the position setting value in the current section.  
It is joined to this next starting note without a comma separating them.


## v1.0,#2 New scale for gaps between notes
Before this idea, I wrote a note that the code  
needed a new fixed scale for gaps between notes:

![dsc_0023b_kindlephoto-66970552 - image of the note](https://user-images.githubusercontent.com/13541254/39725643-73f22cba-5244-11e8-9d66-773bc954dd04.jpg)  

Then I thought of a "new way" to do that: small, medium or large gaps up/down.  
These sizes aren't fixed, relative to each other, more info in this notes photo:

![dsc_0024](https://user-images.githubusercontent.com/13541254/48857274-6176c200-edb0-11e8-8e23-145a35c4e57a.JPG)

\* in readme file, link to this issue as something like "for version 1 ideas/history, go to this page"  
\* a markdown file linked to from the readme with details of each part of the code - example  
at the top showing the structure then sections with headings for a description of each part.
