
<a name="readme-top"></a>

#### [Dataset Source](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/data)

<h3 align="center">DT Algorithm Bakeoff</h3>

  <p align="center">
    Comparing efficiency and accuracy of DT, RF and GBDT algorithms on transactional sales data.
    <br />
  </p>
</div>


<!-- ABOUT THE PROJECT -->
## About The Project

The goal behind this project is to take a practical and grounded look at popular tree based algorithms and to review how they perform on real world data. There were some important concessions made to accomdate computational limitations. The original dataset contained over 3 million observations, and when categorical variables were transformed via one-hot encoding the resulting dataframe exceeded available memory. Bayesian optimization was also limited to 128 trials due to the significant time needed to cross validate complex GBDT models. Access to additional compute resources, or utilizing embeddings to convert categorical variables to high dimensional vectors are two avenues of improving upon the scope of this project.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


### Built With

* [![Python](https://img.shields.io/badge/python-000000?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
* [<img src="https://seaborn.pydata.org/_images/logo-tall-lightbg.svg" width="100" height='100'/>](https://seaborn.pydata.org/)
* [<img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" width="100" height='100'/>](https://scikit-learn.org/stable/)
* [<img src="https://miro.medium.com/max/720/1*yhE3CBwTrlXcAIvNJNTQiA.webp" width="150" height='100'/>](https://xgboost.readthedocs.io/en/stable/)
* [<img src="https://raw.githubusercontent.com/microsoft/LightGBM/a17489328c4f81819b5a4131c9a386b09b90b04f/docs/logo/LightGBM_logo_black_text.svg" width="150" height='100'/>](https://lightgbm.readthedocs.io/en/v3.3.2/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

A description of repo files are below:

* bakeoff.ipynb
  -  Jupyter notebook containing code to clean/transform data, train/optimize/visualize models, compare model RMSE values as a metric of accuracy.
  -  Note that blocks containing hyperparameter optimization are commented as trial results are imported as csv files produced from cloud training sessions. If there is a desire to run the hyperopt blocks locally, uncomment the code and run the appropriate cells. Parameter finding may take 12+ hours for the more complex GBDT models.

* csv_files.zip : **extract csv files and place them in the same directory as bakeoff.ipynb before running the notebook**
  - holiday_events.csv : a list of regional/local/national holidays and dates
  - oil.csv : national oil export data
  - stores.csv : locations and store numbers
  - target.csv : sales amount (response variable)
  - train.csv : training data
  - transactions.csv : contains product categories and information on promotional sales
  - lgb_trials_df.csv, xgb_trials_df.csv, rf_trials_df.csv : exported csv files containing hyperparamter optimization trial values from cloud sessions

### Prerequisites

Outside of standard popular DS libraries (matplotlib, seaborn, pandas, numpy, scikit-learn), this notebook also utilizes hyperopt for Bayesian optimization as well as XGBoost and LightGBM for their distinct approaches to building GBDT models.

<!-- USAGE EXAMPLES -->
## Usage

This project was designed to develop a more practical understanding of the advantages of different tree based models on tabular data, but may not be widely applicable to all use cases. The bayesian optimization portion of the notebook code has high reproducibility, but other sections will require tuning according to the context and purpose of the project. 

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CONTACT -->
## Contact

Paul Song - songpaul8@gmail.com

Project Link: [https://github.com/github_username/repo_name](https://github.com/songpaul8/dt_algo_bakeoff)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
