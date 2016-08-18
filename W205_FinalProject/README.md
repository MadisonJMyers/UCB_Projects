How Secure is Your Job?

Our w205 group set out to find out.

Context:

Introduction: Age of Job Insecurity

Though the upturn of personal freedoms, increased education and developing economies worldwide may lead to the illusion of a secure hiring climate, reality is in great contrast. In fact, the current climate for jobs can be unsettling, particularly depending on the sector in which you seek employment and the subject which you have studied. Global trends show that more and more people are investing in education as it is “believed to deliver opportunity“, yet most recent grads struggle to find employment unless they are in the technology or medical fields. Almost all workers now “face greater job insecurity than in the past, due to increases in the practice of downsizing, layoffs and other expressions of employers’ willingness to treat labour as a variable cost of production”. This change is due to rapidly changing organizations who must adapt to new global trends or fail. “The unpredictable economic situation and the tougher competitive standards have resulted in downsizing, mergers, acquisitions, and other types of structural change”. This insecurity is found across the globe where employment is shifting from product- based to knowledge-based and from full employment to contract or part-time work, leading to a change in skill demand, as well as a change in job availability. As of 2009, the service sector provided 42.7 % of jobs “compared to agriculture (34.9%) and industry (22.4%) and in developed economies the service sector is even larger; for instance representing 71.5% of all EU jobs”, which is a dramatic change from previous decades. As a result, job seekers and current employees are now combating an environment saturated with increased global mobility, increased competition and increased insecurity, leading to a very difficult job market to navigate.

The Solution Our Project Proposes to Have: 

Due to the insecure employment environment, our team has decided to analyze the job market in order to help people make more informed job choices. We have broken the environment down into several factors: location, industry sector, income, expected savings, local standard of living, unemployment rate, hiring trends, retention trends, and layoff trends. Looking at these factors, we hope to not only demonstrate the factors one should consider when choosing a field of study or a field of work, but we hope to also help predict where hiring and layoffs will take place.

Architecture:

Our System Architecture is divided into four phases: Data cleaning, initial querying and analysis, machine learning and visualizations. We initially stored our data in S3 and then launched an EC2 instance, the "ucbw205_complete_plus_postgres" AMI on AWS . We then used Hive on top of Spark within our EC2 instance on AWS. Within Hive we explored our data, conducted queries, formed tables and transformed our data on the connection between our beforementioned factors: location, industry sector, income, expected savings, local standard of living, unemployment rate, hiring trends, retention trends, and layoff trends. This gave us a better idea of what our outlooks were and the trends across different sectors and countries. These outputs were visualized using Tableau. The next step was to build a model to determine how long selected sector employees could survive if given a layoff. The next analysis, using PyBrain and Scikit, was focused on analyzing the global job market and its relation to the related country economy. The outputs were stored again in Amazon Storage Services (S3) and were visualized once again by Tableau. 

File explanation:

Singapore Data:
1. Data.zip 

These are the CSV files that have been downloaded from our public source.

2. ddl sing

This is the set of ddl statements to move the file to hadoop and create external tables in hive. 

(Note that the wget statements refer to s3 in the aws account )

3. sing analysis

This is the set of hive codes for doing analysis over the existing tables created in step 2 above. 

4. sing analysis output

5. W205_FinalProject-ASahni-SYChang-MJMyers.pdf

Final Project Summary

6.W205_Final_ARMA_Prediction-Copy1.ipynb

Jupyter Notebook File (Python) for the Final ARMA Prediction

7.W205_Final_Fred-Copy1.ipynb

Jupyter Notebook File (Python) for the Final FRED analysis

8. W205_Final_TS_Prediction-Copy1.ipynb

Jupyter Notebook File (Python) for the Final TS Prediction

9. Group_w205_Project_A.Sahni_SY.Chang_MJ.Myers

Powerpoint Presentation for Group Project

All data sources are listed in the Final Project PDF.



