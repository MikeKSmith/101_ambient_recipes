# Tools - Live 12 Overview: MIDI and compositional tools {#tools-live12-overview}

During the process of writing this book, Ableton released Live 12. With Live 12
there are a whole host of improvements and additions which make the life of
someone making generative music a whole lot easier. In this chapter we'll look
at the new compositional and MIDI tools. In the next chapter we'll look at new
sequencer tools. In subsequent chapters we'll look at some specific Transformer
and Generator tools.

------------------------------------------------------------------------

## Key idea {.unnumbered}

Live 12 contains a number of tools and new features which enhance how we can
make generative music using Ableton Live. Some of these are enhancements to
existing functionality, but there are many places where there are brand new
features which could be used to create generative music, or provide idea
generators for composition.

------------------------------------------------------------------------



## Scale awareness

Live 12 now has a feature where the scale can be defined at the Set level, which
then sets the scale for each new clip (or can change the scale of existing
clips); but you can also ***set*** the current scale for the set from clips.
This allows you to change the scale of the set for example during live
performance when the each song might be in a different key.

<img src="images/Live12_Scale.png" width="100%" />

But scale awareness goes beyond setting the scale for MIDI notes within a clip -
many devices now have a "scale awareness" so that when the device adds or shifts
notes, it does so within the context of the scale. In the screenshot above you
can see that the purple "Scale Mode" button is ON (b# button). This means that
clips and devices will use the scale shown as the default. Note that this
***isn't*** a Global Scale which overrides scale settings in clips, but rather
an indication of the ***CURRENT*** scale being used. See
<https://help.ableton.com/hc/en-us/articles/11425083250972-Keys-and-Scales-in-Live-12-FAQ>

In the "Random" MIDI device below, again the purple "Scale Mode" or Scale
Awareness button is lit, meaning that random pitch shift will be in the context
of the Current Scale setting, so shifting up or down scale degrees, rather than
semitones. This is a boon for the Lazy Producer because now they won't need to
add MIDI Scale quantizing devices, and also changing the scale in the Current
Scale (or through clips), the MIDI devices and instruments will automatically
pick up whatever the new Current Scale is.

<img src="images/Live12_Random_ScaleAware.png" width="100%" />

So now we can chain together MIDI Devices as discussed in
\@ref(tools-midi-tools) and used in \@ref(recipe-midi-generators) and by turning
on Scale Awareness we'll pick up whatever the Current Scale setting is. Note in
the Chord and Arpeggiator devices that instead of "st" semitones for shifting,
it is now labelled "sd" scale degrees. This takes a little getting used to
because the scale degrees are added onto the MIDI note value - so +4sd is a
fifth above the incoming MIDI note.

<img src="images/Live12_ScaleAware_MIDI_Devices.png" width="100%" />

Scale awareness also extends to some of the Synth instruments in Live 12 - Meld
in particular has scale awareness for some of its tone generators, where
changing the macro knob for that generator adds harmonic content that is in tune
with the Global Scale.

Note that MIDI clips set Current Scale, so if you wish to change the Current
Scale, it's worth checking that ***ALL*** MIDI clips within a scene or all MIDI
clips playing have the same scale setting. See
<https://help.ableton.com/hc/en-us/articles/11425083250972-Keys-and-Scales-in-Live-12-FAQ>

## Compositional tools

### MIDI Generation

Live 12 now comes with two new features built into MIDI clip creation: MIDI
Generation and MIDI Transformation. MIDI Generation does what the name suggests
- provides a range of different methods for generating new MIDI parts: rhythm -
which creates sequences of MIDI notes by specifying the density of notes within
a certain number of steps and then allowing you to choose permutations of these,
stacks - which defines chords, seeds - which generates one or more "voices" of
completely random notes (but these could conform to the clip scale setting)
within the clip, shape - which generates notes by drawing in a pattern or shape,
and Euclidean generators. And because what sits behind these generators is the
power of Max for Live, the possibilities open up for a huge range of innovative
MIDI generation.

<img src="images/Live12_MIDIGenerators.png" width="100%" />

<img src="images/Live12_Max_MIDIGenerator.png" width="100%" />

In Chapter 13 we looked at MIDI Generator devices including Max for Live
devices. But having some similar functionality here "baked into" the Live MIDI
clip tools puts these tools at the fingertips of anyone with Live 12 Suite.

<img src="images/Live12_Euclidean_Pattern.png" width="100%" />

### MIDI Transformation

The MIDI Transformation tools includes tools to arpeggiate the notes within the
clip, connect - connecting existing notes in the clip with passing tones,
ornament - adding additional short notes before the main note, like a flam in
drum terms, or mordent in classical notation, quantize - here applying
quantisation non-destructively, i.e. you can see the effect of the amount of
quantisation on the MIDI notes, recombine - which lets you select notes and then
permute these (rotate the order, mirror, shuffle), span - which allows you to
change the note lengths by various means, strum - which applies a rhythmic strum
pattern to chords, and time warp - which can bend the timing within a bar, so
although the bpm clock remains constant, MIDI notes in a clip can trigger with a
more fluid timing.

<img src="images/Live12_MIDI_Transformers.png" width="100%" />

## Note probability

In \@ref(process-note-wise-probability), we looked at Notewise probability -
where we can set the probability for each note in a sequence, so we can generate
ever changing patterns even from fairly short sequences of MIDI notes. Live 12
has another fantastic feature where we can ***group*** notes together and either
select to play ***all*** notes in the group and adjust the probability of that
group of notes, or group notes and select to play ***only one*** of the notes in
that group. What this means for the Lazy Producer is that you can specify chords
that when triggered play all of the notes (probability acts on the ***chord***)
or you can nominate a group of notes where the computer picks which note in the
group will play, but you can be sure that exactly one of those notes ***will***
be played.

<img src="images/Live12_GroupNotes.png" width="100%" />

Let's give a concrete example. Imagine you want to set up an arpeggiated
pattern, but you always want the pattern to play four notes. You always want the
root note of chord and the fifth of the scale to play, but you want the other
two notes in the pattern to vary each time the chord is played. Well you would
group the root and fifth and select "Play All", while you could group the other
notes in the chord and select "Play One". This will maintain a steady pattern
and predictable notes (root and fifth of the scale) while other notes provide
some randomness and interest. Note that these actions on the grouped notes (Play
One, Play All) also follow whatever is set for the probability setting for those
notes / groups. So you can have a group of notes with "Play One" but that one
note will only happen 50% of the time. This opens up enormous flexibility in
generating note patterns or sequences with a LOT of variation.
