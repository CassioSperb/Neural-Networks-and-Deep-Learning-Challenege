# Neural-Networks-and-Deep-Learning-Challenege
Cassio Sperb

### Overview of the analysis: 
The nonprofit foundation Alphabet Soup wants a tool that can help it select applicants for funding with the best chance of success in their ventures. Using machine learning and neural networks, I used the features in the provided dataset to create a binary classifier that predicts whether applicants will be successful if funded by Alphabet Soup.

Received a CSV from Alphabet Soup’s business team, containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

### Results: 

* Data Preprocessing

    * The target variable for the model is `IS_SUCCESSFUL`, which indicates whether an applicant was successful or not. It is a binary variable (0 or 1).
    * The categorical variables used as features for the model include `APPLICATION_TYPE` and `CLASSIFICATION`.
    * The numerical variables used as features for the model include `ASK_AMT`, `STATUS`, and others depending on the dataset.
    * The variables `EIN` (Employer Identification Number), which does not contribute to predicting success, and `NAME` (the name of the organization), which is not relevant for modeling and could introduce noise, were removed.
    

* Compiling, Training, and Evaluating the Model

    * How many neurons, layers, and activation functions did you select for your neural network model, and why?
I selected 96 neurons for the first and second layers, and 64 neurons for the third layer. This configuration was determined using hyperparameter tuning to balance model complexity and performance.
The model has three layers in total, chosen to provide sufficient capacity to capture patterns in the data while avoiding overfitting.
I used the ReLU (Rectified Linear Unit) activation function for the hidden layers because it is efficient, avoids vanishing gradient issues, and works well for most neural network tasks.   
The output layer uses the Sigmoid activation function because this is a binary classification problem, and Sigmoid outputs probabilities between 0 and 1.

    * Were you able to achieve the target model performance?
The model achieved a final accuracy of 72.73% with a loss of 0.5583, which doens't achieve the target model performance. 
   
    * What steps did you take in the attempts to increase model performance?
To improve the model's performance, I implemented Hyperparameter Tuning, applied a dropout rate of 0.0, as regularization was not needed given the model's performance and dataset complexity. Scaled the input features using a StandardScaler to normalize the data and improve convergence. Trained the model for up to 50 epochs, starting from 17 epochs during tuning to ensure the model had sufficient time to learn without overfitting.

### Summary: 
The model performed well given the complexity of the task and the data provided. Further steps to increase accuracy might include collecting more data, experimenting with additional architectures (e.g., more layers or alternative activation functions), or implementing advanced techniques like ensemble learning or feature selection.