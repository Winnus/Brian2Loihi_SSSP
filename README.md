# Brian2Loihi_SSSP
Jupyter notebooks containing a SSSP algorithm implementation 


# Single Source Shortest Path

An implementation of a Wavefront algorithm using spiking neurons. \
An in depth description of such an algorithm can be viewed in [0].\
The algorithm is implemented using the [Loihi emulator](https://github.com/sagacitysite/brian2_loihi) described in [1].\
Concrete values and the learning rule are taken from the PathPlanning library provided by Intel via their NxSDK Apps package (you have to be INRC member to get the package).

In summary the idea is that a wave of neuron spikes is running trough a lattice graph - a lattice graph is a rectangle of nodes where every node is, if possible, connected to their four surounding neigbours - until the spike front hits the target node / neuron. \
Path backtracing is done via the synaptic weights, which are altered by an anti hebbian leraning rule to enable a change in the weight that can be backtraced to reconstruct the shortest path.

[0] Ponulak F, Hopfield JJ. Rapid, parallel path planning by propagating wavefronts of spiking neural activity. Front Comput Neurosci. 2013 Jul 18;7:98. doi: 10.3389/fncom.2013.00098. PMID: 23882213; PMCID: PMC3714542.

[1] Brian2Loihi: An emulator for the neuromorphic chip Loihi using the spiking neural network simulator Brian
Carlo Michaelis, Andrew B. Lehr, Winfried Oed, Christian Tetzlaff
