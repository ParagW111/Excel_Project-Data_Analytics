# Excel_Project-Data_Analytics
Project demonstrating my Excel skills.

<img width="944" alt="Dashboard Image" src="https://github.com/user-attachments/assets/9b292eae-0d72-4a76-9dbb-4b9f62fa3d7c" />

# Dashboard file

[Checkout my work here.](https://github.com/user-attachments/files/19924415/Dashboard.xlsx)

## Excel skills used

The following Excel skills were utilized for analysis:

-📉 Charts  
-🧮 Formulas and Functions  
-❎ Data Validation

## Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. The dataset is available via my Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

-👨‍💼 Job titles  
-💰 Salaries  
-📍 Locations  
-🛠️ Skills

## Dashboard Build

## 📉 Charts  
📊 Data Science Job Salaries - Bar Chart  

![1_Salary_Dashboard_Chart1](https://github.com/user-attachments/assets/1d4355bf-f3d5-40a7-83c8-06897a33f619)  

-🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.  
-🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.  
-📉 Data Organization: Sorted job titles by descending salary for improved readability.  
-💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.  

## 🗺️ Country Median Salaries - Map Chart  

![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/3c1b8a28-7d4b-4eda-b559-3b9dbf1c3264)  

-🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.  
-🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.  
-📊 Data Representation: Plotted median salary for each country with available data.  
-👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.  
-💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.  

## 🧮 Formulas and Functions

💰 Median Salary by Job Titles  

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

-🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.  
-📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.  
-🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.  
-🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.  

### 🍽️ Background Table

![1_Salary_Dashboard_Screenshot1](https://github.com/user-attachments/assets/9818031a-4cf6-4baa-b257-7128f20a2958)  

### 📉 Dashboard Implementation  

![1_Salary_Dashboard_Job_Title](https://github.com/user-attachments/assets/cb8d3166-1661-44b1-8bf1-db23d36c5301)  

### ⏰ Count of Job Schedule Type  

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

-🔍 Unique List Generation: This Excel formula below employs the ```FILTER()``` function to exclude entries containing "and" or commas, and omit zero values.  
-🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.  

### 🍽️ Background Table  

![1_Salary_Dashboard_Screenshot2](https://github.com/user-attachments/assets/9f33ee8d-a965-47c7-915b-1762278af2a7)  

### 📉 Dashboard Implementation:  


![1_Salary_Dashboard_Type](https://github.com/user-attachments/assets/9920f020-eab4-412c-893a-a6eff3219e3d)  

## ❎ Data Validation
### 🔍 Filtered List  

-🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:  
    -🎯 User input is restricted to predefined, validated schedule types  
    -🚫 Incorrect or inconsistent entries are prevented  
    -👥 Overall usability of the dashboard is enhanced  
    

![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/5c1cbc7e-1950-4e09-9023-fd3d7750a6f1)  

## Conclusion  

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.








