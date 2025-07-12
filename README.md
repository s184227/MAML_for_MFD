# MAML for MFD

The provided code has been designed for the implementation of Model Agnostich Machine Learning to estimate the Macroscopic Fundamental Diagram in data scarcity settings.
The code has been tested on the UTD19 dataset, a public source freely accessible at: https://utd19.ethz.ch/
  

MAML trains models to understand and adapt to new tasks on their own, to alleviate the data scarcity challenge (namely, in the tested use case, with a reduced number of loop detectors). The developed model is trained and tested by leveraging data from multiple cities and exploiting it to model the MFD of other cities with different shares of detectors and topological structures.The model itself is also implemented in the code under the acronym MTPINN (Multi-Task Physics Informed Neural Network), a non parametric model designed to estimate three key parameters of the MFD: the critical occupancy, the maximum flow, and the flow-occupancy relationship. MTPINN integrates Multi-Task Learning (MTL) and Physics-Informed Neural Networks. More specifically, MTL leverages shared layers for common high level representations, while defining task-specific layers for the output branches. Physics-Informed regularization techniques are used to introduce domain knowledge into the MTL architecture. 

# The code
The code can be found in the folder "models".  
- Biparabolic_model_for_MFD implements a white box, benchmarking model
- MultiTaskPINN_for MFD implements the MTPINN as stand-alone, without meta-learning
- meta-learning_for_MFD implements the MAML framework, exploiting the MTPINN as defined in the dedicated code

# The data
The data is publicly available at: https://utd19.ethz.ch/. The "data preparation" folder includes the following code:
- data_preparation for cleaning and reformatting the data as suitable input for the code in "models"
- reduce_loop_detectors for creating datasets with reduced number of loop detectors in the right format  

# The results
The folder "results" includes the extended plots, tables and numerical outputs from the carried out experiments. The folder is structured in the following subfolders:
- MTPINN experiments, in which the outputs of the MAML framework with an embedded MTPINN are reported. It includes the following subolders
    - 75_detectors experiment
    - 50_detectors experiment
    - 25_detectors experiment
    - 10_detectors experiment