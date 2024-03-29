# Olympic-data-analysis-using-Azure

This project deals with Tokyo Olympics 2021 dataset. This project involves understanding the data architecture, creating the ETL pipeline, and finally analysing the data. The project is based off Darshil Parmar video on YouTube. This contains the details of over 11,000 athletes, with 47 disciplines, along with 743 Teams taking part in the 2021(2020) Tokyo Olympics. This dataset contains the details of the Athletes, Coaches, Teams participating as well as the Entries by gender. It contains their names, countries represented, discipline, gender of competitors, name of the coaches. 

There are 5 datasets from which the data was extracted to perform analysis.

- Athletes data: The file contains all athletes data. Columns: Name, Name of Country (NOC) and Discipline
- Coaches data: The file contains coaches names. Columns: Name, Name of Country (NOC), Discipline and Event
- Entries Gender data: The file contains males and females data. Columns: Discipline, Female, Male and Total
- Medals data: The file contains ranks and all the three medals. Columns: Rank, Team/NOC, Gold, Silver, Bronze, Total, Rank by Total
- Teams Data: The file contains all the teams. Columns: Name, Name of Country (NOC), Discipline and Event

Source of the dataset: [Link](https://www.kaggle.com/datasets/arjunprasadsarkhel/2021-olympics-in-tokyo)

# Data Architecture

![Untitled-2024-03-11-0818](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/7df97d32-6649-4576-bee8-685761567c1d)


# Data Ingestion
Extract the data from the the github as a source using Azure Data Factory tool, building a data flow and loading it into Azure Data Lake storage:

![Screenshot (17)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/6047e53e-2542-488d-b643-ddc884176503)

# Data Transformation in Azure Databricks:

Write the code in Python to read the data stored in the Azure data lake, perform the transformations and then load the back to Azure data lake Gen 2 

![Screenshot (27)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/5d48dcd6-8d01-4f62-8308-fd501d5b4d22)

Here you upload your transformed data in ADLS Gen 2:

![Screenshot (28)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/7ca05ddb-97a0-4cbd-be95-d4c663336a13)


![Screenshot (29)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/7b03e6ea-69ee-4e5e-9a65-e4529d802b6c)


# Data Analysis 

The final step is to analyse and derive important insights from this data using SQL. 

## Calculating the total number of athletes from each country

![Screenshot (26)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/f6e7a762-657f-48f2-9415-671043b150ee)


## Total number of medals won by India


![Screenshot (23)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/4873bb22-26da-4fa2-9920-53a6bcc46072)


## Total number of athletes by discipline in India


![Screenshot (24)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/791eae22-bdb1-4a9a-8dc1-938a751dcfbd)

![SQL script 1 (5)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/3a38a871-1b79-4e7e-93db-5b47bc6790e3)

## Countries with highest number of coaches 

![Screenshot (30)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/08c0abe0-e1b8-40d1-9faa-1f432b450842)

![SQL script 1 (6)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/7790f114-6b40-4998-bac7-ff0d5c16d753)


## -- calculate the average number of entries by gender for each discipline 

![Screenshot (31)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/b250bc22-eacd-4d35-8f22-1f279c2134ec)

![SQL script 1 (7)](https://github.com/rajsaurav/Olympic-data-analysis-using-azure/assets/35574674/a4d90b76-4723-4d62-955a-78ba1026b38d)


