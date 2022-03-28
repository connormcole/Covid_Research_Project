# Covid Research Project


# Topic 
Covid 19 has affected the whole world for the last 2 years. The US has tried many different methods in order to combat the number of cases in order to minimize the number of deaths. We want to take a look at whether or not mask mandates placed by the state have had an affect on the number of cases, and if we can predict a spike in the number of cases based on past data. 

# Data Source 
* https://covidactnow.org/data-api
* https://www.littler.com/publication-press/publication/facing-your-face-mask-duties-list-statewide-orders
The Covid Act now Api gives us data about the number of cases, deaths, ang hospitilization rate, etc. And the littler graph gives us information on state mask mandates. 

# Communication 
We will be communicating via Zoom and group chats.

# Technologies used 

## Data Cleaning and Analysis
Pandas will be used on Jupyter Notebook to clean and extract our data. We will also use them for exploratory analysis and predictions. We will be be using Covid API data from: https://covidactnow.org/data-api and creating a csv of mask mandates from: https://www.littler.com/publication-press/publication/facing-your-face-mask-duties-list-statewide-orders.


## Database Storage 
After cleaning the data, we will connect AWS RDS to a local PostgresSQL server using SQLAlchemy, joining the data with a Postgres query and connecting Postgres to our Machine Learning Model.

## Machine learning
We will be using a regression supervised learning by using positive test data and link each state with their mandate laws, in order to try and predict future spikes in covid cases. 

## Dashboard 
We will be using tableau to create an interactive map, and some graphs that display our data. 


[Project Slides](https://docs.google.com/presentation/d/1iJsyCX3Ue4k_nVe7nkrCchj5CML6APWzz7dHxmCkNDc/edit?usp=sharing)
