
## Time Domain 

1. Sound is a pressure wave traveling through air
2. 340 mps speed of sound
3. Pick a single point in space, measure the pressure at that point over time
	1. Amplitude of pressure variation vs time
	2. Microphone isn't calibrated scientific instrument, but rather variation of pressure, so no units of amplitude-- transformed into analog electrical signal
		1. For analysis in computer, need digital signal
4. Enlarge the scale of a spoken sound wave-- amplitude in repeating pattern, vs no clear pattern
5. Need short term analysis of sound over shorter period of time
6. Sound source/speech production
## Sound Source

1. Basic sound source and a way to modify it
2. Tube from lungs to lips
	1. Airflow from lungs, pressure builds up beneath the vocal folds
	2. Eventually enough pressure to burst open the vocal folds
	3. High pressure air from below moves up, releases the pressure below them, so they close again
	4. Higher pressure air exerts force on neighboring low pressure air, moves up at speed of sound
	5. Airflow in general is much slower than the pressure wave
	6. Sound is variation in pressure in air

## Digital Signal

1. Capture signal in time domain and convert to digital signal
	1. Mic gives analog voltage
2. Analog-- smooth and continuous, infinite precision
3. Digital-- fixed number of values it can take, finite precision-- discrete
	1. Computers can only store binary, in finite storage
4. 2 things to consider
	1. Represent amplitude with fixed precision in binary
	2. Store the amplitude finite number of times per second (finite storage)
5. Making time digital-- sampling
	1. Can join the fixed points for visuals, but really it's just points as samples
	2. To store a frequency, you need 2 samples per waveform
		1. Highest frequency you can capture is half the sampling frequency
		2. **Nyquist Frequency** (half the sampling frequency)
			1. Lose high frequencies when you sample at a low rate (ie start losing fricatives)
		3. **Aliasing** when you don't sample frequently enough so you start losing the actual shape of the wave
	3. **Quantization** = making amplitude digital
		1. How many bits per sample
		2. Use nearest available discrete amplitude value
		3. Usually 16 bits per sample (bit depth)
			1. So $2^{16}$ possible values
		4. Noise = error between quantized and actual signal. Reducing the bit depth adds noise to the signal. 

## Short Term Analysis

1. First step to move from the time domain into another domain
2. Other than the duration of the utterance, you want to be using a much smaller time window (on the phon level)
3. Need to use a general purpose method agnostic to linguistic info. Instead, use a fixed duration frame. We don't know linguistic info at this point. 
	1. Choose a window function-- rectangular window called a frame
	2. Then perform analysis on that frame
	3. Then move to the next frame by sliding the window down
	4. We get artifacts at the beginning and end of the window, so instead we use a taper so we don't have the abrupt changes at beginning and end
	5. frame duration and frame shift (need to overlap the analysis frames)-- sequence of frames

## Series Expansion

1. Speech changes over time, so we need to analyze in the short term
2. Series expansion as an abstract concept has many different applications, including Fourier analysis
	1. Expand a complex signal into the sum of simple waves, or basis functions
	2. Can make any complex waves as sum of sine
	3. For a digital signal, we have a finite amount of information, so we need a finite amount of basis functions
	4. Need every frequency up to the Nyquist frequency
	5. Need a certain set of coefficients multiplied by the basis functions to reconstruct the original signal
3. Removing noise-- stop adding terms if some of the higher frequencies are noise/irrelevant

## Fourier Analysis

1. Use series expansion to take digital signal in time domain into frequency domain
	1. Complex wave = weighted sum of basis sine waves
	2. Start with the lowest frequency possible in the window (ie one cycle) up to the Nyquist frequency, which is half the sampling frequency
2. Fourier Analysis is finding the coefficients of each basis function
	1. frequency in kHz vs magnitude
	2. Correlation-- go along the time domain and for each sample, multiply the value of the basis function by the value of the original function. If this is high, they have high correlation
		1. And put that on the new graph at the frequency (on the x axis) corresponding to the basis function
		2. Continue the process for all basis functions
		3. The result tells you how much signal you have at that frequency-- spectrum
3. True sine waves are orthogonal. Their correlation is 0. No energy at one sine function's frequency in another sine wave's frequency
	1. So therefore, there's a unique solution for the coefficient
	2. And is invertible, losing no information-- you can just add up the basis functions to get back to the time domain

## Frequency Domain

1. Need not just the magnitude of the basis function, but also the phase
2. Like for example, if you have a cosine wave... you can't get it from sine with no horizontal shift since cos(0) is 1.
	1. Need to slide the basis functions left and right
	2. Hearing is not sensitive to phase-- the waves look different but they sound the same to us
3. Spectra-- plot the coefficients + magnitude
	1. The magnitude spectrum doesn't consider phase
	2. Vertical axis is usually on a log scale, using units of dB
		1. Relative amount of energy at each frequency
		2. Spaced equally for each frequency up to the Nyquist
4. What happens with a longer analysis window
	1. So we get a lower initial frequency, and they're more closely spaced together, so more basis functions between the initial frequency and the Nyquist
	2. Get more detail in the magnitude spectrum with a larger window
	3. But there's a tradeoff-- now we're generalizing/losing specificity in the time domain (we initially chose to use windows since we wanted to analyze specific sub-parts of the signal to split it up phonetically)