<h1 align="center"> Instahyre Job Analytics </h1>

<img src="https://github.com/AmarjeetRoy/AmarjeetRoy/assets/137817362/089a3079-6ae4-4e1d-885a-6c162f720c66">
<br><br>

Welcome to the **Instahyre Job Analytics** repository! This project revolves around comprehensively understanding the job market dynamics using data-driven insights. Our team, consisting of dedicated members, embarked on a journey to extract, preprocess, and analyze job posting data from Instahyre and LinkedIn, shedding light on the employment landscape.

<br>

## 🧑🏽‍💻Team Members

- Ajaykumar Jogani (My Self)
- Priya Bhardwaj
- Amarjeet Roy 
- Bharat Sharma
<br>

## 🎯Aim
- Develop a robust model for summarizing job posting data, offering users a concise snapshot of prevailing job market trends.
- Establish an interactive webpage interface, facilitating seamless access and exploration of comprehensive job market insights.
- Empower job seekers and recruiters alike by furnishing them with crucial information to make well-informed decisions in the job market.
<br><br>

## 👁️Project Overview

The data extraction phase involves obtaining job posting data from Instahyre's website. This process is crucial for gathering raw data that will be later cleaned, processed, and analyzed.
<br>
### 🗒️Web Scraping
- Employed Python's Selenium library to automate web scraping, streamlining the data collection process for enhanced efficiency.
- Focused on extracting key job-related attributes including "job_id," "company_id," "location," "designation," and company details such as "name," "estab_year," and "employees_count."
- Gathered additional information regarding job involvement, required skills, and HR contact details to provide a comprehensive dataset for analysis.
- Implemented a custom Selenium script, finely tuned to extract the desired data from the Instahyre website, ensuring accuracy and specificity in the scraping process.
**Reference Files:**
- **[`Extraction_Code.ipynb`](Extraction/Extraction%20Code.ipynb)**: Python script for web scraping job posting data and LinkedIn information.
### 🗒️Data Preparation
After scraping the data, our next step involved comprehensive data cleaning and transformation using Python libraries. This step was essential for handling missing values, outliers, and ensuring data consistency. Additionally, we organized the cleaned data into three separate tables, these tables can be found in **[`Tables`](Extraction/Tables)** folder inside the **[`Extraction`](Extraction)** Folder:
- **[`Jobs Table`](Extraction/Tables/job.csv)**: This table contains information related to job postings, including "job_id," "location," "designation," "skills," and "hr_name."
- **[`Company Table`](Extraction/Tables/company.csv)**: Here, we stored company-specific data such as "company_id," "name," "estab_year," and "employees_count."
- **[`Details Table`](Extraction/Tables/Details.csv)**: This table holds additional details related to job postings and companies, including "involvement" and other relevant information.
- **[`Merged Table`](Extraction/Tables/Merged_data.csv)** : This Table contains all the scrpaed Details including Linkedin's data and all three table's data.

**Additional Files in Extraction Directory:**
  - **[`Job webLink.csv`](Extraction/Job%20webLinks.csv)**: Contains web links of all job pages.
  - **[`New Updated Csv.csv`](Extraction/New%20Updated%20CSV.csv)**: Preprocessed data with some initial modifications.

<br>

### 💻Data Preprocessing and Model Building

- The data preprocessing and model building phase focus on refining the raw data and creating a clustering model for analysis.

### 💻Data Cleaning
- Conducted thorough data cleaning and preprocessing using Python libraries to enhance data quality and prepare it for further analysis.
- Addressed issues such as missing values and outliers, ensuring data integrity and accuracy throughout the dataset.
- Implemented measures to maintain data consistency, a crucial step in ensuring reliable and meaningful analytical results.

### 💻K-means Clustering Model
- Utilized Scikit-learn to construct a K-means clustering model, enabling the categorization of companies based on their LinkedIn followers and employee count, facilitating a comprehensive understanding of distinct company classes.
- The K-means model played a pivotal role in extracting valuable insights from the job market data, and efficiently classifying companies based on their relevant attributes.
- All code related to these processes is available in the **[`Processing`](Processing)** folder's **[`Data Preprocessing and Clustering.ipynb`](Processing/Data%20Preprocessing%20and%20Clustering.ipynb)** file. This notebook utilized the **[`New Updated Csv.csv`](Processing/New%20Updated%20CSV.csv)** as input dataframe, resulting in the generation of **[`Processed_file.csv`](Processing/Processed_file.csv)** which includes detailed information on Job Class and any alterations made during the data cleaning process.
<br>

- Added a Python script to calculate the Sum of Squared Error (SSE) for different cluster numbers using K-Means clustering, and visualized the results with an Elbow Plot using Matplotlib.
<p align="center">
    <img src="https://github.com/Ajaykumarjogani/Instahyre_Job_Analytics_2/assets/122745303/d7786d67-7c78-41fd-9bf9-3d4de20bd1b3.png">
<p>


<p align="center">
    <img src="https://github.com/Ajaykumarjogani/Instahyre_Job_Analytics_2/assets/122745303/afe73644-275a-4349-8466-a3dac73092df.png">
<p>



- Developed a Python script utilizing the KMeans clustering algorithm to categorize data points into four clusters based on scaled values of Employee Counts and LinkedIn Followers. Visualized the resulting clusters and centroids using Matplotlib, distinguishing them with distinct colors for enhanced clarity.
<p align="center">
    <img src="https://github.com/Ajaykumarjogani/Instahyre_Job_Analytics_2/assets/122745303/f4110e8f-a7c8-4006-a95b-6c54615eec15.png">
<p>
  
<p align="center">
    <img src="https://github.com/Ajaykumarjogani/Instahyre_Job_Analytics_2/assets/122745303/1419c316-5782-47e2-8b75-de8e0ab5efd5.png">
<p>


### 🕸️Website Development and Model Deployment

- The website development and model deployment phase involved creating an interactive website to present our insights and model results to users.

### 🖼️Frontend Development

We designed and implemented the website's frontend using HTML and CSS. The website consists of three pages which are stored in **[`templates`](Application/templates)** :

- **[`first.html`](Application/templates/first.html)**: The landing page where users input their skills.
- **[`second.html`](Application/templates/second.html)**: A page that displays summarized job market insights.
- **[`Job_details.html`](Application/templates/job_details.html)**: A page presenting detailed job posting information.

### 💾Backend Integration
- The Flask application, named **[`app.py`](Application/app.py)** serves as the intermediary between user inputs and the backend operations. It facilitates seamless interaction with the data, allowing users to explore insights and retrieve specific job details.

## Additional Files

- **[`Job Analytics.pptx`](JOB%20ANALYTICS.pptx)**: A presentation summarizing the project's details and key insights.

<br>

## 🤩Website Overview
**Landing Page**
- The landing page serves as the entry point for users. It's where users can input their skills and interests to explore job market insights.

<p align="center"> 
  <img src="https://user-images.githubusercontent.com/137817362/267758828-92c5904b-432c-4b54-9028-54b79d5c8d32.png" style="border-radius: 50%;">
</p>


**Summarized Insights Page**
- The summarized insights page presents users with key information about the job market based on their input.
<p align="center"> 
   <img src="https://github.com/AmarjeetRoy/InstaHyre-Job-Analytics-Machine-Learning-/assets/137817362/9a133c9b-3ba2-458a-a585-a5d8036827f9" style="display: inline-block; margin: 0 auto; width:800px;">  
</p>

**Job Posting Details Page**
- Detailed information about individual job postings, including job title, company name, location, required skills, and HR contact details.
<p align="center"> 
   <img src="https://github.com/AmarjeetRoy/InstaHyre-Job-Analytics-Machine-Learning-/assets/137817362/74d7f80d-5e05-441d-849e-252ee78c636e" style="display: inline-block; margin: 0 auto; width:1000px;">  
</p>

<br>

## 📝Key Findings

1. **Experience Level**: "Mid-Level" is the most common experience level in job postings.

2. **Top Industries**: IT, Finance, Healthcare, and Engineering are the leading industries.

3. **Company Size**: Companies with 100-500 employees have the most job listings.

4. **In-Demand Skills**: Python, Java, SQL, and Data Analysis are highly sought after.

5. **Job Type**: Full-time positions dominate job postings.

6. **HR Contact**: HR contact information is available for direct communication.

7. **Clustered Companies**: Companies are categorized using K-means clustering based on employee count and LinkedIn followers.

<br>

## 💼Project Summary

The Instahyre Job Analytics project involved web scraping job posting data from Instahyre, followed by data preprocessing and clustering analysis. It culminated in the development of an interactive web application for users to explore job market insights.

### 💡Key Learnings

- Automating web scraping for data acquisition.
- Data preprocessing and clustering analysis techniques.
- Web development for user-friendly data presentation.

### 🪨Challenges

- Ensuring data consistency and accuracy.
- Developing and fine-tuning the clustering model.
- Creating an interactive web application.
- Handling large data volumes while considering data privacy.

In summary, the project successfully provided insights into the job market through data analysis and web development, despite various data-related challenges.🙏🏻
