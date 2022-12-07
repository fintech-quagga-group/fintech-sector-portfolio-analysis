# Fintech Sector Portfolio Analysis 

Project Goals: 
1. How each fintech sector/stock performs over time
2. Relationship between each sector (correlation)
3. Advice on which sectors and individual stocks could be potentially profitable
4. Based on what we learned about the sectors/stock, if we were to come up with a portfolio (almost like an ETF) what stocks would we choose?

Project Outline: 
- Get daily returns
- Data analysis and calculations
    - Daily return plots
    - Box plots
    - plot cumulative returns (probably move this above rolling stats)
    - plot 21-day rolling average and std
    - calc annualized average return, annualized std, then plot sharpe ratio (probably all stocks in one graph)
    - average (.mean(axis=1)) all the sectors and do the steps for “Diversify the portfolio”
        - when doing cov probably want to compare banking and lending to paytech
            - banking.rolling().cov(paytech)
            - lending.rolling().cov(paytech)
- Monte carlo simulations
    - Even weight (.33, .33, .33) 5 year prediction
    - (.5, .2, .3) 5 year
    - (.33, .33, .33) 1 year
    - (.5, .2, .3) 1 year
- Custom portfolio (last part for module 7 challenge + monte carlo)
    - average daily returns (.mean(axis=1))
    - annualized average daily returns
    - cumulative returns of average daily returns
    - plot cumulative returns
    - Monte carlo sims (TBD)

(Add description here)

(Add data section here)

(Add project summary here)

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
[]() <br>

---

## License

This project uses the [GNU General Public License](https://choosealicense.com/licenses/gpl-3.0/)
