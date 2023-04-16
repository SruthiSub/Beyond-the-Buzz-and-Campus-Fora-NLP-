# Beyond-the-Buzz-and-Campus-Fora-NLP-
The executed code of the model can be referred here:
https://colab.research.google.com/drive/13FnAUJJFLA-I-UgLQI7GSvVMTD1sYt2e?usp=sharing

Importing all the required libraries. We mainly use keras from tensorflow in this model. 

Downloaded all the data- the data to train the model as well as the data required to test the model

Converted the data into the files we require- extracting all X columns and Y column seperately to use easily in further code

Building the neural network:
A neural network is basically a system of multiple nodes in different layers. It is a complicated function in which we input the first layer and get the last layer as the output.
Each layer is a linear function of the previous layer and we can obtain each element of the layer as a linear function of all the elements of the previous layer. (each element= (sum of products of weights of each x(of the previous layer) and x)+a bias term)
When we create a model, we are defining the structure of our neural network, in the sense, how many layers we require and how many nodes we want in each layer. When we assign this, python automatically creates all the weights and biases required in the model and when we train the model with the training data, python edits these weights and biases to the most optimum values, increasing accuracy of our model.

In model.compile()=> we give the loss function we want to use, which in this case is the Mean Absolute Error. The weights and biases, i.e. variables in the model are adjusted to get the least loss according to this function.
in model.fit(), we give the data to train it with along with epochs, which tells python how many times to go through the training set, and batchsize, which determines the number of batches python runs while training the model.

Once we run model.fit(), values are assigned to all weights and biases and we can now use this to predict the values for the test data. 
I have converted the predicted values into a numpy array, which I have then saved as a csv file, on which I have ran an if function to obtain the Verdicts. The file is uploaded in the repository.
