# Covid Research Project

## Overview 
### Topic and Hypothesis 
There is plenty of argument in the US (and world) for and against mask mandate and vaccine mandate. Here we want to quantify if mask mandates, and COVID-19 vaccine are effective tools in fight against COVID-19. There are plenty of data available on mandates, vaccination rate, hospitalization, and covid related deaths. Here, our team will analyze following hypothesis. 


H01: Mask mandate does nothing to prevent COVID-19 transmission. __
HA1: Mask mandate does prevent COVID-19 transmission. __

H02.1: Vaccination does not prevent COVID-19 transmission.__

HA2.2: Vaccination helps prevent COVID-19 transmission. __

H02.2: Vaccination does not reduce hospitalization. __

HA2.2: Vaccination helps reduce hospitalization.__

H02.3: Vaccination does not reduce death rates.__

HA2.3: Vaccination does reduce death rates. __
 ### Data Sources 
The two sources we have picked are:__

HA2.2: Vaccination helps prevent COVID-19 transmission __

https://covidactnow.org/data-api  __

https://www.littler.com/publication-press/publication/facing-your-face-mask-duties-list-statewide-orders  __

The COVID act now data API contains information about all states' vaccination numbers. Ratio of vaccines to the population as well as number of vaccines administered. The team will create a database that would have information from above sources and run report sorted by states overall performance on different factors. __

We will be using data from March 01, 2021 to February 28, 2022 and analyze trend over a year. __

## Team and Roles 
There are four members in our team: 
##### Connor Cole: 
Conor is playing role of the square where he will be will be responsible for the repository.__

##### Adibayo Ajibosin 
Adibayo is playing role of the triangle who will create mockup of machine learning model.__
##### Hammad Rahman
Hammad is the circle of the team where he will be working with database and dataset  __
##### Aayam Shrestha 
Aayam is the X and in charge of technologies decisions. __
### Communication Protocol 
We are using following communication methods 
Slack is for note taking and communicating to team members and also providing minutes to people who missed the Zoom meetings. __
Zoom: Zoom is to hold meetings and share screens for live collaboration. The meetings are not recorded however minutes are posted on slack. __  
Github: Github is store work and so we can submit our work and combine branches. __
Phone and Text: If we need to communicate urgently and tell everyone something that cannot wait for them to be in front of a computer. __  

## Machine Learning Model 
Our model is to show __
(Y) Number of cases = (X) vaccines completed ratio to state population 

## Project Outline 
### ETL
#### Extract: 
We extractd data from multiple sources listed in data source and saved it to CSV format with the help of Jupyter notebook. The tools used in this stage was Pythin and Pandas. We used mainly Python and Pandas to drop irrelevant data and clean up dataframe till what we had was extracted datframe with relevant data. Then data was loaded into Postgres SQL hosted on AWS RDS. There were four input tables. __
            1. Main Table: This table was created by an API from littler.com which had most data about our four hypothesis. We extracted infection rate per day, new deaths per day, vaccination rate per state, and hospitalization rate per day. __
            ![Main Table](Images/Input_main.png) __
            2. Input mandate: This table has data on mask manadate by states by months. __
            ![Mandate](Images/input_mandate.png)
            3. Input Population: This table has population by states. __
            ![Population](Images/input_population.png) 
            4. Input State_id: One of our table has state abbrivation while others has state name. Therefore, we added a table to translate state name in to state code (example Alska to AK). __
            ![State_ID](Images/inputState_ID.png)  
#### Tranform: 
Then data was tranformed to fit into four tranformed tables that helps tranform into tables that could be analyzed by machine learning and Tableau. __
            1. Mask mandate: This table has State_id, date, infection_rate, and mask requirements. The purpose poupose of this table is to analyze H01: Mask mandate does nothing to prevent COVID-19 transmission.__
            ![Mask Mandate](Images/output_masks_mandate.png)
            2. Infection Rate: This table has State_id, date, new_cases, vaccination_ratio, and state population. The purpose of this table was to analyze H0: Vaccination does not prevent COVID-19 transmission.__
            ![Infection](Images/output_infection_rate.png)
            3. Hospitalization: This table has State_id, date, number of hospital beds occupied, vaccination_ratio, and state population. The purpose of this table was to analyze H0: Vaccination does not prevent COVID-19 hospitalization.__
            ![Hospitalization](Images/output_hospital_beds.png)
            4.New Deaths: his table has State_id, date, number of deaths per day, vaccination_ratio, and state population. The purpose of this table was to analyze H0: Vaccination does not prevent COVID-19 deaths.__
            ![Deaths](Images/new_deaths.png)
Furthermore, these output tables were converted into CSV and using excel further tranform to grouped data firest by state then by months and uploaded to tableau to be nalyzed. The original CSV were also used in machine learning to be analyzed. Results are below.  


## Results. 
### Tableau
Tableau dashboared can be found below.
[Covid_Data_Dashboared](<div class='tableauPlaceholder' id='viz1649734294266' style='position: relative'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;XZ&#47;XZ9DDYX2W&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='path' value='shared&#47;XZ9DDYX2W' /> <param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;XZ&#47;XZ9DDYX2W&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1649734294266');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.minWidth='1120px';vizElement.style.maxWidth='3320px';vizElement.style.width='100%';vizElement.style.minHeight='1087px';vizElement.style.maxHeight='2087px';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.minWidth='1120px';vizElement.style.maxWidth='3320px';vizElement.style.width='100%';vizElement.style.minHeight='1087px';vizElement.style.maxHeight='2087px';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else { vizElement.style.width='100%';vizElement.style.height='1827px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>)


