# MSCI_436
Our code is structured into initial model visualizations and graphs, and then the streamlit application writer and run sections. The intial model visualizations were for us to be able to better understand the correlations between the model variables and sale price, allowing us to ask for the user's input on only the parameters that will have the most impact on the sale price prediction; It would not be useful to the user to need to enter 81 separate parameters, most of which will have only a marginal effect on the predicted sale price. By looking at the correlation ebtween the various columns and the Sale price, we were able to successfully narrow it down to a total of 27 columns that would have a reasonable impact on the house sale price.

The second half of the code is the streamlit application itself, and is divided up into four parts: Pulling in the raw data, the Interface, Processing the User Data and the Linear Regression Model. 

In the pulling in raw data portion, we read in the raw data for the columns we had selected in the code above, and ensure that any null values are filled according to the column type. 

The interface includes all the code for the interactive widgets and the visuals, as well as some simple code to convert the widget outputs into the codes for the columns as seen in the dataset.

The user data processing portion is only computed once the "Calculate Property Value Estimation" button is pressed, to help ensure the code runs smoothly and isn't doing unnecessary computations whenever a user enters an input into one of the widgets. This section ensures that there are no null values left over in the inputs, and encodes the categorical columns in preparation for linear regression.

Finally, the regression section completes the prediction of the model, and outputs the result, alongside the average house price for the same neighbourhood for the user to compare their house against. 

Colab share link: https://colab.research.google.com/drive/1d25JVC82vp3jjeRvWfAFGx-5oTRnGs37?usp=sharing
