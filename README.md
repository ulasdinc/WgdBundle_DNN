# Photonic waveguide bundles using 3D laser writing and deep neural network image reconstruction
DOI: https://doi.org/10.1364/OE.446775

This repository contains the dataset of digits, the Beam Propagation Method (BPM) code, and the U-net type convolutional neural network (CNN) underlying the results presented in
the paper whose DOI link and the title are given above. Please see the article for details of the study.

The dataset is created by rotating and scaling the layout of the digits we have patterned to be used as the physical imaging sample
(Supplement 1, Section 9 of the article) in the experiments. This dataset can be found in the dataset folder. The file is d_all_norm256.zip.

You can use the Beam Propagation Method (BPMforWgdBundles) to propagate the given inputs. You can change the waveguide number and dimensions, the length of the bundle, etc. 
Please see the comments in the BPMforWgdBundles code for customizing your simulation. The code is written in a easy to use manner by providing necessary explanations
in the commented lines.

Then, you can use Bundle_U_net code, which provides a U-net type convolutional neural network using Keras (details can be found in Supplement 1, Section 7 of the article).
The propagated patterns are your inputs to be reconstructed. The ground-truths are the original input patterns you provided to BPM as inputs. You can train the network by providing these pairs. In the Bundle_U_net code, you will see optional sections for adding a synthetic background noise and removing the cladding light. Please see the explanations given in the commented lines of the script.

For further questions, please send an email to niyazi.dinc@epfl.ch

