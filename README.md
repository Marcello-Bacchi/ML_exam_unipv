# Objective

The objective of this project is to train a machine to distinguish between two classes of resonance: Lorentz resonance and Fano resonance.
Resonaces are detected when broad spectrum light is guided towards a resonator: if the wavelength (energy) of light corresponds to one of the own resoances of 
the resonator, then light is trapped and the trasmittance of the system decreases.
Resonance's shape depends on many factors and its study provides a huge number of information about the physical processes happening.


Here we are interested in the ability to separate the two kind of resonances that I can encunter in my research field (quantum photonics). 
The appearance of a Lorentz or Fano resonance depends on the coupling condition between the media where light is propagating and the resonator:
the more the coupling between the continuos of the modes in the travelling media and the discrete modes of the resonator, the more Fano-like resonance will be seen in a trasmittance spectrum.
Lorentz resonace is the limit in no-coupling condition: this is not a physical case, but it is still a very good approximation in weak-coupling condition.

It is very useful to be able to distinguish between the two classes of resonance since they correspond to different coupling condition and different coupling lead to 
different behaviour of light that interacts with the resonator.

# Issues encountered 

I used the approach of supervised learning, since it allows me to label the resonances correctely. 
The amount of data required made it impossible for me to exploit real experimental data from trasmittance spectrum of samples measured in our laboratory:
in fact, coupling condition can change even between two nearby resonances (separated by roughly 1nm) of the same sample. 
As a consequence, I should check thousands of resonances and label them one by one, since I am not able to know apriori light coupling conditions for each wavelength.

In order to overcome this problem, I simulate in Python 3000 resonances, random varying thier parameters (resonance positions, amplitude, full width half maximum, 
out-of-resonance trasmittance, coupling coefficent) and adding a random noise to each point of the spectrum. The simulation code is uploaded in this repository.

# Colab notebook

The notebook contains four images of resonance spectrum as examples of the output of the simulation: Lorentz shape, symmetric Fano shape (weak-coupling condition) 
and two asymmetric Fano shape.
I used the MLP and CNN 1D models: results are given separately and then compared for optimized input parameters of the models.
























