# jspsych-vislexdec-vp-mask
Visual Lexical Decision with masked prime

# Task Description
This is one of many 'standard' variations of a visual lexical decision task. The 'parent' of this boilerplate/template is the general visual [Lexical Decision With Visual Prime](https://github.com/UiL-OTS-labs/jspsych-vislexdec-vp/). You may want to visit there first and come back here, especially if if you need general info about how to use and set up these kinds of boilerplates.

In its current state, the additional sub trial phases are:

- A _pre prime mask phase_ (with '#####')
- A _post prime mask phase_ (with '&&&&&')

The general Lexical Decision with Visual Prime trial structure is: 

1. Fixation cross (fixed duration, no user input)
2. Prime presentation (fixed duration, no user input)
3. Response item presentation and repsonse interval (last word/non-word, user keypress interval)

This version can be used to do

1. Fixation cross (fixed duration, no user input)
2. __Pre prime mask presentation__ (fixed duration, no user input)
3. Prime presentation (fixed duration, no user input)
4. __Post prime mask presentation__ (fixed duration, no user input)
5. Response item presentation and repsonse window (last word/non-word, user keypress interval)

## Globals for (sub) trial phases
Settings can be specified for durations. You can find them in ```globals.js``` 

## Stimuli
The easiest and most customisable way to implement masks, is to define them as timeline variables in ```stimuli.js``` for each stimulus/trial specification. A _function_ to do approximately the same is not difficult to add, but this verbose way of defining it in the stimulus.js file leaves it up to the creativity of the user to think up additional categories and or fucntionalities of mask function and behavior. In this boilerplate, we've defined to use a monospaced font, so
that the layouting of masks and prime will be consistent, _if_ the user takes into account to use _equal lengt as the prime_ for each masking string. 

## Things that differ from the parent boilerplate
- In ```index.html```
    - New sub trial phases:
		- present_pre_prime_mask
		- present_post_prime_mask	
	- Additions of the new sub trial phases' in the timeline procedures: 
		- practice_procedure
		- trial_procedure
	- Some new styling elements 
		- Monospace stimulus
		- Better margins and layouting for instructions
- Instructions in ```instructions.js``` have changed a bit
- Stimuli in ```stimuli.js``` have new key-values for post and pre prime phases
- New globals in ```globals.js```

## Todo
- Check/ask for instruction content and defaults.
- Discuss function version pro/cons: different repos?
- Make docs for how and where to edit boilerplate?



