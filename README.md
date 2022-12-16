# Fintech Sector Portfolio Analysis 

This project is a portfolio analysis of different sectors within Fintech to better understand the growth, correlations, and profitability of Fintech companies. Through analyzing different calculations such as finding the cumulative returns, 21-day rolling average and standard deviations, Sharpe ratios, and running Monte Carlo simulations, our analysis should provide insights into which sectors/stocks in Fintech would be good investments. 

Through our analysis we hope to answer the following questions: 
1. How does each Fintech sector, and the individual stocks within them, perform over time?
2. Which sectors and individual stocks are the best potential investments? 
3. What are the relationships or correlations between each sector? 
4. Based on what we learned about the sectors and stocks, if we were to come up with a Fintech portfolio what stocks would we choose?

### Data Used
We currently use [yfinance](https://pypi.org/project/yfinance/) to grab 5 years of closing price data (from the time that the notebook code is ran) for the following sectors if Fintech: 
    
1. Paytech
    * PayPal 
    * Square
    * MasterCard
2. Lending
    * LendingTree
    * LendingClub
    * Black Knight
3. Banking
    * Fiserv
    * Jack Henry and Associates
    * FIS (Fidelity National Information Services)

### Summary

Our project begins by using yfinance to collect 5 years of closing price data from each stock within our chosen Fintech sectors. We then reformat the data to produce the daily returns needed to run the majority of our calculations. 

![DataFrame that holds the daily returns of each stock in the Paytech sector](/Resources/Images/paytech-daily-df.png)
![Line plot showing the daily returns of PYPL](/Resources/Images/paytech_daily_plot.png)

Then we calculate metrics such as the cumulative returns, rolling 21-day averages and standard deviations, betas, and sharpe ratios. Each metric is visualized to better see how each stock or sector compares to each other. 

![Composite line plot of cumulative returns for all stocks](/Resources/Images/all-sectors-cumulative-returns.png)
![Composite bar plot of sharpe ratios for all stocks](/Resources/Images/all-sectors-sharpe-ratios.png)

Next we run 5-year and 1-year prediction Monte Carlo simulations where for each prediction length we run even and uneven weight distributed simulations for each sector. The uneven weight distributions are a 50%, 30%, 20% split where each stock within the sector is weighted based on its Sharpe ratio. With the results from the Monte Carlo simulation we describe the 95% confidence intervals assuming we start with a portfolio value of $10,000

![Resulting line plot of the cumulative returns predicted by the evenly weighted Monte Carlo simulation for Paytech](/Resources/Images/mc-even-weight.png)
![95 percent confidence intervals based on the Monte Carlo prediction results](/Resources/Images/mc-confidence-interval.png)

Finally, with the insights we gained from the calculations, we create a custom portfolio made up of the highest Sharpe ratio stocks from all sectors. We then run similar calculations by averaging the daily returns of all stocks to get the portfolio's daily returns for 5 years. With the daily returns we calculate annualized metrics and run Monte Carlo simulations to give predictions of how the portfolio might do in 1 or 5 years, again by looking at the 95% confidence intervals for each prediction with different weight distribution. 

![Annualized average return and cumulative returns for custom portfolio](/Resources/Images/custom-portfolio-annualized.png)

---

## Technologies

This is a Python 3.7 project ran using a JupyterLab in a conda dev environment. 

The following dependencies are used: 
1. [Jupyter](https://jupyter.org/) - Running code 
2. [Conda](https://github.com/conda/conda) (4.13.0) - Dev environment
3. [Pandas](https://github.com/pandas-dev/pandas) (1.3.5) - Data analysis
4. [Matplotlib](https://github.com/matplotlib/matplotlib) (3.5.1) - Data visualization
5. [Numpy](https://numpy.org/) (1.21.5) - Data calculations + Pandas support
6. [hvPlot](https://hvplot.holoviz.org/index.html) (0.8.1) - Interactive Pandas plots 
7. [holoviews](https://holoviews.org/) (1.15.2+) - **REQUIRED VERSION** Interactive Pandas plots; will cause error without proper version
8. [Alpaca Trade API](https://alpaca.markets/docs/trading/) (2.3.0) - Required for Monte Carlo simulations
9. [yfinance](https://pypi.org/project/yfinance/) (0.1.87) - Data collection
10. [nbdime](https://nbdime.readthedocs.io/en/latest/) (3.1.1) - Fixing merge conflicts in Jupyter notebooks

---

## Installation Guide

If you would like to run the program in JupyterLab, install the [Anaconda](https://www.anaconda.com/products/distribution) distribution and run `jupyter lab` in a conda dev environment.

To ensure that your notebook runs properly you can use the [requirements.txt](/Resources/requirements.txt) file to create an exact copy of the conda dev environment used to create the notebook. 

Create a copy of the conda dev environment with `conda create --name myenv --file requirements.txt`

Then install the requirements with `conda install --name myenv --file requirements.txt`

---

## Usage

The Jupyter notebook [fintech-sector-portfolio-analysis.ipynb](/fintech-sector-portfolio-analysis.ipynb) will provide all steps of the data collection, preparation, and analysis. Data visualizations are shown inline and accompanying analysis responses are provided.

Note that the data collection and the Monte Carlo simulations change every time that the notebook is ran. The data collection gets data 5 years from the date ran and the Monte Carlo simulations use that data to produce randomized results to predict what the portfolio performance could look like based on that data. 

The data collected and shown in the examples were from the time that this project was started - November 2022. 

Our presentation slides for this project are in the Resources folder: [Fintech-Sector_Analysis-Presentation](/Resources/Fintech-Sector-Analysis-Presentation.pptx)

---

## Contributors

[Ethan Silvas](https://github.com/ethansilvas) <br>
[Naomy Velasco](https://github.com/naomynaomy) <br>
[Karim Bouzina](https://github.com/karim985) <br>
[Jeff Crabill](https://github.com/jeffreycrabill) <br>

---

## License

This project uses the [GNU General Public License](https://choosealicense.com/licenses/gpl-3.0/)
