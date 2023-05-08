# Neurotransmitter-classification
Neurons use different neurotransmitters to communicate; some are excitatory, while others are inhibitory; others alter neural activities in more subtle ways. 
Previous efforts have used machine learning to predict what neurotransmitters a neuron uses based on electron microscopy images ([Eckstein et al., 2020](https://www.biorxiv.org/content/10.1101/2020.06.12.148775v2)).
First, I reproduce those results in this project.
These previous results are from an electron microscopy volume, the "Full Adult Female Brain," ([FAFB](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6063995/)), which uses serial section transmission electron microscopy.
More recent electron microscopy volumes use Focused Ion Beam Scanning Electron Microscopy, which generates superior resolution in the z dimension, at the cost of x-y resolution.
![ssTEM vs. FIB-SEM](https://github.com/philshiu/Neurotransmitter-classification/blob/main/Readme%20Images/ssTEM%20vs%20FIBSEM.png?raw=true)
I find that using FIB-SEM microscopy images results in significantly worse neurotransmitter predictions.
Finally, I compare synapse-level neurotransmitter predictions versus synaptic bouton-level predictions. Synaptic boutons contain many synapses; Eckstein et al., 2020 predicted
neurotransmitters at the synapse-level. However, this may be problematic because the synapse
is at the edge of the neuron, so by definition, these images only contain 50% of the neuron of interest. Furthermore, these images may be too small to contain relevant information to predict
neurotransmitters accurately. I find that predicting neurotransmitters using the entire synaptic bouton dramatically increases accuracy, even when the same total area of image data
is used for training.
![Bouton vs. Synapse](https://github.com/philshiu/Neurotransmitter-classification/blob/main/Readme%20Images/Bouton%20vs%20synapse.png?raw=true)
