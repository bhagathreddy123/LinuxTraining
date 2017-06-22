simple commands shortcuts for shell

time command
 how long it takes to run the program

$ time

$ time ls /etc/

real	0m0.008s
user	0m0.004s
sys	0m0.004s
$ time

real	0m0.000s
user	0m0.000s
sys	0m0.000s






$ time ls
$ time pwd

pwd

CTRL X Backspace

if you put cursor in btw 2 words if we use above command the word infront of cursor will remove.

CTRL R

for fast searching of commands
Vi commands and usage:


vi myfile

it will create new file

type i that is in insert mode

we hit esc that is in command mode
Yank is used for yy letters.

Yy  is used for copying(yanking)

p(small letter ) is used for paste after the cursor
P is used for paste before the cursor


o  is used for create new line.

If we want to delete 10 lines we need to use 10dd


4yy
p

dd command delete a line

shift A it is used for cursor display  end of the line

lower case a is used for type  the letters next char after cursor

enter R

type 20dd

dd
A
shift H         starting the line top

shift L       ending the line bottom

u              undo changes

dd         delete line
cc          changing entire line of the code

cw            changing one word



Search


type  /

N for next
Shift n                      up
n                           down

Save changes         using w
:wq
:!ls
:e filename   ---------> load the file

:q!    --------------> without saving changes
