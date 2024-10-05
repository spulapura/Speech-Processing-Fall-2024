# Acoustic Phonetics 

Low-pass vs high-pass filter applied to same speech. In the former, you hear the fricatives most of all, in the latter you get booming vowels and intonation, not as much frication. 
## Source/Filter Theory

Quality of a vowel depends on overtone structure, in other words, it contains many pitches simultaneously, called **formants**. The lowest three suffice to tell vowels apart. 

Imagining the vocal tract like a pipe, some sound goes directly out, while some echoes/gets reflected back and re-interacts with new source energy, which amplifies some frequencies and damps others. Vocal folds are a **source** of sound energy, and the vocal tract is a frequency **filter** that affects the timbre or vowel quality of the sound. 

This is similar to many musical instruments. 

$$ F_n = \frac{(2n-1) \times c}{4L}$$

Where $n$ is the number of the formant, $c$ is the speed of sound, and $L$ is the length of the vocal tract. The resonating portion of the vocal tract is a different length for different types of sounds. 

Formants also determined by shape of vocal tract. Above formula assumes uniform diameter. 
## Tube Models

Smaller bodies of air produce higher frequency sounds. Vocal tract has many different bodies of air for different overtones, like if you were tapping many bottles at the same time. We hear the sum of these waveforms together.

Not as simple as vocal tract air vibrates one way, air in other parts in another way. The vocal folds may vibrate faster or slower (changing the pitch) but the formant frequencies remain the same if the shape of the vocal tract is the same. 

All voiced sounds are distinguishable from one another by formant frequencies. For example, when doing speech synthesis, you need to put all the formants on top of each other, then you can hear clearly except for the releases of the stops, and the fricatives. 

## Perturbation Theory

We can also model the acoustics of vowels in terms of perturbations of the uniform tube. So for example, rounding the lips creates an acoustic effect on formant frequencies, which distinguish between rounded and unrounded vowels. 

There are locations in the vocal tract where constrictions cause formant frequency to rise, or elsewhere, fall. For $F_1$ through $F_3$, the resonant waves are all in the vocal tract at the same time. You can see in the diagram where the pressure and air velocity maxima are located. Perturbation theory states that if there is a constriction at a velocity maximum in a resonant wave, the frequency of the resonance will decrease, and if there is a constriction at a pressure maximum, the resonance frequency will increase. 

For example: $F_1$ frequency is higher in low vowels, since there is constriction in the glottis (pressure maximum). With $F_2$, you can increase the frequency with constriction of the glottis or by moving the tongue to the roof of the mouth (since that's also a pressure maximum), which is more common. 

## Acoustic Analysis  

**Spectrograms** show the sounds in terms of their components. Time on the horizontal axis, frequency on the vertical axis, and amplitude in the darkness. 

Can see upward/downward movement of formants, indicating diphthongization. Higher formants also visible in the diagrams, more towards individual's voice quality rather than distinguishing vowels. 

Can see in British vowels, there's less diphthongization (and also the British speaker has a lower voice so his formants are all lower).

Regularly spaced vertical lines on the spectrogram when vocal folds are vibrating (sustained for longer amount of time in a vowel). Can use these to measure pitch, which is higher when the vertical lines are farther apart. 

## Acoustics of Consonants

## Interpreting Spectrograms

## Individual Differences 

