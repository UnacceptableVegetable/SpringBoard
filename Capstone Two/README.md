# Predicting air quality due to wildfire smoke

>Wildfires that burn near populated areas can have significant impact on the environment, property, livestock and human mortality and morbidity depending on the size, speed and proximity to the fire, and whether the population has advanced warning to evacuate.
>
>Wildfire smoke is a mixture of air pollutants of which particulate matter (PM) is the principal public health threat.
>
>PM2.5 from wildfire smoke is associated with premature deaths in the general population, and can cause and exacerbate diseases of the lungs, heart, brain/nervous system, skin, gut, kidney, eyes, nose and liver. It has also been shown to lead to cognitive impairment and memory loss. Firefighters and emergency response workers are also greatly impacted by injuries, burns and smoke inhalation, particularly at high concentrations.
> --- [WHO](https://www.who.int/health-topics/wildfires#tab=tab_2)

The goal of this project is to predict the longevity of PM2.5, particulate matter most associated with wildfires (with diameters 2.5 micrometers or smaller). We will look at weather station and air quality monitors around the San Francisco metro area from 2018 to 2019.

## Data

The Centers for Disease Control and Prevention is the national public health agency of the United States. The following CDC dataset contains the target feature PM2.5 concentration (‘DS_PM_pred’) which indicates fine particulate matter most associated to wildfires (2.5 micrometers and smaller). According to the WHO and EPA, the recommended short-term (24-hour) PM 2.5 level is 15 μg/m3.

> * <https://data.cdc.gov/browse/select_dataset?tags=pm2.5>

The Automated Surface Observing System (ASOS) is considered to be the flagship automated observing network. Located at airports, the ASOS stations provide essential observations for the National Weather Service (NWS), the Federal Aviation Administration (FAA), and the Department of Defense (DOD). The primary function of the ASOS stations are to take minute-by-minute observations and generate basic weather reports.

> * <https://mesonet.agron.iastate.edu/ASOS/>

## Notebooks

1. [data_wrangling.ipynb](https://github.com/UnacceptableVegetable/SpringBoard/blob/main/Capstone%20Two/data_wrangling.ipynb)

Data Wrangling: time series data from the CDC and ASOS is merged to form datasets with explanatory variables in weather and a response variable in PM2.5. Highlights include:

- Missing data analysis
- geopandas
- Inner merge

2. [eda.ipynb](https://github.com/UnacceptableVegetable/SpringBoard/blob/main/Capstone%20Two/eda.ipynb)

Exploratory Data Analysis: the newly merged dataframe is analyzed for important features. Highlights include:

- Correlation table

3. [preprocessing.ipynb](https://github.com/UnacceptableVegetable/SpringBoard/blob/main/Capstone%20Two/preprocessing.ipynb)

Preprocessing: the time series data is experimented on how it can be implemented into a regression analysis framework. Highlights include:

- Time series cross-validation
- Scaling
- One hot encoding

4. [modeling.ipynb](https://github.com/UnacceptableVegetable/SpringBoard/blob/main/Capstone%20Two/modeling.ipynb)

Modeling: 4 models LSTM, Linear regression, Ridge regression, and Lasso regression are compared using RMSE. 


## Model Metrics

Final model features, parameters, hyperparameters, and performance metrics. 

[model_metrics.txt](https://github.com/UnacceptableVegetable/SpringBoard/blob/main/Capstone%20Two/model_metrics.txt)


## Report

[capstone_two_final_report.pdf](https://github.com/UnacceptableVegetable/SpringBoard/blob/main/Capstone%20Two/capstone_two_final_report.pdf)