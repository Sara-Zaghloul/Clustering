Problem Statement :

HELP International is an international humanitarian NGO that is committed to fighting poverty and providing the people of backward countries with basic amenities and relief during the time of disasters and natural calamities. HELP International have been able to raise around $ 10 million. This money now needs to be allocated strategically and effectively. Hence, inorder to decide the selection of the countries that are in the direst need of aid, data driven decisions are to be made. Thus, it becomes necessary to categorise the countries using socio-economic and health factors that determine the overall development of the country. Thus, based on these clusters of the countries depending on their conditions, funds will be allocated for assistance during the time of disasters and natural calamities. It is a clear cut case of unsupervised learning where we have to create clusters of the countries based on the different feature present.


The analysis aims to identify patterns in countries’ economic, health, and trade indicators to classify them into clusters:

- **Help Needed**
- **Might Need Help**
- **No Help Needed**
- **Noise / Outliers** (DBSCAN)

Clustering is performed using two approaches:

1. **Feature Combination**: Aggregating key indicators into `Health`, `Trade`, and `Finance` scores.  
2. **PCA Data**: Reducing dimensionality using Principal Component Analysis (PCA).


Data link (Kaggle):

https://www.kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data?resource=download


Dataset Attributes:
    
- country : Name of the country
- child_mort : Death of children under 5 years of age per 1000 live births
- exports : Exports of goods and services per capita. Given as %age of the GDP per capita
- health : Total health spending per capita. Given as %age of GDP per capita
- imports : Imports of goods and services per capita. Given as %age of the GDP per capita
- Income : Net income per person
- Inflation : The measurement of the annual growth rate of the Total GDP
- life_expec : The average number of years a new born child would live
- total_fer : The number of children that would be born to each woman
- gdpp : The GDP per capita. Calculated as the Total GDP divided by the total population.


3. Clustering: 

 a-K-Means :

    - Used Elbow Method and Silhouette Score to select k=3, which is standard.

    - After clustering, you correctly labeled clusters based on income & child_mort.

    - Choropleth maps visualize the clusters per country

 b-DBSCAN :

    - Used k-distance graph to select eps and min_samples.

    - Correctly handled outliers/noise (-1).

    - Resulted in slightly different cluster interpretations compared to K-Means.


 
