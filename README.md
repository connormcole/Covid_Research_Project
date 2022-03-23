# Covid Research Project


# Technologies used 

## Data Cleaning and Analysis
Pandas will be used on Jupyter Notebook to clean and extract our data. We will also use them for exploratory analysis and predictions. We will be be using Covid API data from: https://covidactnow.org/data-api and creating a csv of mask mandates from: https://www.littler.com/publication-press/publication/facing-your-face-mask-duties-list-statewide-orders.


## Database Storage 
After cleaning the data, we will connect AWS RDS to a local PostgresSQL server using SQLAlchemy, joining the data with a Postgres query and connecting Postgres to our Machine Learning Model.

## Machine learning
We will be using a regression supervised learning by using positive test data and link each state with their mandate laws, in order to try and predict future spikes in covid cases. We will use the sklearn.linear_model, and LinearRegression tools. 

## Dashboard 
We will be using the D3.js dashboard to create an interactive and fun dashboard.  
