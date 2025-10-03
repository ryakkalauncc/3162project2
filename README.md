# Global Crocodile Species Prediction
<H2>Introduction to the Problem</H2>
<b>I am using the Global Crocodile Species Dataset from Kaggle. This dataset provides detailed information on all recognized crocodile species across the globe. It includes taxonomic classification, geographic distribution, habitat details, population estimates, and conservation statuses. The dataset provides both biological and ecological attributes to compare with. With some of the features of this dataset in mind, I want to predict the species of a crocodile based on the length, weight, habitat, location, and few other characteristics. I am considering using random forest becuase my dataset is moderate sized, random forest can handle numerical and categorical data and can capture non-linear relationships.</b>
<h2>Pre-processing the Data</h2>
<b>
I plan on handling missing and unknown data in the sex column with NaN and dropping irrelevant columns such as Observation ID, Observer Name and Notes, and Date of Observation. I also drop rows with missing values. From there I'll choose a target variable. My target variable is "Common Name" and I continue by defining features x and target y. Finally, in order to ensure a clean numeric dataset for modeling, I identified categorical columns in X. I used one-hot encoding to turn them into numeric features, and used drop_first = True to avoid the dummy variable trap.
</b>
<h2>Data Understanding/Visualization</h2>
<b>I began by exploring the dataset and variables that might help with prediction (df.head(), df.info(), df.describe()). I used value_counts() for categorical columns to check class balance. I created the histograms and boxplots for numeric variables to inspect distributions and outliers. I created the countplots/barcharts for categorical distributions and for target calss balance. I created the boxplots and violin plots of Length and Weight by Common Name to visualize overlap between species. Finally, the correlation heatmap was created for numeric features to detect multicollinearity and find strong numeric associations. What I learned from the visualizations is how a few species dominate the dataset while several species have relatively few obeservations and kept this in mind for modeling and evaluation. I found overlap in length and weight distributions across multiple species, indicating that morphology alone may be insufficient for classification. Species are often associated with particular habitat types and regions. My visuals helped clarify the need to group rare countries or use stratify = in splits to preserve class balance. My evaluation plan shifted as to using class precision/recall/F1 and macro/weighted F1. Confusion matrices are also essential to show which species get confused. </b>
<h2>Modeling</h2>
<b>My primary model is Random Forest, the baseline alternatives considered were SVM/KNN however they are less convenient with many categorical features and require scaling. I used RandomizedSearchCV to tune n_estimators, max_depth, max_features, min_samples_split, and min_samples_leaf. Randomized search is a good trade-off for exploration in moderate size search.</b>
<h2>Evaluation</h2>
<b></b>
<h2>Storytelling/Findings</h2>
<b>  </b>
<h2>Impact</h2>
<b> </b>
<h2>References</h2>
<b>https://www.kaggle.com/datasets/zadafiyabhrami/global-crocodile-species-dataset</b>
