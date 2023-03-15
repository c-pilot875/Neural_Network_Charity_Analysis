# Neural_Network_Charity_Analysis
Neural Networks and Deep Learning Models

## Dataset:
charity_data.csv

## Software Used:
`Tensorflow`
`Python 3.7`
`sklearn`

## Purpose 
The purpose of this project was requested by Alphabet Soup to preditc where to make investments with their foudnation. Using machine learning and neural networks to feature the provided dataset, a binary classifier was created capable of predicitng success of appicant's funded by Alphabet Soup. The dataset contained 34,000 organizations along with meta data from the fundings.

## Results:

### Data Processing
1. What variables are considered the targets for the model?
Target variables were marked as "successful" in the Dataframe.

2. What variables are considered to be the features of the model?
The variable "IS_SUCCESSFUL" is the feature for this dataset.

3. What variables are neither targets or features, and should be removed from the input data?
The "EIN" and "NAME" column were removed from the input as they would not have increased the accuracy of the model.

## Compiling, Training, and Evaluating the Model

4. How many nuerons, layers, and activation functions where selected for the neural network model, and why?
For the original model I selected 80 neurons for layer_1 ad 30 nurons for layer_2 with a `relu` activation. The `sigmoid` activation was used for the final layer which seemed to be the better fit.

![Origin_model](https://user-images.githubusercontent.com/115188500/225425015-d37d940c-bcae-4bf1-8e8b-0fdf22533001.png)

5. Was the target model performance achieved?
The target for the model was 75% or higher, but the original model produced 72.5% accuracy.

![Origin_result](https://user-images.githubusercontent.com/115188500/225425415-4b950528-5e33-4e63-b45a-2e019590b4d3.png)

6. What steps were taken to try and increase model performance?
* To increase model performance I first increased the neurons to 110 for layer_1 and 40 for layer_2 using the same `relu` activation and `sigmoid`. This resulted in a 72.5% accuracy.

![Optimization1](https://user-images.githubusercontent.com/115188500/225425605-b90a3e32-fdfc-425f-b107-6eb52ebbb736.png)

* For the second optimization I used a third hidden layer with 20 neruons which resulted in a similar output of 72.5% accuracy.
* 
![Optimization2](https://user-images.githubusercontent.com/115188500/225426295-4f4148fa-cf16-4f62-baa6-b78c03887b9e.png)

* For my third attempt to optimize I used the `tanh` activation for all three hidden layers which resulted in 72.4% accruacy. All optimization changes seemed to have little affect on the accuracy output, leaving the `'relu` and `sigmoid` model as the best.
* 
![Optimization3](https://user-images.githubusercontent.com/115188500/225426519-db45dc9a-11b5-43b5-a868-b6bf27484ad6.png)

## Summary:
The second optimization model proved to output the highest accruacy score of 72.5%. A recommendation would be to try the `random forest classifier` module.
