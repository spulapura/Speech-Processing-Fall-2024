Time Domain
1. sound travels through medium-- air
2. high pressure air propagates through the medium
3. horizontal axis is time, vertical axis is amplitude of pressure variation 
	1. no units on the vertical axis? change in pressure around the microphone
	2. Plot is called a waveform
	3. Amplitude decays over time 
	4. Look at waveform to get duration of the wave, notice some repeating patterns vs some random waves 
4. Analog signals can't be stored on the computer, so we need to make them into a digital signal
5. Need to look at original source of sound, and individual parts of signal over short period of time

Sound Source
1. How is speech made? need basic sound source, and some way to modify it
	1. ie distinguish two different vowel sounds
2. Think of the vocal tract as a tube (chewb)
	1. can block the flow of air through the tube with vocal folds, which increases the pressure (tightly packed molecules in smaller space)
	2. Get pulse of higher pressure air bursting through the vocal folds, surrounded by lower pressure air everywhere else
	3. So then higher pressure air moves up at speed of sound (breathing normally does not move that fast)
	4. Increasing pressure as the pulse escapes, then decreasing as it moves away, then back to ambient pressure
	5. Glottis-- space between the vocal folds
3. Actual signal will be repeating sequence of pulses
	1. Speech perception **pulse train**-- now we no longer hear individual clicks but rather a continuous flow
4. What if we constrict the vocal folds to a narrow gap, creating chaotic and turbulent pressure airflow
	1. So the signal has no repeating pattern but rather a random "noise" signal (fricatives)
5. The two above ways of making sounds are called voicing and frication

Periodic Signal
1. Whenever there is a periodic signal, it comes from voicing, which comes with a corresponding pitch
2. Periodic signal from vibration of vocal folds
	1. Predictable/deterministic (vs aperiodic/stochastic)
	2. $T_0$ is the period or length of the cycle 
	3. $F_0$ fundamental frequency, number of periods per second $\frac{1}{T_0}$ 
		1. Unit of Hz-- cycles per second
3. We need to move out of the time domain into the frequency domain, harmonics

Pitch
1. Part of set of acoustic properties that speakers use, called prosody
	1. Fundamental frequency, duration, and amplitude, sometimes voice quality
2. Pitch is a perceptual phenomenon, which is related to the physical signal property of frequency
3. Relationship between $F_0$ and pitch is not linear-- need to double the frequency to go up an octave. It's logarithmic.
4. Praat can make an estimate of $F_0$ based on the speech signal, which it calls the pitch (but they aren't technically the same thing, pitch is perceptual, but they are related)

Formants
1. In instruments or speaking, $F_0$ is filtered through numerous parts of the resonating body
	1. Resulting harmonics are multiples of $F_0$, these are called formants $F_1$, $F_2$ etc
	2. Several resonance chambers within the vocal tract
		1. Oral cavity and pharynx create $F_1$ and $F_2$ 
	3. Resonance chambers change depending on what speech sound it is, for example ee vs aa use different resonance chambers and therefore different values for $F_1$ and $F_2$ 

Spectrograms
1. Visual representations of spoken words
2. Vertical axis is frequency, horizontal axis is time in ms
	1. Third dimension from shading, which represents the amplitude or loudness
3.  5 different formants for voice phonemes, but usually the first two are sufficient to identify speech sounds
4. $F_0$ corresponds to height, $F_1$ with frontness 
5. Darkness across wide section of the spectrogram indicates fricative or affricate

Reading a Spectrogram: Vowels
1. Have fully developed formant pattern, can be classified based on first two formants
2. Approximately associated with size of two cavities-- $F_1$ with pharynx, and $F_2$ with oral cavity
3. /i/ front constriction, large pharyngeal cavity, small oral cavity, /aa/ with back constriction, with small pharyngeal and large oral cavity
4. /i/ has a low $F_1$ and high $F_2$, while /aa/ is the other way around
5. Cardinal vowel chart is similar to the acoustic vowel chart, but not all the same because the former is just based on the tongue, acoustic on many different cavities
6. Diphthong-- you can see the formants moving farther apart 

Reading a Spectrogram: Consonants
1. Classified by voicing and place and manner of articulation 
2. In acoustics, we do frequency patterns, portions of silence, no formant pattern
3. Absence of vocal fold vibration so no fundamental frequency in voiceless consonants
	1. Voiced consonants have fundamental frequency $F_0$ 
4. All plosives have significant silence and a burst of friction noise when aspirated
5. All fricatives have clearly marked portion of friction noise, can be kept apart by frequency
6. Trills-- regular patterns of vibration, small closure inbetween
7. Nasals and Approximants have some formants but not as clear as vowels
8. Influence their environment-- steady formant pattern of two vowels, but adding consonant in between alters shape of resonance chambers **formant transition** 

