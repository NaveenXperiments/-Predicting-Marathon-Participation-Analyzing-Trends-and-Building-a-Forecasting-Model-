# Marathon Data Analysis and Prediction 🏃‍♂️🏅

Welcome to the **Marathon Data Analysis and Prediction** project! In this project, we explore and predict marathon race participation, specifically the number of finishers, based on several features such as race type, year, season, and more. The project employs machine learning algorithms to provide insights into marathon trends and help organizers plan better.

![Marathon](https://img.icons8.com/ios/452/marathon.png)

## Project Overview 📊

In this project, we analyzed marathon race data from various events around the world and developed machine learning models to predict the number of finishers in each race. The dataset includes features like race name, year, date, and finishers. Using these features, we aimed to build predictive models that could estimate the number of finishers for a given marathon based on past data.

### Key Objectives:
- **Data Preprocessing** 🧹: Clean, transform, and prepare data for model building.
- **Feature Engineering** 🔧: Create new features such as the month, day, and season of the race.
- **Model Building** 🤖: Develop machine learning models such as Random Forest Regressor and XGBoost to predict the number of finishers.
- **Model Evaluation** 🏆: Evaluate the performance of these models using appropriate metrics like Mean Squared Error (MSE), R-squared, and others.

## Work Done 🔨

### 1. **Data Collection and Understanding 📥**
The project starts by gathering marathon data, which includes the following columns:
- **Race**: The name of the marathon.
- **Year**: The year in which the marathon was held.
- **Date**: The exact date of the event.
- **Finishers**: The total number of people who finished the race.

After loading the data, I performed initial exploratory data analysis (EDA) to understand the structure of the dataset and identify any issues, such as missing values or duplicates.

### 2. **Data Preprocessing 🧹**
To prepare the data for analysis, I handled various preprocessing tasks:
- **Date Handling** 📅: The 'Date' column was converted into a datetime format to extract features like month, day, and weekday.
- **Handling Missing Values** ❓: Checked for and handled any missing data, ensuring the dataset is clean.
- **Duplicate Removal** 🔁: Removed duplicate entries to avoid bias in the analysis.
- **Feature Creation** 🔄: Created additional features like `Month`, `Day`, `Weekday`, and `Season` (based on the month) to enhance the predictive power of the models.

### 3. **Feature Engineering 🔧**
Feature engineering is crucial in improving the performance of machine learning models. Some important feature engineering steps included:
- **Encoding Categorical Data** 🏷️: Categorical features such as race type, season, and race size category were encoded into numerical values using techniques like **Label Encoding**.
- **Normalization** 🌱: The 'Finishers' feature was normalized to scale the values between 0 and 1, ensuring better model performance.
- **Race Size Categorization** 📏: Created a new categorical feature to classify races based on the number of finishers (Short, Medium, Long).

### 4. **Model Building 🧠**
I implemented several machine learning models to predict the number of finishers:
- **Random Forest Regressor** 🌲: A tree-based model that is robust and works well with non-linear data.
- **XGBoost** 🚀: A powerful gradient boosting model used to improve the predictive accuracy of the task.

The models were trained on the training data, and hyperparameters were tuned using grid search to find the best combination of parameters.

### 5. **Model Evaluation 🏅**
After training the models, I evaluated their performance using metrics such as:
- **Mean Squared Error (MSE)** 📉: Measures the average squared difference between the predicted and actual values.
- **R-squared (R²)** 📈: Indicates how well the model fits the data. A higher R² value implies a better fit.
- **Accuracy** ✅: Calculated accuracy after binarizing the target variable.

The Random Forest Regressor achieved a MSE of 0.0037, while XGBoost showed a relatively lower R² score of -0.98, indicating room for model improvement.

### 6. **Results and Insights 💡**
The models provided interesting insights into marathon trends:
- Some races consistently have higher finishers than others.
- The performance of both models varied based on race type and season.
- The `Race_Encoded` and `Season_Encoded` features had significant predictive power in determining the number of finishers.

### 7. **Visualization 📊**
Throughout the project, I used visualizations to gain deeper insights into the data:
- **Correlation Heatmap** 🔥: A heatmap was created to understand the correlation between different numerical features like `Finishers`, `Month`, and `Day`.
- **Pairplot** 🖼️: Used to visualize the relationships between multiple features such as `Finishers`, `Month`, `Day`, and `Weekday`.
- **Boxplots and Violin Plots** 📈: These were used to analyze the distribution of finishers across different races and seasons.
- **Time Series Plot** ⏳: A line plot showing how the number of finishers changes over time, categorized by season.

### 8. **Challenges and Future Work 🚧**
While the models were able to make predictions, the relatively low R² value indicates there is still room for improvement. Possible future steps include:
- Exploring more sophisticated models like **Neural Networks** 🧠.
- Implementing feature selection techniques to reduce noise in the data.
- Investigating other external factors that may affect the number of finishers, such as weather 🌤️ or global events 🌍.

## Installation Instructions 💻

To run this project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/username/repository.git
