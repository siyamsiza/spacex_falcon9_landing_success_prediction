# SpaceX Falcon 9 First Stage Landing Prediction

## Project Overview

This project aims to predict the landing success of SpaceX's Falcon 9 first stage rocket. SpaceX's ability to reuse the first stage of their rockets is a key factor in reducing the cost of space transportation, making their launches significantly cheaper than those of other providers. By accurately predicting the landing outcome, this project seeks to provide valuable insights that could influence cost estimation and competitive bidding in the aerospace industry.

## Introduction

The SpaceX Falcon 9 rocket has revolutionized space travel with its reusable first stage, significantly lowering launch costs. In this project, we utilize machine learning techniques to predict the success of the first stage landing. The ability to make these predictions can help in estimating launch costs and assessing SpaceX's competitive edge.

## Data Collection

Data for this project was collected through web scraping techniques, focusing on historical launch data of SpaceX rockets. This includes details such as the payload mass, launch site, booster version, and landing outcome.

## Methodology

### Data Wrangling
- The dataset contains various landing outcomes, including successful and failed attempts on ocean platforms, ground pads, and drone ships.
- These outcomes were converted into binary training labels, where `1` represents a successful landing and `0` represents a failure.

### Model Building
- The dataset was loaded and transformed using NumPy and Pandas.
- Data was split into training and testing sets.
- A variety of machine learning algorithms were tested, with hyperparameters tuned using GridSearchCV.
- Models were trained and evaluated based on accuracy.

### Evaluation and Improvement
- Accuracy scores were calculated for each model, with confusion matrices plotted for further insight.
- Feature engineering and algorithm tuning were applied to improve model performance.
- The model with the best accuracy was selected as the final model.

## Results

- The **Tree Classifier Algorithm** was identified as the best-performing model for this dataset.
- Analysis showed that lower payload weights are associated with higher landing success rates.
- The success rate of SpaceX launches has improved over time, indicating continuous advancements.
- The **KSC LC-39A** launch site had the highest success rate among all sites.
- Orbits such as **GEO, HEO, SSO,** and **ES-L1** showed the best landing success rates.

## Usage

The haversine formula was used to calculate the great-circle distance between two points on the Earth's surface, based on latitude and longitude coordinates. This formula was chosen due to its accuracy in accounting for the Earth's spherical shape.

## Deployment

The project’s dashboard was built using Flask and Dash web frameworks and is hosted on PythonAnywhere, allowing it to be live 24/7. The dashboard includes visualizations such as:
- A scatter plot showing the relationship between landing outcome and payload mass.
- Pie charts displaying the distribution of launches across different sites.

## Conclusion

- The Tree Classifier Algorithm is the most effective model for predicting Falcon 9 first stage landing success.
- Launch success rates are positively correlated with time, indicating continuous improvement in SpaceX's technology.
- KSC LC-39A emerged as the most successful launch site, and certain orbits were particularly associated with successful landings.

## How to Run

1. Clone the repository.
2. Install the required Python packages listed in `requirements.txt`.
3. Run the Flask app to view the dashboard.
4. Use the notebook to experiment with the data and models.

## Future Work

- Integrating more detailed weather data for enhanced predictions.
- Expanding the model to predict launch success for other SpaceX rockets.
- Developing more advanced visualization techniques to better analyze the results.

## Acknowledgments

Special thanks to the SpaceX API and various online resources for providing the data and tools necessary for this project.
