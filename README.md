# SALARY PREDICTION PROJECT 

**Application deployed :** [Click to see APPLICATION ](https://salarypredictionapplication.herokuapp.com/ "Application")

# DEFINE

## Project Goal:
The goal of this project is to examine the dataset of job postings, and predict salaries for a new set of postings. - This will involve building a model to predict the salaries given in the test dataset.

##  Practical use:
HR Department of a large company or a Consulting groups that needs real-time solutions in order to make effective employment offers to potential hires.

It also finds use in getting to understand current realities in the job market and how businesses can leverage this in order to secure high quality talent, while keeping recuritment cost low.

The primary tool used for this project is Python 3, along with an extensive array of libraries and packages available for the manipulation of data,and development of predictive modeling algorithms.

# DISCOVER

### Data loading
- Received data having 2 .csv files
    - 1st contains job features
    - 2nd contains salaries for each job.
- In both sheets, JobID is common column.
- Import both files and merge them into one single dataframe with reference to jobID.

### Clean Dataset - Observatios & Outcomes
- There are zero rows negative values in all numeric columns.
- Years of Experience can be zero for fresher also Miles From Metropolis can be zero who live in city.
- But, There are 5 invalid entries in salary column and all having value 0 which is not expected.
- Hence need to handle those 5 values

### Exploratory Data Analysis (EDA)
- Target feature is Salary column rest others will be independent features (we exclude jobID, companyID features as they are unique identity key)
- Except salary colum other two features having median and mean close to each other
- Salary:
        - Mean is greater than median shows its right skewed/ positive sekwed and contains outliers

<img src="/Users/ganesh_dhasade/Desktop/outliers.png">
![Outliers](/Users/ganesh_dhasade/Desktop/outliers.png)


As we can see above 3 visualizations in box plot "SALARY" column having outliers
Remove the outliers rows from the dataset
As there are only 5 rows out of 1million datarows we can delete
refer to get more about formula: https://www.simplypsychology.org/boxplots.html#:~:text=When%20reviewing%20a%20box%20plot,whiskers%20of%20the%20box%20plot.&text=For%20example%2C%20outside%201.5%20times,Q3%20%2B%201.5%20*%20IQR).
So basically use formula:
outside 1.5 times the interquartile range above the upper quartile and
below the lower quartile (Q1 - 1.5 IQR or Q3 + 1.5 IQR).

# DEVELOPMENT

# DEPLOYMENT