# Chicago-Restaurant-Clustering

• The project explores restaurants in Chicago and clusters them based on their location. This helps to classify the city into different zones (neighborhoods) and compare metrics such as average rating, average risk and the size of the clusters.<br>
• The project is aimed to help customers or tourists in Chicago find the most dominant area for a specified cuisine to dine out.<br>
• It can also act as an aid to new restaurateurs to explore the city to find localities where their restaurant is likely to be profitable. This is done by further analyzing the clusters to obtain information that can help identify areas with high competition or low interest for a particular cuisine.<br>
• Extracted and collected data from Yelp Fusion API, Google Maps API, and the Chicago Food Inspection Dataset.<br>
• Integrated all the datasets using similarity matching and cleaned all the datasets to produce the final dataset.<br>
• Performed EDA to visualize the trends in the data and understand it better.<br>
• Trained and tested various clustering models like K-Means, DBSCAN, HDBSCAN, OPTICS, to cluster the restaurants based on geospatial data (geographical coordinates).<br>
• Assigned a neighborhood to each cluster and performed Analyzed the clusters to suggest clusters to users based on food preferences, or potential restaurateurs planning to open a new restaurant in Chicago, based on cuisine, competition, business failure rate, etc.<br>

The project contains the following Jupyter notebooks:<br>
1. Yelp_API_Extractor.ipynb<br>
2. Similarity_Matching.ipynb<br>
3. Dataset_Merging.ipynb<br>
4. EDA_Clustering_Visualization.ipynb<br>


If you need to run the entire project code, please make sure to run the notebooks sequentially in the order mentioned above.<br>


The details of each Jupyter notebook has been mentioned below:<br>
1. Yelp_API_Extractor.ipynb:<br>
This notebook reads the data from the Chicago food inspection dataset and uses that data to fetch the additional details of those restaurants from Yelp API. The data fetched from Yelp API is then stored in two JSON files, yelp.json and restaurant.json. yelp.json stores the business IDs of the restaurants, which are then used to fetch additional data from the API, and the results are stored in restaurant.json. The names of unique restaurants and addresses are also found from the Chicago food inspection dataset and that data is stored in ChicagoRestaurantsAndAddress.csv file.<br>


2. Similarity_Matching.ipynb:<br>
This notebook reads the data from ChicagoRestaurantsAndAddress.csv and restaurant.json, and then performs string similarity matching between the restaurant names and addresses from both the data files. The output is stored in the finaldataframe_fuzzy_alliterations.csv file.<br>


3. Dataset_Merging.ipynb:<br>
This notebook reads data from finaldataframe_fuzzy_alliterations.csv file and merges the Chicago food inspection and restaurant.json datasets, to create a final merged dataset, which is stored in “Both dataset merged.csv”.<br>


4. Analysis_Clustering_Visualization.ipynb:<br>
This notebook reads data from “Both dataset merged.csv” and performs EDA analysis, KMeans clustering, neighbourhoods fetching from google API, cluster plotting on folium and cluster analysis. This is the final result of our project.<br>

<b>Note: All the .csv and .json files are data files. The 'Food_Inspections.csv' is missing since it exceeds GitHub's maximum upload size limit. You can download it using the link for the Chicago Food Inspection Daaset mentioned in the Project Report file titled 'Final Report.pdf'.</b>
