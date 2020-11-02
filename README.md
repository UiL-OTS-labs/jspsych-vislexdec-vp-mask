# jspsych-vislexdec-vp-mask
Visual Lexical Decision with masked prime

# Task Description
This is one of many 'standard' variations of a visual lexical decision task. The 'parent' of this boilerplate/template is the general visual [Lexical Decision with prime](https://github.com/UiL-OTS-labs/jspsych-vislexdec-vp/). You may want to visit there and then come back here if you need general info about how to use and set up these kinds of boilerplates.

In its current state, the additional sub trial phases are:

- A *pre prime mask phase (with '#####')
- A post prime make phase (with '&&&&&')

The general Lexical Decision with Visual Prime trial structure is: 

1. Fixation cross (fixed duration, no user input)
2. Prime presentation (fixed duration, no user input)
3. Response item presentation and repsonse window (last word/non-word, user keypress interval)

This version can be used to do

1. Fixation cross (fixed duration, no user input)
2. __Pre prime mask presentation__ (fixed duration, no user input)
3. Prime presentation (fixed duration, no user input)
4. __Post prime mask presentation__ (fixed duration, no user input)
5. Response item presentation and repsonse window (last word/non-word, user keypress interval)

## Globals for (sub) trial phases
Settings can be specified for durarions. You find them in ```globals.js``` 

## Stimuli
The easiest and most customisable way to implement masks, is to define them as timeline variables in ```stimuli.js```. A function to do the same is not difficult to add, but this verbose way of defining it in the stimulus.js file leaves it up to the creativity of the user to think up additional categories of masks, etc. In this boilerplate, we've defined to use a monospaced font, so
that the layouting of masks and prime will be consistent, _if_ the user takes into account to use _equal lengt as the prime_ for each mask. 

## Things that differ from the parent boilerplate
- New globals in ```globals.js```
- In ```index.html```
    - New sub trial phases:
		- present_pre_mask
		- present_post_mask
    - Deleted 'data' key-value pairs from all but the 'response phase' test item presentation variables.
	- Additions of those phases in the timeline procedures: 
		- practice_procedure
		- trial_procedure
	- Some new styling elements 
		- Monospace stimulus
		- Better margins and layouting for instructions
- Instructions in ```instrcutions.js``` have changed a bit
- Stimuli in ```stimuli.js``` have new key-values for post and pre prime phases

## Todo
- Check/ask for instruction content
- Discuss function version pro/cons: different repos?
- Make docs for how and where to edit boilerplate



