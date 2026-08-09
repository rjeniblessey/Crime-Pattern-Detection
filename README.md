# 🚨 Chicago Crime Pattern Detection Using K-Means Clustering

## 📌 Project Overview

**Chicago Crime Pattern Detection** is a machine learning project that uses **K-Means Clustering**, an unsupervised learning algorithm, to identify groups of crime incidents based on their geographical and time-related characteristics.

The project uses historical Chicago crime data to discover patterns in **where and when crimes occur**. The resulting clusters are analyzed to understand their crime characteristics and dominant crime types.

The project also provides a geographical visualization of the identified crime clusters using latitude and longitude.

---

## 🎯 Objectives

* Analyze historical crime data from Chicago.
* Clean and preprocess the crime dataset.
* Handle missing and invalid values.
* Handle missing geographical coordinates appropriately.
* Extract useful information from the crime date and time.
* Identify geographical and temporal crime patterns.
* Apply K-Means Clustering to group similar crime incidents.
* Use the Elbow Method to select a suitable number of clusters.
* Analyze the characteristics of each cluster.
* Identify the dominant crime types within each cluster.
* Visualize crime clusters geographically.

---

## 💡 Why This Project?

Crime datasets contain valuable information about **crime location, date, time, and crime type**.

Traditional data analysis can show individual crime statistics, but clustering can help discover groups of crime incidents that share similar characteristics.

This project can help answer questions such as:

* Where are similar crime incidents concentrated?
* During which time periods do crimes occur more frequently?
* What crime types dominate different clusters?
* How are crime incidents geographically distributed?
* What characteristics distinguish one crime cluster from another?

The project is intended for **exploratory crime pattern analysis** and is not a system for predicting individual future crimes.

---

## 📊 Dataset

The project uses a **Chicago Crime Dataset** containing historical crime records.

The dataset includes information such as:

* Date and time of crime
* Primary crime type
* Latitude
* Longitude
* Police district
* Ward
* Community area
* Arrest information
* Domestic crime information
* Location information

The dataset used in the project contains approximately **1.45 million crime records** before preprocessing.

---

## 🛠️ Technologies Used

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

### Development Environment

* Jupyter Notebook

### Machine Learning

* K-Means Clustering
* Elbow Method
* Silhouette Score using a sample for evaluation

---

## 🔄 Project Workflow

**1. Data Collection**

The Chicago crime dataset is loaded and examined.

**2. Data Exploration**

The dataset structure, data types, statistical information, and crime distributions are analyzed.

**3. Missing Value Analysis**

Missing values are identified for numerical and categorical columns.

**4. Missing Value Handling**

Numerical missing values are handled using median values, while latitude and longitude are treated separately because they represent geographical locations.

**5. Geographical Data Cleaning**

Records without valid latitude and longitude information are removed, and geographical coordinates are checked to ensure that the data represents the Chicago region.

**6. Date and Time Processing**

The crime date is converted into a proper date-time format, and useful temporal information such as year, month, day, hour, and day of the week is extracted.

**7. Feature Selection**

Geographical and temporal features are selected for clustering.

The main features used are:

* Latitude
* Longitude
* Hour
* Day of Week
* Month

**8. Feature Scaling**

The selected features are standardized because K-Means is a distance-based clustering algorithm.

**9. Selecting the Number of Clusters**

The Elbow Method is used to determine a suitable number of clusters.

**10. K-Means Clustering**

K-Means is applied to group similar crime incidents.

Four clusters are used in the current project implementation.

**11. Cluster Analysis**

Each cluster is analyzed based on:

* Number of crime incidents
* Top crime types
* Average latitude
* Average longitude
* Average crime occurrence hour

**12. Crime Type Analysis**

The most frequent crime types within each cluster are identified to understand the characteristics of the clusters.

**13. Visualization**

The clusters are displayed geographically using latitude and longitude to help understand the spatial distribution of crime incidents.

---

## 🔍 Cluster Results

The clustering process produces four groups:

| Cluster   | Dominant Crime Type |
| --------- | ------------------- |
| Cluster 0 | Other Offense       |
| Cluster 1 | Criminal Damage     |
| Cluster 2 | Battery             |
| Cluster 3 | Theft               |

These crime types represent the **most frequently occurring crime type within each cluster**.

A cluster does not contain only one type of crime. Each cluster can contain several different crime types, with the listed type being the dominant one.

> Cluster numbers are labels assigned by K-Means. They do not represent crime severity or ranking.

---

## 📈 Results and Analysis

The project identifies groups of crime incidents based primarily on:

* **Geographical location**
* **Crime occurrence hour**
* **Day of the week**
* **Month**

The clustering results allow the crime incidents to be grouped into four different patterns.

The dominant crime type analysis provides additional information about what types of crimes are more common within each cluster.

The geographical visualization helps show how these clusters are distributed across the Chicago area.

---

## 🗺️ Crime Cluster Visualization

The project uses a geographical scatter plot based on:

* Longitude on the X-axis
* Latitude on the Y-axis
* Cluster number represented using different colors

This visualization provides a simple way to observe the spatial distribution of the identified crime clusters.

---

## 📁 Project Structure

```text
Chicago-Crime-Pattern-Clustering/
│
├── Dataset/
│   └── Chicago_Crimes_Dataset.csv
│
├── Chicago_Crime_Pattern_Clustering.ipynb
│
├── README.md

---

## ⚙️ Installation

Clone the repository and install the required Python libraries.

### Required Libraries

* pandas
* numpy
* scikit-learn
* matplotlib
* seaborn
* jupyter

After installing the dependencies, open the Jupyter Notebook and run the project cells sequentially.

---

## ⚠️ Limitations

* K-Means requires a predefined number of clusters.
* Crime records without geographical coordinates cannot be used for geographical clustering.
* K-Means is distance-based and may not perfectly represent complex geographical crime patterns.
* Cluster numbers do not represent crime severity.
* The clusters represent patterns in historical crime data and should not be interpreted as predictions of future crimes.
* Results depend on the selected features and preprocessing methods.
* Reported crime data may not represent all crimes that actually occurred.

---

## 🚀 Future Enhancements

The project can be further improved by:

* Comparing K-Means with DBSCAN and other clustering algorithms.
* Using more advanced geographical clustering techniques.
* Adding interactive crime maps.
* Developing a Streamlit dashboard.
* Performing year-wise crime pattern analysis.
* Adding police district and community-area analysis.
* Improving temporal feature representation.
* Including additional crime characteristics in the clustering process.
* Comparing clustering results using multiple evaluation metrics.
* Developing an interactive system for exploring crime hotspots.

---

## 🎓 Learning Outcomes

This project provides practical experience in:

* Data preprocessing
* Missing-value handling
* Exploratory Data Analysis
* Feature engineering
* Date and time analysis
* Geographical data analysis
* Feature scaling
* Unsupervised machine learning
* K-Means clustering
* Elbow Method
* Cluster evaluation
* Crime pattern analysis
* Data visualization

---

## ⭐ Conclusion

The **Chicago Crime Pattern Detection** project demonstrates how unsupervised machine learning can be used to discover patterns in large-scale crime data.

By combining geographical and temporal information with K-Means Clustering, the project groups crime incidents into meaningful clusters and analyzes the dominant crime types within those groups.

The results provide an exploratory view of **where and when different groups of crime incidents occur**, demonstrating the practical application of machine learning to real-world crime data.
