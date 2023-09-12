# Disulfide bond prediction

Disulfide bonds, also known as disulfide bridges or disulfide linkages, are covalent bonds formed between the sulfur atoms of two cysteine amino acids within a protein. These bonds play a crucial role in maintaining the stability and structure of proteins. Disulfide bonds contribute to the stabilization of a protein's three-dimensional structure. They form covalent linkages between specific amino acid residues and help lock the protein into its native or biologically active conformation. This stabilization is particularly important for proteins that need to maintain their structure in dynamic and fluctuating cellular environments. Disulfide bonds act as "molecular staples" that hold together different parts of a protein. These bonds resist the forces that would otherwise cause the protein to unfold or denature. 
This contribution of disulfide bond towards protein stability attracted our attention and we developed a CNN based regression model to predict number of disulfide bonds from protein sequence.

## Dataset

The dataset with protein sequences along with number of disulfide bonds was collected from [SCRATCH Protein Predictor](https://scratch.proteomics.ics.uci.edu/) provided by [Institute for Genomics and Bioinformatics, University of California, Irvine, USA](https://download.igb.uci.edu/). Dataset was curated to get a clean and significant data for model training. Frequency distribution of dataset post curation is represented in fig. 1. 

![image](https://github.com/Growdeatechnology/Di_sulphide_bond/assets/72397529/2a0b363e-5a2f-4b88-8029-ae8329492944)

 fig. 1: Frequency distribution of dataset

 To observe any possible relation between sequence length and number of disulfide bonds a graph was plotted between these two and is represented in fig. 2.

![image](https://github.com/Growdeatechnology/Di_sulphide_bond/assets/72397529/794e4903-90b9-4153-b49c-d3964e3e6111)

 fig. 2: Scatter plot of number of bonds against sequence length

A fixed pattern was not observed in the plot so the datapoints for disulfide were normalised by dividing each value with the length of their corresponding sequences. The normalised values were plotted against sequence length which is represented in fig. 3. 

![image](https://github.com/Growdeatechnology/Di_sulphide_bond/assets/72397529/51f4fb14-6f3d-41d2-abd1-0fb04919188e)

 fig. 3: Scatter plot of normalized value (target value) against sequence length

 Normalized values seemed to be suitaible for model training and hence was used for further processes.

 ## Encoder and Model

 The protein sequences present in training dataset were encodded before they were feeded to the model. 

![image](https://github.com/Growdeatechnology/Di_sulphide_bond/assets/72397529/f65c5bc4-c4be-4749-af25-6b8a7d190bbc)

 fig 4. Plotting of original data vs predicted data on test dataset

![image](https://github.com/Growdeatechnology/Di_sulphide_bond/assets/72397529/4ad0c923-87ba-4efc-925f-75bca4f886a3)

 fig 5. Plotting of original data vs predicted data without outliers
