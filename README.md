# no-canvas-targetting
An attempt at making tokens selectable and targetable in no-canvas mode, in Foundry VTT

Broad plan:

Targets are stored in game.user.targets
Controlled tokens are stored in canvas.tokens.controlled

Both of these take the Token object, i.e. the canvas object not the document.

Need to make a spoofed Token object, which contains only the data/functions relevant to targeting and control operations
Also need to spoof canvas.tokens.controlled, since it won't exist

Also will need to fix various other bits in the token targeting workflow which might rely on the canvas, e.g. user.updateTokenTargets

And need to be able to clear targets/control when switching scenes

And may need to fire appropriate hooks

And then need to test with MidiQoL in 5e, in PF2, and in Lancer once that comes out

Plus going to need some way to handle template placement, which... no idea how that'll work

UI: Grid of tokens, buttons to target/control those tokens (possible toggle for multi/single select)
