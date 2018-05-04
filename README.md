## Deep Neural Networks on NYPD's  Stop-and-Frisk 
**Team:  Mahmoud Badi, Aman Preet Singh, and Rahul Khandalkar, Southern Methodist University 

**Goal and Business/Use Case**:  
We have utilized NYPDs Stop and Frisk dataset for our exercise and tried to implement different DNN architectures to predict arrests. 
In our dataset (2012), New Yorkers were stopped by the police 532,911 times:
- 473,644 were totally innocent (89 percent).
- 284,229 were black (55 percent).
- 165,140 were Latino (32 percent).
- 50,366 were white (10 percent).

## *Dataset:*
http://www.nyc.gov/html/nypd/downloads/zip/analysis_and_planning/2012_sqf_csv.zip

## *Dataset Description:*
http://www.nyc.gov/html/nypd/downloads/zip/analysis_and_planning/2012_sqf.zip

In order to understand the information captured in the csv file, we took a look at the specs document that helps us identify the various features recorded in our dataset.
Our goal is to build a classification algorithm that can predict arrests efficiently so that they can be implemented on other states or other country's law enforcement databases. This will not only help reduce the number of inmates in prisons and save tax payer's money but also decrease the public frustration rate/anger and improve's the law enforcement's credibility.
We found that people of African or Hispanic descent were stopped more frequently than whites. This is due to the fact that humans make decisions based on their own experiences with people from different races, ages, shapes, and other characterisitics. We've also tried to find a correlation between the arrests made, age, and race.
Using a strong classification algorithm will allow a law enforcement agency to negate the possibility of making mistakes, give them a second non-judgemental point of view, and reduce the unprofessionalism of police by a high extent.
### Defining and Preparing Our Variables 

Our Dataset came with 112 features. Due to the massive size of this datasete  and the computational needs to accomodate such big dataset, we performed this lab only on a fraction of these  features which we believe are important and came up with results that backup the claims of the police being unprofessional and biased in their judgments and arrests. 

The part where we do visualization is not included here, since it will be a replica of what we did in the previous lab. If the reader is interested in seeing if actually the police of NYC were biased and unprofessional, this is proved in our visualization part in the previous lab. 

We shortlisted and included the following features in this Deep Neural Network project:

* **perobs**: Period of Observation
* **rf_attir**: reason for frisk: inappropirate attire for season 
* **offunif**: Was officer in uniform? 
* **inout**: WAS STOP INSIDE OR OUTSIDE ?
* **perstop**: PERIOD OF STOP (MMM)
* **arstmade**: WAS AN ARREST MADE ?
* **frisked**: WAS SUSPECT FRISKED ?
* **searched**: WAS SUSPECT SEARCHED ?
* **contrabin**: WAS CONTRABAND FOUND ON SUSPECT ?
* **pistol**: WAS A PISTOL FOUND ON SUSPECT ?
* **race**: SUSPECT'S RACE
* **sex**: SUSPECT'S SEX
* **age**: SUSPECT'S AGE 

**Some Preprocessing Operations**:

* We've converted all Yes and No values to 1s and 0s.
* We also performed one-hot encoding on *sex* and *race* and had all of these one-hot-encoded values saved into columns.
* Removed all of the NaNs.
* Concatenated all of the feature columns into one X_all variable that has all of our features.
* We didn't implement PCA here, because when we tried implementing it on these features, it wasn't able to seperate.

**The final dataset will be in X_all where all of the engineered features will be stored** 

**We will comment on each pre-processing step just to make it clear**
