# This file is used to contain all the relevant notes for using Vim editor.

### Vim uses many plugins to enhance the user experience.
Learning these plugins activation and their usage can be significantly helpful in different areas of using Vim and its applications throughout the linux environment.


Command for setting line numbers in Vim
:set number 	= ":"set(space)number

Command for setting relative number
:set relativenumber	= ":"set(space)relativenumber
This enables relative number setting to identify how many lines apart in position you are from any given line. It can further help with navigation keys mentioned below and also be used for deletion, movement, coding etc.

Vim uses different keys for navigation up, down, right and left. This can help the users stay on the main keyboard instead of laying off to arrow keys during the typing process. The keys are as follows:
	* k key - up
	* j key - down 
	* h key - left
	* l key - right

Pro tip: These keys can be used with numbers to navigate quickly. For instance, *number 5+k* can take you 5 lines up, the command would be *5k*. Similarly, 4l will be moving the current position to right 4 times. Its the same as pressing *llll*. All these commands need to be used in normal mode.


**Vim settings go away every time vim is closed or the current file is closed. Upon reopening, number settings and any other configuration would need to be set again.**

To avoid having to set these settings every time, a configuration file is used. Vim uses the VIMRC file to store these settings.


Redo & Undo in Vim
	* for undo, press *u* or :u
	* for redo, press and hold ctrl+R or :redo
The same rule for numbering applies in undo and redo, for instance, using *3u* will undo 3 times, or act as *uuu*. Similarly, *5Ctrl+R* will act as *Ctrl+R Ctrl+R Ctrl+R Ctrl+R Ctrl+5*.


#### Vim Visual Mode and key bindings
To enter Visual mode, press *v* for visual.
Upon entering, keys have a different usage, some of which listed below:
	1. as soon as v enters in visual mode, navigating up, down, right or left will **select** the text as the position moves from one place to another.
	2. d = deletes the selection
		* D or uppder case D = deletes the rest of the line
		* dd = deletes the whole line
		* 5dd = deletes 5 lines
	3. y = yanking (it means copies of a press)
		* yy and Y  = copies the whole line
		* 5yy = copies 5 lines
	4. p = paste (there is no pp)
		* 3pp = pastes 3 yankings
	5. u = undo
	6. Ctrl + R = redo
	7. c = removes the selection and lets you *change it* by entering insert mode
		* cc = change the whole line and enters insert mode
	8. r = replaces the selected test
	9. w = go forward a word, W or capital W moves forward where there is a space next to what is written, it only considers space as separators.
	10. b = go back a word, uppercase B or B also considers space as the only separator.
	11. e = jumps to the end of a word
	12. I or capital I = go to the beginning of a line, and enters the Insert mode there.
	13. 0 = goes to the beginning of the line without entering insert mode unlike I.
	14. $ = goes to the end of the line.
	15. % = jumps from opening bracket to closing bracket, the position must be on the opening sign of where the user wants to jump from.
		* %d, %y, %r = all these can be used with their relative combinations.
	16. t and symbol or word = jumps one position before the symbol or word user is looking for next from its position.
		* dt, yt, rt and symbol or word = deletes, copies, replaces  everything forward one place before the symbol or word specified.
		* capital T does the same thing backwards.
	17. f and symbol or word = jumps to the position of the symbol or word user is looking for next from its position.
		* df, yf, rf and symbol or word = deletes, copies, replaces  everything forward towards the place including the symbol or word specified. 
		* capital F does the same thing backwards.
	18. gg = jumps to the beginning of the file
		* G = jumps to the end of the line
		* 12G or :12 = moves to line number 12.





	

Combinations of above mentioned key bindings:
	* dw = deletes a word **(same concept of deletion words with yanking/copying or y such as yw, y0, y$, yiw, 2yw or y2w, 2yb or y2b etc)**
	* dw in between a word = deletes the rest of the word from selection
	* d0 = deletes everything till the beginning of the line
	* d$ = deletes everything till the end of the line
	* diw = delete in a word, deletes the word regardless of its position, be it between or at the start
	* 2dw or d2w  = deletes 2 words forward | delete 2 words forward
	* 2db or d2b  = deletes 2 words back | delete 2 words backward
	* ciw = change in a word, to change the whole word your selection is on
	* ci, di, yi = *change in*, *delete in*, *yanking in*, these work in brackets (), quotation marks "", curly brackets {} etc. 

