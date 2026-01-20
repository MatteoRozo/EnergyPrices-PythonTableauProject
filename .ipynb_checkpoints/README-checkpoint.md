# Colombian Energy Market - Stock vs Secondary Market Dashboards

![Dash GIF](Images/DashboardIntro.gif)

## Introduction
This Energy Market Price Analysis Tableau dashboard was developed to understand how the spot market prices and secondary market prices in Colombia have evolved, and to evaluate whether there are potential gains from participating in either of the two markets.

This dataset, available from the Sinergox platform of XM (https://sinergox.xm.com.co/Paginas/Home.aspx), contains all market transactions for the year 2025. It features a wide range of variables, such as market prices, plant capacity, plant generation, and demand forecasts, among others.

## Key questions
This dashboard seeks to answer the following questions surrounding the dynamics of Colombia’s energy markets:

- ¿What's the evolution of prices between the spot market and the secondary market?

- ¿Do companies have incentives to participate in the secondary market compared to the spot market?

- ¿Which types of plants (by energy source) benefit the most from participating in the secondary market?

## Methodology

This dashboard was built in two steps.

**Step 1: Database Exploration in Python**  
The first step involved exploring the database using Python, as documented in the Jupyter Notebook. The goal was to reshape, organize and merge the data through operations such as **melts**, **pivots**, and **filters** across different tables. Libraries such as **pandas** and **numpy** were employed to handle data transformations, ensure consistency, and prepare the dataset for further analysis. This stage focused on structuring the information to highlight key variables such as **market prices, secondary market prices, generation, and plant characteristics**.

**Two notes:**
- This initial analysis can be found in the Jupyter Notebook within the *Data_Exploration* folder.  
- It is important to note that this exercise does not use or demonstrate **causal** or **predictive interpretation methodologies**. Therefore, the insights derived are purely **descriptive** of the analyzed sample.  

**Step 2: Trend Analysis and Visualization in Tableau**  
The second step was to conduct trend analysis and present the results through **Tableau dashboards**. Tableau was used to generate interactive visualizations that allowed for a clearer understanding of how **spot market prices** and **secondary market prices** evolved over time, as well as how **profitability indicators** behaved across different plant types.  

Since this exercise was not focused on modifying the original dataset, no **missing values** or **complex data typologies** were introduced.

## Graphs

### Hourly Prices - Line Chart  
This line chart shows hourly prices by market type and month.

![Detail 1](Images/Graph-HourlyPrices.png)

### Daily Difference in Prices - Line Chart  
This line chart shows average daily difference in price by month.

![Detail 2](Images/Graph-DailyDifference.png)

### Hourly Profit - Line Chart  
This line chart shows hourly profits by plant type and month.

![Detail 3](Images/Graph-HourlyProfits.png)

### Daily Difference in Profit - Line Chart  
This line chart shows average daily difference in profit by month.

![Detail 4](Images/Graph-DailyDifferenceProfit.png)

## KPI Cards

### Profitability Indicator by Market 

This card presents the profitability indicator comparing the **spot market** and the **secondary market**. The indicator is defined as:
\[ \pi = \big( P_{\text{sale}} - P_{\text{bid}}^{MC} \big) \cdot \text{Generation} \] 

**Assumptions:** 
- The **offer price** (\(P_{\text{bid}}^{MC}\)) is assumed to be equal to the **marginal cost**, given the competitive nature of the market. 
- \(P_{\text{sale}}\) represents the spot market price or secondary market price (COP/kWh). 
- **Generation** is measured in kWh.
- The result \(\pi\) is expressed in COP, representing the potential gain from participating in the spot market relative to the secondary market.
-
### Profitability by Plant Type (Energy Source) 
This card shows which types of plants (e.g., hydro, thermal) benefit the most from participating in the secondary market. By applying the profitability indicator across different plant sources, we can identify which technologies capture higher margins and whether incentives exist to favor the secondary market over the spot market.

![KPI 1](Images/KPI-Profits.png)

## Widgets and Others

### Data Validation, Filtered List and Sheet Protections  
To ensure the tool is easy to use and free from erroneous user manipulations, slicers with validators and filtered lists were created and organized. 


## Formulas and Functions
### Dashboard Formulas and Functions


## Key Insights

- Without discounts on purchases and using **flexible** payment methods (cash or digital wallet), Walmart consumers with median/low loyalty levels (silver/bronze) tend to be the highest spenders. When banked payment methods are introduced, consumers with higher loyalty (platinum/gold) tend to spend more.

- At different levels of disaggregation, promotions with percentage discounts attract the most consumer spending, almost doubling the amounts observed in BOGO-type promotions.

- Discounts appear to have a greater effect on lower-loyalty customers when paying with cash or digital wallets. However, when analyzing those using banked payment methods, there is a spending gap between high-loyalty and low-loyalty consumers.

## Additional Dashboard

![Example 1](Images/Graph-Dashboard1.png)
