# Why do we have price fluctuations when booking an Airbnb?

- <a href= "https://www.kaggle.com/code/joeyzijiantan/analysis-on-airbnb-seattle/data" > Kaggle data </a> 
- <a href= "https://medium.com/@mukunzialex47/inside-airbnb-data-7b7b1340c012" >Blog post on medium </a> 


<b> Main focus</b>

<ol>
<li>Get the busiest times of the year to visit Seattle and By how much do prices spike </li> 
<li> Get the vibe of each Seattle neighbourhood using listing descriptions </li>
<li> Segment  location are you possibly going to spend more for an Airbnb </li>
<li> <a href= "https://medium.com/@mukunzialex47/inside-airbnb-data-7b7b1340c012" > Blog post(medium)</a> </li>

</ol>

<h3><b>Libraries used .</h3></b>

<code>Wordcloud version: 1.8.2.2</code> <br>
<code>Numpy version: 1.21.6.</code> <br>
<code>scikit-learn version: 1.0.2.</code> <br>
<code>Pandas version: 1.3.5.</code> <br>
<code>Matplotlib version: 3.2.2.</code> <br>
  
  <h3>Install requirements </h3>
  <code> pip install -r requirements.txt</code> <br>

  <h3> File description </h3> 
  - analysis-on-airbnb-seattle.ipynb: <i> Notebook containing the analysis data</i> <br>
  <span>- airbnb data/reviews.csv : reviews data</span><br>
  <span>- airbnb data/listings.csv : listings data</span><br>
  <span>- airbnb data/calendar.csv : calendar data</span>

  ### Structure
  ```

  udacity-datascience-nanodegree/
├── airbnb data/
│   ├── calendar.csv
│   ├── listings.csv
│   └── reviews.csv
├── analysis_on_airbnb_seattle.ipynb
├── Disaster_Response/
│   ├── app/
│   │   ├── run.py
│   │   └── templates/
│   │       ├── go.html
│   │       └── master.html
│   ├── data/
│   │   ├── disaster_categories.csv
│   │   ├── disaster_messages.csv
│   │   └── process_data.py
│   ├── ETL Pipeline Preparation.ipynb
│   ├── images/
│   │   ├── screenshot1.png
│   │   ├── screenshot3.png
│   │   └── sreenshot2.png
│   ├── ML Pipeline Preparation.ipynb
│   ├── models/
│   │   └── train_classifier.py
│   └── README.md
├── Ibm-recommndations/
│   ├── __pycache__/
│   │   └── project_tests.cpython-310.pyc
│   ├── data/
│   │   ├── articles_community.csv
│   │   └── user-item-interactions.csv
│   ├── debug.log
│   ├── IBM__recommendations.ipynb
│   ├── project_tests.py
│   ├── README.md
│   ├── Recommendations_with_IBM.html
│   ├── top_10.p
│   ├── top_20.p
│   ├── top_5.p
│   └── user_item_matrix.p
├── README.md
├── requirements.txt
└── Starbucks-Capstone-Challenge/
    ├── data/
    │   ├── portfolio.json
    │   ├── profile.json
    │   └── transcript.json
    ├── pic1.png
    ├── pic2.png
    ├── README.md
    ├── Starbucks_Capstone_notebook.html
    └── Starbucks_Capstone_notebook.ipynb
```
<h3> Executive summary(Insights) </h3> 
<ul> <li>The average price for the summer holiday (June, July, and August) is higher than the other period of the whole year. The orange line represents the median value of price in that specific month</li>
<li>We can conclude that the summer holiday period(June, July, August) and January have fewer available listings than the rest months of the year. Probably, customers have made the reservation in advance.</li>
<li> Monday has more available listings than the rest of the week. For the average price, the average price for weekends (Friday & Saturday) is higher than the weekdays.</li>
<li>The number of accommodations, the number of bedrooms & beds, and cleaning fees have a significant effect on raising the listing price. Meanwhile, it seems the monthly number of reviews has a weak, negative correlation with the listing price.</li>

  
&nbsp;
&nbsp;
<h3><b>Licensing, Authors, and acknowledgements</h3><b>

Data source- <a href= "https://www.kaggle.com/code/joeyzijiantan/analysis-on-airbnb-seattle/data"> Kaggle data </a> <br>
<h6> acknowledgements <br>
  <a href= "https://www.kaggle.com/airbnb" > Airbnb (Owner) </a> </h6>
 

