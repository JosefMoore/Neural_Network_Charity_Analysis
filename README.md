# Neural_Network_Charity_Analysis

### Overview of Analysis
______________________________

The purpose of this analysis was to determine if a charities and organizations would be successful if funded by Alphabet Soup. We have a dataset containing 34,000 entries of charites that have received funding from Alphabet Soup and are tasked with creating a binary classification model to predict success or failure. 

### Results
______________________________

#### What variable(s) are considered the target(s) for your model?
* Our target for this evaluation was pretty cut and dry. We used the IS_SUCCESSFUL column since we will be trying to predict whether or not an organization would be successful provided they were funded by Alphabet Soup.

#### What variable(s) are considered to be the features for your model?
* Every feature aside from the EIN column were features in our dataset. 

#### What variable(s) are neither targets nor features, and should be removed from the input data?
* We removed the EIN column as stated above. It is useless for our model as it just assigns a number to reference for organizations. During the training process I experimented with the removal of other features to try and better the models accuracy to no avail. Removing features from the dataset proved to be detrimental, and they're all generally usefull. The only column, besides EIN, that didn't change our accuracy much was the STATUS column. 

#### How many neurons, layers, and activation functions did you select for your neural network model, and why?