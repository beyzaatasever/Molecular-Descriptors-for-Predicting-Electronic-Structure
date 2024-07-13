# Molecular-Descriptors-for-Predicting-Electronic-Structure
this project revolves around increasing accuracy in predicting electronic structures by integrating molecular descriptors with machine learning algorithms. The comprehensive research question aims to explore whether integrating these components can significantly improve the accuracy of electronic structure predictions. 



## Project Structure
- `Hidden_Layers_400.ipynb`: exploring the impact of different hidden layer configurations on model performance.
- `neural_network_hyperparameter_tuning.ipynb`: detailing the hyperparameter tuning process for optimizing the neural network.

## Project Explanation
- `Hidden_Layers_400.ipynb`:
In this project, I developed a neural network to predict HOMO-LUMO gaps using Coulomb matrix representations of molecular structures. Here's a concise overview of my approach:
I accessed and processed Coulomb matrix files from Google Drive. The files were sorted and read into Pandas DataFrames, transposed to have each file's data as a row, and then concatenated into a single DataFrame with 1999 rows and 841 columns. The target HOMO-LUMO gap values were extracted from a separate text file and converted into a NumPy array.
Using TensorFlow and Keras, I constructed a neural network with an input layer matching the 841 features, followed by several hidden layers. The final layer had a single neuron for regression. The model was compiled with the Adam optimizer and mean squared error loss function.


I split the data into training and testing sets (80-20 split) and experimented with different hyperparameters to optimize the model. The best model achieved a test loss of 4.97 and an R-squared value of 0.79. A scatter plot of actual versus predicted values showed a strong correlation, validating the model's performance.

This project successfully demonstrated the neural network's capability to predict molecular properties from structural data, offering a solid foundation for further exploration in computational chemistry.



- `neural_network_hyperparameter_tuning.ipynb`: I implemented a neural network to predict the HOMO-LUMO gap of molecules using SOAP descriptors. First, I mounted Google Drive to access descriptor files, filtered out specific files, and sorted the remaining files numerically. Each file's SOAP descriptors were read, flattened, and stored in a list, which I converted to a 2D NumPy array.

Using TensorFlow and Keras, I built a sequential model. The input layer had 10,350 features, followed by multiple dense layers with varying units, and a final output layer for regression. I split the data into training and testing sets with an 80/20 split. The model was compiled using the Adam optimizer and mean squared error loss function.

Hyperparameter tuning involved experimenting with different optimizers, activation functions, units, and layer counts. The training process iterated through these combinations, and the model achieved a test loss of 1.74 and an R-squared value of 0.93. The best configuration resulted in a test MAE of 1.14. A scatter plot of actual vs. predicted values showed strong correlation, indicating the model's effectiveness. This project demonstrates the power of machine learning for predicting molecular properties in computational chemistry.
