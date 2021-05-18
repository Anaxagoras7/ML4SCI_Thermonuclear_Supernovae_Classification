## ML4SCI (GSoC'21 Evaluation Task) : Thermonuclear Supernova Classification via their Nuclear Signatures
Thermonuclear supernovae (Type-Ia or SNeIa) are deeply connected to topics throughout astrophysics and cosmology. They are, however, an enigma. What are they? Why do they explode? How diverse is their population? The answers to these fundamental questions will have far-reaching impact. These beacons of the Cosmos are governed by nuclear physics processes, and the emergent nuclear radiation produced by these cataclysmic events encodes details of their structure and dynamics. Future population studies enabled by next-generation space-based astrophysics investigations will seek to identify progenitor sub-classes based on the fundamental nuclear emissions. Ultimately, nuclear physics-based observations and analyses will deepen our understanding of the role these objects play in the Galaxy and beyond. Classification based on a machine learning approach — or similar — is appropriate, in part because the connections between nuclear physics observables and intrinsic parameters (e.g. progenitor type, mass, explosion dynamics, and distribution of radioactive material) can be complex. An extensive library of detailed supernova simulations facilitates the establishment of classification metrics in preparation for future nuclear astrophysics investigations.

#### Step 1: Observable Parameters
The supernova classification project requires the use of an existing supernova
simulations database. This database is a systematic exploration of fundamental
parameters that characterize SNeIa events, such as their total mass, composition,
explosion dynamics, and the distribution of radioactive material. The temporal evolution
of the nuclear emission from each supernova model in this database can be
summarized by three observable (3) parameters:
τ: the initial optical depth, or optical thickness. This parameter characterizes the
attenuation of emitted radiation as it traverses material. In this case, the initial
optical depth corresponds to the optical depth near the start of the supernova
explosion and the ejection of material.
ν Max : the maximum expansion velocity of the ejecta. This parameter characterizes
the maximum velocity with which the outermost radius of the supernova ejecta.
Φ 300 : the emergent flux of gamma-rays at 300 days post-explosion, in the energy
band 2 to 4 MeV (MeV = 10 6 electronvolts) and at a supernova distance of 20
Mpc (Mpc = 10 6 parsecs).As an initial task, we’d like you to demonstrate that you can write a Python code, using
Jupyter Notebook, that retrieves and plots the relationships between these three
observable parameters. The parameters from 512 simulated supernovae, and their
uncertainties, are located in GSOC_Data_DataCube.txt file (hereafter referred to as the
data cube) that was sent with this evaluation. The file is in a csv format with the columns
corresponding to the following:
Observable Parameters
• Column 1: τ (dimensionless)
• Column 2: Uncertainty in τ
• Column 3: ν Max , (s -1 )
• Column 4: Uncertainty in ν Max
• Column 5: Φ 300 , emergent SNeIa flux (photons cm -2 s -1 )
Physical Parameters
• Column 6: Total mass (units=solar mass)
• Column 7: Mass of 56 Ni (units=solar mass)
• Column 8: Explosion energy (units=10 51 ergs)
• Column 9: Initial SNeIa mass distribution flag

#### Step 2: Physical Parameters
The data cube file also contains information regarding the inputs to the simulations, i.e.
physical parameters such as total mass, nickel mass, kinetic energy, composition, and
initial distribution of radioactive material.
• Using the data cube can you identify connections between the observable and
physical parameters?
• What trends can you identify among the observable and physical parameters?
• Are there any groups you can distinguish? If so, what are their unique qualities?

#### Step 3: Classification
Write a routine that applies machine learning techniques of your choice to the
classification of supernova based on data cube. This routine needs to predict all
physical parameters based on a set of observable values. The specific approach is left
to you, so feel free to impress us! Please make sure you address why the approach you
chose is appropriate for this problem and how you validated your machine learning
models. Make sure that all your work is clearly shown in Jupyter Notebook.Using your routine, predict the physical parameters of the following three test cases:
1. Test Case 1:
o τ = 3.35
o ν Max = 0.015
o Φ 300 = 1.20×10 -5
2. Test Case 2:
o τ = 2.54
o ν Max = 0.013
o Φ 300 = 5.02×10 -6
3. Test Case 3:
o τ = 2.46
o ν Max = 0.013
o Φ 300 = 1.03×10 -5
