# M-Tune : Mean Based Optimized Thresholding Tuning
This is an implementation of M-Tune Thresholding Shifting Method. 
This method is based on the mean probablities value. In the Direct-M-Tune,
the classifier model is trained with training data and the prediction probablities
are extracted. The mean of the prediction probablities is the new threshold for the input data.

In the ENSEMBLE-M-Tune method, the majority class is grouped as small k-subsets. 
Multiple smaller groups are created based on k-subset with minority class. The classifier is trained with the 
each subset and prediction probablities are extracted. The prediction proablities are considered as the new threshold.
Each instance are classified based on the new threshold and majority voting. 



The method was implemented for 6 cell-lines for 11 fingerprints.


# Contents of the Repository

1. **Cell-Line SMILES**

    This directory contains SMILES for all the Six Cell-Lines. The folder TGF-B contains one training set and one external validation set. 
	
2. **Example of Fingerprints**
    
	The folder TGF-B Train FP and TGF-B External FP contains the example AtomPairs2DCount output for training set and external set respectively. 

3. **M-tune Example**:

    As an example M-Tune has been implemented for `TGF-B Cell-line` in notebooks `DIRECT-M-Tune.ipynb` and `ENSEMBLE-M-Tune.ipynb`.
	DIRECT-M-Tune.ipynb: Identification of threshold and classification based on single input data. 
	ENSEMBLE-M-Tune.ipynb: Identification of threshold and classification based on small k-subsets and majority voting. 
	
	
2. **Calculate_fps.ipynb** :  

    This notebook contains code for downloading or Calulating the 11 Fingerprints considered for the cyto-toxicity cell-line datasets.
	
    1. AtomPairs2DFingerprintCount
    1. AtomPairs2DFingerprint
    1. EStateFingerprint
    1. ExtendedFingerprinter
    1. Fingerprint
    1. GraphOnlyFingerprint
    1. KlekotaRothFingerprint
    1. MACCSFingerprint
    1. PubchemFingerprint
    1. SubstructureFingerprintCount
    1. SubstructureFingerprint
	
*NOTE: This notebook access "xmls" folder to calculate respective selected fingerprints. 



4. **Libraries used**:

    The necessary libraries used in this implementation has been listed in the `reqs.txt` file.
