# mintRULS
mintRULS work flow


Scripts for cross validations

Simulations on human data

KronRLS_settingA1.py is for running simulations in LOOCV condition.
KronRLS_settingC1.py is for running simulations in LmiTOCV condition.

Simulations on mouse data

KronRLS_settingA1_mouse.py is for running simulations in LOOCV condition.
KronRLS_settingC1_mouse.py is for running simulations in LmiTOCV condition.	

Data folders

In order to run above simulations, please confirm the following folders.
1)	Folder “MyData” contains all required sub-folders e.g. “Interaction_data”, “miRNA_features”, “mRNA_features”, and “Results” and all corresponding materials. 
2)	Similarly, in case of simulation using mouse data, MyData_mouse folder contains same pattern of folders and sub-folders.
The contents of the folders “MyData” and “MyData_mouse” can be accessed from https://doi.org/10.5281/zenodo.5639816
Inside individual folders-
a)	the interaction data (known or imputed) has to be filled in the “\MyData\Interaction_data\human_data”.
b)	The different similarity scores (e.g. FE, SSR, Gaussian, and Needleman) of query miRNA with the existing ones should be calculated separately and kept in the “\MyData\miRNA_features”. 
c)	The different similarity scores of query miTS should be in the “\MyData\mRNA_features”.
d)	The result folder “\MyData\Result” contains results of the simulation in text file.
The similar pattern of folders and sub-folders can be followed in case of mouse data. 

The python scripts as mentioned above can be executed to run the simulations. The output is save in the folders \MyData\Result and \MyData_mouse\Result


Making query and predict interactions 

The predicted interaction scores by mintRULS in human and mouse have been saved in the folder “Query_interactions_Human_and_Mouse”, which can be accessed from https://doi.org/10.5281/zenodo.5639816.
This folder contains separate sub-folders for human and mouse. Inside each sub-folder, execute  the following steps for predicting the score for query pair- 
1)	Write query pairs in the query file “query_interactions.csv”, as given in the example.
2)	Run “1_Human_data_query_interactions.py”, and check the output in file “Query_output.txt”. 
Similar workflow can be followed in case of mouse data. 
