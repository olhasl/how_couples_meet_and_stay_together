# **How Couples Meet and Stay Together (HCMST) - Clustering Analysis**

## **Project Overview**
This project explores the *How Couples Meet and Stay Together (HCMST)* dataset from Stanford's Social Science Data Collection. The goal is to apply clustering methods to identify patterns in how couples meet and stay together. The analysis focuses on the 2009 dataset (first wave), grouping respondents based on key demographic and relationship factors.

## **Project Details**
- **Repository:** Clustering  
- **Challenge Type:** Learning  
- **Duration:** 5 days  
- **Deadline:** 21/02/2025 17:00  
- **Team Challenge:** Solo  
- **Dataset:** HCMST (2009)  

## **Mission Objectives**
- Understand and apply clustering methods 
- Learn to visualize cluster distributions  
- Gain familiarity with sociology research protocols  
- Work with real-world survey data  
- Formulate and test experimental hypotheses  

## **Research Questions**
- Can we categorize respondents into broad groups?  
- What are the characteristics of each group?  
- What are the best ways to visualize these groups?  
- Can we derive new insights from clustering results?  

## **Methodology**

### **1. Data Exploration & Feature Selection**
- Examined survey data structure and relevant features  
- Selected **7 categorical features** suitable for **K-Modes clustering**:  
  - **Education Level (4 levels)**  
  - **Age Group (7 groups)**  
  - **Met Online (Yes/No)**  
  - **Has Partner (Yes/No)**  
  - **Marital Status (Married/Not Married)**  
  - **Income Group (groups)**  
  - **GLB Status (Yes/No)**  

### **2. Clustering Approach: Why K-Modes?**
Since all selected features are categorical, **K-Means was not suitable** (as it relies on numerical distances). Instead, the **K-Modes algorithm** was applied, which:  
- Uses **mode-based dissimilarity** instead of Euclidean distance  
- Handles categorical variables efficiently  
- Assigns cluster centroids based on most frequent category values  
- Provides meaningful clusters without requiring numerical transformations  

### **3. K-Modes Implementation**
- The **4-cluster model** was chosen based on interpretability and silhouette analysis.  
- The clustering process was run on the dataset, grouping respondents based on relationship status, education, meeting method, and other demographic factors.  

## **Cluster Insights**
| **Cluster** | **Age Group** | **Education** | **Partner** | **Married** | **GLB Status** | **Meeting Method** |
|------------|-------------|-------------|-----------|---------|------------|---------------|
| **Cluster 0** | 45-54 years | High education (college+) | Has partner | Not married | GLB | Mostly offline (but highest % of online meetings) |
| **Cluster 1** | 35-44 years | High school or college | Has partner | Not married | Not GLB | Mostly offline (second highest % of online meetings) |
| **Cluster 2** | 45-54 years | High school | Has partner | Married | Not GLB | Mostly offline |
| **Cluster 3** | 35-44 years | High education (college+) | Has partner | Married | Not GLB | Mostly offline |

## **Results & Further Analysis**
- The study identified **clear patterns** in how different groups meet their partners.  
- **GLB individuals were more likely to have met online compared to non-GLB individuals.**  
- **Higher education levels correlated with higher online meeting rates.**  
- The **K-Modes method successfully categorized respondents into meaningful groups** without requiring numerical conversion.  

## **Next Steps**
- Expand the analysis to include **HCMST 2017** data.  
- Experiment with **alternative clustering methods** (e.g., hierarchical clustering).  
- Conduct **predictive modeling** on relationship outcomes based on meeting methods.  

📌 **For more details, refer to the Jupyter Notebook: `K-Modes.ipynb`**  
