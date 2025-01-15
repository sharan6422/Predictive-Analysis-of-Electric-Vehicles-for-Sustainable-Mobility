#Abstract
The transition to electric vehicles (EVs) represents a pivotal shift in the automotive industry,
 driven by environmental concerns and advances in technology. This dissertation presents a
 comprehensive predictive analysis of EV adoption and performance, addressing the growing
 significance of EVs in the context of sustainable transportation. The primary objective of this
 study is to forecast key trends in EV usage happening in the US and connect them to the
 change in the air quality in the US through a systematic review of existing literature and an in
depth exploration of available data. This research also investigates the factors influencing EV
 adoption, from government policies and consumer preferences to economic considerations.
 By employing a judicious blend of statistical methods and data-driven models, the study aims
 to provide practical insights into the future of EVs, addressing questions of range anxiety,
 charging station accessibility, and its effects in the Air Quality Index.The findings of this
 study not only offer valuable perspectives for industry stakeholders and policymakers but
 also contribute to the broader discourse on sustainable transportation solutions. After the
 research, the results showed that the dependency of air quality index on electric vehicles
 is less compared to other factors which may contribute to the pollution. The dissertation
 concludes with a reflection on the limitations of the analysis and prospects for future research
 in this evolving field. In essence, this research seeks to illuminate the path towards a more
 sustainable and electrified future in the realm of transportation

  The previous works on electric vehicles predominantly focused on investigating on a more
 environment friendly and efficient approach for transportation. The aspects, advantages and
 disadvantages of different types of electrical vehicles like HEV, plug in EV, fuel cell, bio cell
 etc were investigated. The revolution of the industry has also enables pioneering changes to
 the industry. There has been a push to encourage mass production of electric vehicles even
 though it was never done in history.
 Pevec et al., (2019) elaborates about the rising popularity of electric vehicles in a data
 science perspective. The paper discusses about the socio-economic point-of-view of electric
 vehicle transition. The current advancements in EV, the environmental impact it creates and
 it’s economic point of view contributes to the increasing popularity of the electric vehicles.
 Economic factors are important in analysing the growth of electric vehicles, the prices of
 and maintenance cost of different electric vehicles in comparison to the traditional internal
 combustion engine contributes a lot to the electric vehicle transition. The authors have taken
 their data from kaggle, alternate fuels vehicle data, EV volumes and data.gov. The parameters
 affecting the acceptance of electric vehicles includes the availability of charging stations,
 electricity cost, long charging time etc. The discussion and conclusion briefs the finding of the paper. The machine learning algorithms used in the paper were XGboost and clustering. And
 optimization was done using greedy and genetic algorithms. The reduced number of data
 driven analysis of electric vehicles were solved using this paper. The government incentives
 and conjoint analysis of factors which may be a concern to the electric vehicle customers
 can tackle the anxiety of electric vehicle adoption.

Evaluation Metric
 1. Accuracy Accuracy is the most widely used evaluation metric in classification tasks. The
 overall correctness of the model can be understood by accuracy. Accuracy is simply
 the ratio of correctly predicted instances to the total number of instances. Accuracy
 can be use as sole evaluation metric if the classes are balanced. Many Libraries and
 framework use accuracy as the default metric for classification problems
 2. F1 Score F1 score is a practical method in evaluating the model. This is because F1
 scores combines the precision and recall into a single value. F1 scores are widely used
 in cases when the false positives and false negatives are important considerations. It
 is also used when the dataset is imbalanced.
 3. Area under AUC-ROC AUC-ROC curve evaluates the model performance in all possible
 classification thresholds. A detailed view of model’s efficiency in classifying the positive
 and negative classes is done by AUC-ROC. AUC-ROC is not affected much by class
imbalance. In the cases where the class imbalance is high, AUC-ROC curve is used
 instead of accuracy or precision

Dataset Selection
 The selection of dataset involved researching extensively through the available websites.
 The dataset should fullfill all my requirements as well as have a fair grade of usability.
 With rising environmental concerns and governments around the world taking up a mission
 to reduce the carbon emissions, electric vehicle dataset was a clear choice. Later it was
 decided to use two different dataset and examining both to obtain a clear conclusion. The
 electric vehicle dataset was downloaded from gov.data. The dataset contained the Battery
 Electriv Vehicles(BEV) and Plug-in Hybrid Electric Vehicle (PHEVs) that are currently registered
 through Washington State Department of Licensing. The Air Quality Index (AQI) dataset was
 downloaded from United States Environmental Protection Agency where the monitored AQI
 is stored. The main objective of the study was to find out the effect of electric vehicle in the
 air quality index. Combining these dataset would help in achieving that

  The datasets used for the research are secondary datasets which is available to public.
 The historical data of the electric vehicle population is important to analyze and predict the
 future of the variable. This is then combined with the air quality index dataset to find the
 environment impact of the electric vehicle population.
 Table 5.1 enlists the columns in the electric vehicle dataset. The electric vehicle dataset
 has 17 columns and 130444 rows. The dataset has seven string type columns, five numeric
 columns, two categorical column and two alpha numeric columns.
 Table 5.2 enlists the columns in the AQI dataset. The air quality index databases are a
 group of six datasets each giving the information about daily AQI values in different counties
 in the USA. All datasets have 10 columns and 330623 rows. The dataset has four string type
 columns, two numeric, two categoric and one date type column.
 The figure 5.1 shows the boxplot graph which shows the median value of the model year
 with respect to the CAFV eligibility and EV type. The median sales rate gives us an idea
 about the highest sales time of the year. And understanding the vehicle type gives us a
 perspective about the consumer preference of EV. The AQI variation graph, figure 5.2, helps
 us understand the years and counties where the AQI has been high. We can understand the
 variations in graph where the EV adoption rate has been high.

Sampling strategy
 The electric vehicle population data’s training data is resampled to solve the class imbalance.
 The data is first split into training and testing data using the train-test-split function from
 scikit-learn. We use ’stratify’ parameter to make sure that the class distribution is maintained
 in training and testing data. The class distribution is then checked using the .value-counts()
 function. The nearmiss algorithm is used for undersampling the data. This procedure is done
 to solve imbalanced datasets by reducing the number of instances from over represented
 classes to balance the distribution. The class distribution in training sets is printed to confirm
 the resampling process.

EDA
 DataOverview:Thecodeinitiallyprovidesanoverviewof thedata, includingthenumberof
 records,features,anddatatypes. Itisimportanttounderstandthestructureandcharacterstics
 of thedataset. Geographical representationof thedata isalsodone. Thisenablesus to
 understandthepatterns, relationshipbetweenfeaturesandpotentialoutliers.
 DescriptiveStatistics: Thedescriptivestatistics, suchasmean,medianandrange, fornu
merical features iscalculated.Forencoding, thefrequencyofcategorical tableisnecessary.
 25
Number of instances, features and unique value is found out for better understanding of the
 code. The number of null values and NaNs are also calculated.
 Data Visualization: Data visualizations techniques, such as histograms, boxplots, and scatter
 plots are generated to explore the distribution of features, identify potential outliers, and
 uncover relationships between variables. The population difference of electric vehicles in
 different counties, electric vehicle type, AQI variation in different counties etc are plotted
 using matplotlib, seaborn and tableau

 Data Preparation
 Data preparation involved in modifying the features of the dataset to work in the machine
 learning algorithm.
 Data loading
 pd.read-csv function from pandas library is used to load the csv file to the dataframe. The
 same method was used to load the AQI data to the dataframe.
 Data Cleaning
 1. Missing values were dropped using ’.dropna’ method. The number of missing values
 were insignificant in comparison to the volume of data. So dropping the values will not
 affect the dataset in any way.
 2. Data filtering is done to extract columns based on specific conditions. By doing this we
 would be able to get the relevant data and effectively exclude the outliers. The outliers
 were also handled by removing values which has a high deviation from the average.
 3. encoding categorical values are done to make sure the machine learning models have
 a numeric input. Label encoding methods were used to encode the state names and
 electric vehicle types

 The electric vehicle population dataset and the Air Quality Index dataset was analyzed and
 examined. The findings are given below. The electric vehicle database was loaded, cleaned
 and analyzed. The missing values were imputed to make the data fit for the machine learn
ing models. univariate and Bivariate plots of the dataset was created. Along with matplotlib
 graphs which helped in visualization and exploration of the data. We understand the number
 of electric vehicles in king county was significantly higher than the others and the clean en
ergy fuel vehicle eligibility was satisfied by less than 50 percent of the total electric vehicles.
 Heatmap of feature correlation was obtained. Pairplot was generated using the important
 features. Encoding of the states and the electric vehicle type were also performed. We
 understand that BEV constitues to 76.8 percent of the total electric vehicle population and
 PHEV constitues to 23.2 percent. The training and testing data was created to make the ma
chine learning models. Four machine learning algorithms were used to create the model.
 The algorithsm were naive bayes, random forest, XGboost and Logical regression. Hyper
parameter tuning and AUC-ROC curves were used as performance metrics. The classification
 report and confusion matrix of all models were generated. The model with the best accuracy
 was selected to predict the future electric vehicle population.
 The Air Quality Index database was on a yearly basis. The datasets of 2015, 2016, 2017,
 2018, 1029 and 2020 were merged together to create a single dataframe. The states outside
 of the united states were eliminated using the ’isin’ method. The states were divided into good,
 
moderate and bad categories. Column distribution of the data was plotted using matplot lib.
 The number of ’unhealthy’ AQI days is significantly higher than the ’morderate’ and ’good’
 AQI days. The variation of AQI along the years was also plotted to understand the change
 in AQI with repect to the number of electric vehicles.There is noticable variation in the AQI
 value during the timeframe of 2015-2020. We can observe a steady growth and fall of AQI
 values in no particular pattern. The electric vehicle dataframe and the AQI dataframe was
 merged to find out the correlation of AQI and electric vehicle population.  The correlation value indicated a weak correlation between the electric vehicle population
 and AQI. This clearly shows that the affect of number of electric vehicles is less in comparison
 to other factors causing it. The causality from the reduction of air pollution of the vehicles
 has significantly less impact in comparison to other factors causing it.
 Figure 8.1 shows the confusion matrix of the random forest model with which the prediction
 is done. The percentage of true negative, true positive, false negative and false positive helps
 us in understanding the accuracy of the model. Confusion matrix classification works in a
 binary mode and all the evaluation metrics are calculated from it. The model bias towards
 any class could be understood from the confusion matrix. It is evident from the graph that the
 dataset we used did not have a high bias towards any class. Figure 8.2 shows the Receiver
 Operating Characteristic Area Under the Curve where the x axis is the true positive rate and
 y axis is false positive rate. TRP and FPR are calculated as the ratio of true value and the
 sum of true and false values.
