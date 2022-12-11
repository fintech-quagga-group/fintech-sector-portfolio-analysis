# Fintech Sector Portfolio Analysis 

This project is a portfolio analysis of different sectors within Fintech to better understand the growth, correlations, and profitability of Fintech companies. Through anaylzing different calculations such as finding the cumulative returns, 21-day rolling average and standard deviations, Sharpe ratios, and running Monte Carlo simulations, our analysis should provide insights into which sectors/stocks in Fintech would be good investments. 

Through our analysis we hope to answer the following questions: 
1. How does each Fintech sector, and the individual stocks within them, perform over time?
2. Which sectors and individual stocks are the best potential investments? 
3. What are the relationships or correlations between each sector? 
4. Based on what we learned about the sectors and stocks, if we were to come up with a Fintech portfolio what stocks would we choose?

#### Data Used
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

---

## Installation Guide

If you would like to run the program in JupyterLab, install the [Anaconda](https://www.anaconda.com/products/distribution) distribution and run `jupyter lab` in a conda dev environment.

---

## Usage



---

## Contributors

[Ethan Silvas](https://github.com/ethansilvas) <br>
[Naomy Velasco](https://github.com/naomynaomy) <br>
[Karim Bouzina](https://github.com/karim985) <br>
[Jeff Crabill](https://github.com/jeffreycrabill) <br>

---

## License

This project uses the [GNU General Public License](https://choosealicense.com/licenses/gpl-3.0/)
