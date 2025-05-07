# House Price Prediction

## Project Description
This project aims to use regression models in machine learning to predict the house price based on various house features, including the area, year built, number of bedrooms and more. In total, there are 4 different regression model used at first, including a random forest regressor while the rest of the three are multiple linear regression with ridge, lasso, and elastic net regularization. Model selection is employed by training the 4 models using the training dataset, then based on their performances in terms of mean squared error (MSE) on the validation dataset, I select the best performing model for the final prediction using the testing dataset (includes 146 individual houses). The final selected model turned out to be ridge regression, which is used for the final house price prediction and the result is assessed by R² score and MSE. The comparison between the prediction and actual house price is visualized into two plots, being a line plot and a histogram.

## Prediction Results
- Figure 1: House Price Values Comparison Line Plot

![Prediction VS Actual line plot](https://github.com/user-attachments/assets/683e2c70-dfb9-4fa6-bfa8-d133d6023c49)

- Figure 2: House Price Distribution Comparison Histogram

![Prediction VS Actual Histogram](https://github.com/user-attachments/assets/3c2e8634-7437-4f4f-8486-d3d80d1d4462)

## How to Install and Run the Project
### Dependencies:
  - sklearn >= 1.5.2
  - matplotlib >= 3.10.0
  - seaborn >= 0.13.2
  - pandas >= 2.2.3
  - numpy >= 1.26.4

### Instructions:
  1. Make sure all libraries in the above dependency list are installed to your current working environment
  2. Download the HousePricePrediction.csv file and two ipynb files
  3. Run the Data_processing.ipynb file to give you a cleaned dataset called Cleaned_house_price.csv, which should be stored in you current directory
  4. Run the Machine_learning.ipynb file to do the house price prediction, and the prediction results should appear at the end of the notebook cells.

### Troubleshooting:
  - If there's error reading the HousePricePrediction.csv file, make sure it's in the same directory as your ipynb files and its name isn't modified after downloaded. If there's error reading the Cleaned_house_price.csv file, make sure you store it in the same directory as you ipynb files but not other folders, and its name isn't modified from what it was in the code.
  - If there's error with the libraries used, make sure they're all properly installed to your current environment, and the version are the same or newer than the versions in the dependency list
  - If there's error of getting a different prediction result and graphs, re-run the entire notebook files from the very first to the last cell.

## How to Use
### Using the Two ipynb Files


### Interpreting the Model Performance:
The R² score of the prediction result is 0.652, indicating that 65.2% of the house price variance is explained by the fluctuation in house features. This means most patterns and trends within the dataset are captured and learned by the model, indicating a good model fit. Although the prediction result has a MSE of 2.4 billion, it’s an acceptable and reasonably low error considering how large the house price gets, which usually ranges from hundreds of thousands to even millions, and thus often leads to high MSE value after the error is being squared. Overall, the result tells that there’s indeed a certain level of linear relationship between the house features and house price, and a moderately accurate price prediction can be made through proper model training, selection, and testing using ridge regression. With that being said, there is definitely room for improvement in terms of reducing prediction errors and making more precise predictions, which could be done through validating more non-linear models with a larger dataset to better find the patterns between house features and house price.

### Interpreting the Result Graphs:
Figure 1 is a line plot showing the fluctuation in the predicted house price and actual result. The x-axis is the index for individual houses and the y-axis is the house price. The blue line is the predicted house price while the yellow line is the actual price. Throughout each of the 146 houses in the testing subset, the blue and yellow lines constantly overlap and stay very close to each other. This indicates an accurate model performance as the predicted house price closely follows the up-and-down trend of the actual price. Figure 2 is a histogram showing the distribution of the actual house price and predicted price. The x-axis is the house price and the y-axis is the density, while the yellow density curve represents the predicted house price and the blue bars represent the actual price. The yellow curve follows the same trend of the blue bars as they both peak at the price around 150,000 - 200,000, and remain low for prices below 80,000 or above 300,000. It shows that the density distribution of the prediction and actual house price are highly identical, indicating a good model performance and accurate prediction. Overall, these two figures show that the predicted house price follows closely with the trend of the actual price for the 146 individual houses in the testing dataset with small/acceptable errors, while the prediction and actual house price also share a highly similar distribution pattern that follows a bell curve but slightly right skewed.

## Analysis You Can Do Using the Prediction Results
- Looking at the line plot, does it reveals possibility of overfitting of the dataset or not?
- Looking at the?
- Given a specific cancer, are male or female patients more likely to get the disease over the other?
- Given a specific cancer, which age group is the most or least likely to get the disease?
- Given a same disease, is there a difference in the therapy used between male and female patients? Is it the same between younger and older patients?

## Contributors
1. Kuan-Chun Chiu (Myself) - beagledirk1@gmail.com
2. Atharva Nilapwar - adhikari.ay@northeastern.edu
