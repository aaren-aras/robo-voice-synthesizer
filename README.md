# Robo-Voice Synthesizer 
## Power-line Interference
 - Filter: Notch (Bandstop)
 - Type: Butterworth
 - Order: 2nd 
 - Centre (fo): 60 Hz
 - Transfer Function: H(s) ≐ (s^2 + 142122.3)/(s^2 + 533.1s + 142122.3)

Since we are removing a highly specific frequency, namely the 60 Hz hum from AC power sources, without affecting the passband, a Butterworth notch filter is the ideal choice. This is owing to its ability to precisely and sharply attenuate frequency-specific noise. Additionally, a Q-factor of 60 is chosen to maintain a bandwidth of 1.0 Hz, as per the equation: Q = fo/BW.

## Background Noise
 - Filter: Bandpass 
 - Type: Butterworth 
 - Order: 2nd
 - Cut-off: fl = 0.1 Hz, fh = 450 Hz
 - Transfer Function: H(s) ≐ 45/(s^2 + 0.015s + 45)

Since we are preserving a specific range of frequencies, i.e., 0.1 Hz to 450 Hz (as specified), a bandpass filter is a solid option. A Butterworth configuration has been chosen to provide a maximally flat frequency response that ensures the passband is undisturbed.

