# Process - Using Scales {#process-scales}

As discussed in \@ref(tools-midi-tools), scale quantisation is a widely used
tool to harness the random note values from MIDI Generators. It provides *just
enough* quantising to turn something unlistenable into something that's still
random, but within a context of something that's more listenable. The problem is
that even within a defined scale, there are sometimes notes that will irritate
the listener if they happen too often - for example in the C Major scale, the
note B - one semitone below or 11 semitones above the root is always going to be
a bit jarring. In the context of most Western music that note is often played in
passing on the way back to the root note C. But in the context of random note
generators it may pop up a little too often for comfort and not always resolve
to the C. So what do we do? Avoid Major scales?

------------------------------------------------------------------------

## Key idea {.unnumbered}

Finding a few useful scales that work well in a generative context is a good
idea. This is largely a matter of taste, and potentially just trial and error to
see what you like, but there are a few guiding principles that might help inform
your choice. Choosing scales or eliminating *awkward* notes from a scale can
also help make music where the tonal centre of the music isn't locked in or
***obvious***, which allows you to imply a change of key through a root note
change, without having to change the scale for the generated (or quantised)
MIDI. I'll call this being tonally ambiguous.

------------------------------------------------------------------------

## Pentatonics - Minor and Major

You know how you can play only the black keys on the keyboard and no matter what
you play it just all somehow "fits" and sounds good? That's because you are
playing a pentatonic scale. Many guitarists will scoff at players who riff away
on a pentatonic scale, because it is seen as being somehow a "cheat" and avoids
having to learn more complex scales and harmonies. But for our generative
purposes, ***pentatonic scales are your absolute number 1 pick***. You can
combine any number of generative processes working within a pentatonic scale and
they will fit together like hand in glove.

Below are the notes and scale tones of the C pentatonic scales:

C Minor pentatonic: C - Eb - F - G - Bb - C; 1 - m3 - 4 - 5 - b7\
C Major pentatonic: C - D - E - G - A - C; 1 - 2 - 3 - 5 - 6

If you pick any 3 out of either of these scales then you get nice triads from
their respective (non-pentatonic) scales.

## Modes

Modal scales are ***hard*** to wrap your brain around at first. In practice,
they are very easy. Take the notes in the scale of C, start on different note
and end on the note one octave above that.

### Mixolydian mode

Start on the G of the C major scale and play only the "white keys" of the C
major scale up to the next G. That's the Mixolydian mode. Let's look at the
notes and scale tones and try to understand what's going on though:

G Mixolydian: G - A - B - C - D - E - F; 1 - 2 - 3 - 4 - 5 - 6 - b7\
C Mixolydian: C - D - E - F - G - A - Bb.

Mixolydian is essentially a major scale but with a flattened 7th. This is a
nicer alternative to the straight major scale because the harsh major 7th is
"softened" by flattening it. You can combine this flattened 7th with other notes
in the scale and get attractive chords. You can also swap between the Mixolydian
mode and the fourth of the natural major key. So C Mixolydian has the same notes
as F Major. G Mixolydian has the same notes as C Major. If your MIDI note
generator process pings out the flattened seventh here, it won't sound harsh and
abrasive. And you could either play a root drone of the Mixolydian mode root, or
the fourth of the natural key and both would sound fine.

### Dorian mode

D Dorian: D - E - F - G - A - B - C - D; 1 - 2 - m3 - 4 - 5 - 6 - b7\
C Dorian: C - D - Eb - F - G - A - Bb - C

Dorian is a more "minor" sounding mode (with a minor third from the natural
scale) and also the flattened 7th we talked about above. Dorian is essentially
the "minor" version of what we discussed above with the Mixolydian, and it works
for many of the same reasons.

## There are no "wrong" notes, only context

To paraphrase an old saying "Play a note once and it might be wrong. Play it
twice and it's jazz...". There is certainly a truth that there are truly no
"wrong notes" - whatever note you play you can add additional notes around or
resolve it to a point that it will work within the context. When you compose or
play with others, you can work on the context or resolve these problematic notes
towards something more comfortable. This tension and release is a great feature
of many tunes. But within generative music, we can't guarantee that the
processes we have set up will provide that context or resolve the notes towards
something more pleasant.

If you are using generative processes to create something to play along with -
where ***you*** can provide the context and resolution, then go ahead and try
out other scales. In fact, this might be a really good musical challenge... But
this is a little beyond the scope of this book. And my skill set.

## Selections of notes - chords

In \@ref(recipe-changing-chords) and \@ref(process-note-wise-probability) I
talked about stacking notes in a chord and then applying probability. I
mentioned that you might want to choose notes that would work well together, so
that regardless of which notes were chosen you would get something that didn't
sound too "weird". Now given the context of the scales above, I hope it will
help point you towards scale tones that would work over a selection of root
notes, or where a random selection of 3 or 4 (or 5 or 6!) of the notes would
produce something that would still be a "nice chord". Also contextualising this
collection of notes (chord!) with a given root note or bass note for the chord
would imply one key / mode or another.

## Other scales & traditions

In Western music we have a view of what collections of notes and pitches sound
"nice" and "harmonious". Of course, there is a huge world of scales in the world
across a huge range of musical traditions. In this chapter I've only focussed on
typical scales from this Western Tradition. With Ableton's Scale plugins and
scale awareness you might well find others where generative methods would give
interesting results. Within the DAW, experimenting with these scales is only a
click away...
