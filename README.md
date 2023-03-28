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
I spent a lot of time trying to optimize the model in order to get better accuracy and lower loss. I tried anywhere between 2 and 8 layers, between 1 and 13 neurons, and multiple activation functions. Typically, the optimization function applied, using keras hyperband, determined around 2 to 3 layers was best. I let the hyperband choose between relu, tanh, and sigmoid activation functions for the hidden layers. It tended to bounce between relu and tanh. The sigmoid activation function was chosen for the final output. Sigmoid deals with values between 0 and 1, so that works perfectly for our output activation function. I could've spent more time on the model, but I've already devoted several hours to optimization and I'm sure I could've done better than 80% accuracy.
![Results/best_hyperparameters.PNG]

#### Were you able to achieve the target model performance?
I did achieve over the goal of 75% accuracy but, again, I'm sure I could've done better. There is a lot to the tensorflow library that I'm sure I could've been utilizing. I could've also made many mistakes along the way. For example, I realized after I did a lot of testing that I was using a random state while splitting the data into testing and training sets. This made it so I was splitting the data the same way everytime I ran my notebook. It also took me time to re-add the name column back into the dataset, since it was organization names and not people's names. 

#### What steps did you take to try and increase model performance?
I went through numerous changes to try and improve model performance. I added and removed features. I tried different bucketing values to try and see if more or less buckets changed anything. Lastly, I tried optimizing the parameters of the model itself, as described above.

### Summary
______________________________

Overall, our goal was achieved with satisfactory performance. Our model achieved close to 80% accuracy and 44% loss. If I had to try another model, I would use another supervised machine learning model, such as a logistic regression model for binary classification. They're typically quicker to set up and require less machine performance. 