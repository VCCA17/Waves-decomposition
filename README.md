# Waves-decomposition
A project, with potential to become an academic paper, aimed to decompose a wave signal using any type of wave as a basis.

The great algorithm to decompose wave signals into complex exponentials (Fourier Transform) is the undisputed FFT, and this approach does not intend to take its crown.

When you are in a lab and have a wave signal, you may want to express it in different types of waves according to some alternative theoretical model.
For example, waves that propagate in a round 2d surface, like a drum, are described by Bessel functions.
In order to decompose the waves in many Bessel functions modes (a Fourier-Bessel series) one should use a discrete Henkel Transform, which is also ok with modern software.
However, what if the modelling sugests many types of waves (functions) to be possible? How to easily change from one to the other? What if the waves are interactive (non-linear)?

This is what this is about.

By training an ANN to many known functions (waves), we train the network to recognize and decompose the signal as the given main wave modes.

In the code I start by recreating a Fourier-Transform, then I only use the FFT to compare the results (in contrast with @endolith 's approach).
Then the code is extended to sine/cosine waves and then to Bessel functions.

Since the Fourier, Sine , Cosine  and Hankel Transform are linear, no activation function shall be used; the ANN will find out by itself the parameters for this supervised learning process.

The next step is to go to non-linear waves decomposition.
