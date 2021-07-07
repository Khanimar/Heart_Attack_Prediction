**Attention please**:
To see the result of the latest version of the project, please refer to:

https://www.kaggle.com/khanimar/heart-attack-prediction-eda

# Heart_Attack_Prediction
The problem that this project is going to anlyze is heart attack. The final objectives of this project is to use the provided data to perform the following tasks:  
1. Performing EDA to obtain useful primary insights 
2. Using the provided set of input features and their corresponding labels to predict the likelihood of a potential heart attack in each sample. In other words, the problem is to provide a binary classifier that is able to predict if a person is prone to a heart attack or not.

# Preface

## Problem Identification/ Problem statement

First of all, in each project, we should understand what exactly the problem is, which reasons exist behind of the problem, how does it affect all the involved parties and what are clarified points in the main goal of this data science project or the business goal of the project. 

One way to make the final objective more clear is to ask this question: 

*For what purpose can the company/customer use the provided analysis?*

## Business understanding

To this aim, we should get the **domain knowledge** by speaking to the stakeholder and the industrial partner experts. In addition, we should get enough information about the company/customer iself and their business/services and products. 

Furthermore, by reading the **documentation of the project** including data description/feature description, the format of provided data file etc. we can get some information about the data and become familiar with the data.

The following 3 steps can be done during our analysis, too:

1. We should make clear **which questions do we want to answer in this project** to provide useful insights from the data and improve decision-making process as well as providing data-driven solutions? By **designing meaningful and insightful questions** that should be answered during the analysis, we can correctly analyze the founded answers.

2. Moreover, it is really recommended to **search over the internet and review external valid sources** to add some useful aspects, insights and suggestions to the project or provide some hints to perform useful Exploratory Data Analysis (EDA) and data visualization steps. It is also a good idea to **find some valid documentation (information/reports/research/analysis), evidence, statistics** to support the obtained insights and recommendations.

3. Another point is that if it is possible, and it can improve the result, we can **add some other data to the original data** or even combine structured and unstructured data. 

### Identifying Challenges

We should make clear **which challenges we are facing regarding the project and the data**. For example, if we want to work with an unstructured data like text, we should know that extracting information from text files, converting unstructured information into a structured format, combining the data, and ensuring data quality are some of the main challenges. 

### Project Properties

We should determine **key objectives of the project** and **project specifications**, **project schedule** as well as calculate **time requirements and sequencing project elements**. For example, we should know if the company wants to receive prediction or some insights or some important factors (strong indicators) behind an event.

### Necessary Spices
During each technical data analysis process, it is a good idea to add some **artistic aspects** to the work that play the role of spices during cooking a food. For example, we can put some related images for every part of the analysis to make it more understandable. 

# Heart attack prediction problem

Based on the above-mentioned steps, we determine the following points for the current project:

## Problem Identification/ Problem statement

The problem that this project is going to anlyze is heart attack. The final objectives of this project is to use the provided data to perform the following tasks:

1. Performing EDA to obtain useful primary insights 
2.  Using the provided set of input features and their corresponding labels to predict the likelihood of a potential heart attack in each sample. In other words, the problem is to provide a binary classifier that is able to predict if a person is prone to a heart attack or not.

## Business understanding

In this project, we have some data for Heart Attack Analysis & Prediction which is downloaded from:https://www.kaggle.com/rashikrahmanpritom/heart-attack-analysis-prediction-dataset?select=o2Saturation.csv
    
Since we do not have an industrial partner and got the data over the kaggle website, there is no opportunity to get further domain knowledge from such a partner.

-----------------------

# Project properties

## Data exploration

The provided data for the project is in the shape of **two CSV files** of `heart.cs`* and `o2Saturation.csv`.

The `heart.csv` file includes **13 input features** and their corrsponding **target feature** for **303 samples**.

Beside the first tow features that express the **age** and the **gender** of each sample (person), remaining **11 featurs** are providing some values of various medical measurements of that person.

**3 input features** as well as the **target feature** have **binary values ({0,1})** , while others have numerical values in different ranges. So, although there is no categorial feature among the data that should be transferred a numrical feature, in the case of using some specific machine learning models, we may need to normalize our numerical input features before feeding them to the selected model. 

The `o2Saturation.csv` is a single column csv file that includes **3585 floating point values** without nay further infomation. So, using the values of this file along our data analysis process without any clu about its meaning and its different dimensionality with respect to the data of the `heart.csv` file, can be quite challenging.

## Feature description:

The very short documentation of the project, provides following descriptions for each feature of the the `heart.csv` file: 

1. **Age**: Age of the patient

2. **Sex**: Gender of the patient
    - 0: Female
    - 1: Male
    
3. **cp**: Chest Pain type, For this feature, possible values and their meaning are as follows:
    - 0: typical angina
    - 1: atypical angina
    - 2: non-anginal pain
    - 3: asymptomatic    
    
4. **trtbps**: resting blood pressure (mm Hg)

5. **chol**: Serum cholestoral (mg/dl) fetched via BMI sensor

6. **fbs**: (fasting blood sugar > 120 mg/dl)
  - 0: No
  - 1: Yes

7. **restecg**: resting electrocardiographic results, For this feature, possible values and their meaning are as follows:
  - 0: normal
  - 1: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV)
  - 2: showing probable or definite left ventricular hypertrophy by Estes' criteria
  
8. **thalach**: maximum heart rate achieved during thalium stress test  
  
9. **exng**: exercise induced angina:
    - 0: No
    - 1: Yes
    
10. **oldpeak**: ST depression induced by exercise relative to rest    

11. **slp**: Slope of peak exercise ST segment (
  - 0: upsloping
  - 1: flat
  - 2: downsloping
    
12. **caa**: number of major vessels (0-3).

13. **thall**: Thalium stress test result: 
    - 1: normal
    - 2: fixed defect
    - 3: reversible defect

14. **output**: heart attack prediction output (target feature)
    - 0: less chance of heart attack
    - 1: more chance of heart attack

-------------------------

### External obtained knowledege about input features of the project

As explianed before, since we do not have a partner, we cannot get more information about these features from our partner. So, we search over the internet and try to get some information about them.

3.**cp**: This feature is related to some well-known **chest pain types** as follows:
       
- **Typical angina (TA)**: is defined as substernal chest pain precipitated by physical exertion or emotional stress and relieved with rest or nitroglycerin. Angina chest pain is a pressure or squeezing like sensation that is usually caused when your heart muscle doesn’t get an adequate supply of oxygenated blood.

- **Atypical angina**: When one experiences chest pain that doesn’t meet the criteria for angina, it’s known as atypical chest pain. If the chest pain cannot be considered as angina, then that person is said to suffer from atypical chest pain, which unlike typical chest pain, doesn’t occur in the sternum and may radiate to other parts of the body.

- **Nonanginal pain**: Which has one characteristic of typical angina. Nonanginal chest pain carries intermediate risk for CAD (stable coronary artery disease) in women older than 60 years and men older than 40 years.

- **asymptomatic (Silent myocardial ischemia - SMI)**: is defined as a transient alteration in myocardial perfusion in the absence of chest pain or the usual anginal equivalents. Patients may be classified as having one of the three types of SMI: 
    - **type A**: totally asymptomatic patients with no history of angina or myocardial infarction,
    - **type B**: asymptomatic patients with previous myocardial infarction,
    - **type C**: patients with angina and asymptomatic ischemic episodes.

4.**trtbps**: Normal resting blood pressure, in an adult is approximately "120/80 mmHg"
       
6.**fbs**: Fasting blood sugar test. A blood sample will be taken after an overnight fast. A fasting blood sugar level less than 100 mg/dL (5.6 mmol/L) is normal. A fasting blood sugar level from 100 to 125 mg/dL (5.6 to 6.9 mmol/L) is considered prediabetes. If it's 126 mg/dL (7 mmol/L) or higher on two separate tests, you have diabetes
       
7.**restecg**: is used to assess known cardiovascular diseases

9.**exng**: Exercise-induced angina (AP) is a common complaint of cardiac patients, particularly when exercising in the cold. This feature indicates whether the patient had the experience of the exercise induced angina or not. 

12.**caa**: number of major vessels. The major blood vessels connected to your heart are 
  - aorta, 
  - superior vena cava, 
  - inferior vena cava, 
  - pulmonary artery (which takes oxygen-poor blood from the heart to the lungs where it is oxygenated), 
  - pulmonary veins (which bring oxygen-rich blood from the lungs to the heart), and 
  - coronary arteries (which supply blood to the heart muscle). 

    This feature indicates the **number of observable major vessels colored by fluoroscopy for each patient**. 

    **Fluoroscopy** is a test that uses a steady beam of x-rays (like a movie) to look at parts of the body and movement within the body, such as blood moving through a blood vessel. Fluoroscopy also can be used to help find a foreign object in the body, position a needle for a medical procedure, or realign a broken bone.

---

##### Some questions that we may ask about the problem (before any data exploration or going further to the analysis steps):

- What are the most important factors that increase the risk of heart attack occurrences?
- What is the amount of correlation between the given features and heart attack occurrences? 
- Does the sex affect the heart attack occurrences? 
- How is the rate of heart attack occurrence in different countries?
- Is there a special period of time during the day or night that the rate of heart attack occurrence increases?
- Is there a special year that the rate of heart attack increased? if yes, why?
- How does the rate of heart attack change during different seasons of a year?
- What is the most effective strategy or medicine to prevent the heart attack occurances?
- Which factor(s) determine(s) if a heart attack leads to death or not?
- What kind of the chest pain can be considered as a serious warning of potencial heart attack for a patient?
- Is there any correlation between levels of        
  * blood pressure
  * cholestoral 
  * blood sugar      
  and the risk of having a heart attack?
- which features can be considered as the heart health measures that may reduce the risk of having a heart attack in a patient?  

   
More questions can be proposed during the data analysis process.
