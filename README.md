# simple-dialogue-construct
a simple dialogue system for construct 3 projects


# how to set up this simple dialogue system.

tasics:
- the DialogueManager object should be a global object in your project, make sure it is spawned only once on project start
- use flowcharts to organize different sets of dialogue. probably based on a single speaker or level or similar.
- the first node of a flowchart's tag should be the name of the dialogue sequence
- middle nodes are always tagged "mid"
- ending node is always tagged "end" -- you should leave the ouptut value empty but it shouldn't matter.

To create a speaker:
- create a new dialoguecomponent
- make sure it has an overlap as a child in the hierarchy
- attach the dialoguecomponent and overlap to the parent object as children
- set the dialoguecomponent flowchart name to the flowchart you want this node to access
- set the currScene variable to the start tag of the flow you want to reference
- language doesn't do anything right now


setting up your layout:
- add your dialoguebox and dialoguetext to a scene with parallax set to 0x0% and place them where you want (ideally this is a global layer you can add to as many layouts as you want)
- on layouts where you will have dialogue, on layout start create your dialogueselector and mask as a hierarchy and put them on one of your main layers. they will automatically hide, unhide, and move themselves around
