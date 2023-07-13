# Loginext_Case_Study


![image](https://github.com/Jayeshdahiwale/Loginext_Case_Study/raw/main/poster_image.jpg)

Address structuring is an important aspect in the logistics and delivery industry. With the rise of e-commerce and online ordering, customers often make mistakes or provide incomplete addresses, which can lead to delivery failures, delays, or additional costs for businesses.

Some common issues with address input include:

   -  Spelling Mistakes: Customers may misspell street names, locality names, or other address components. These errors can cause confusion for delivery personnel and result in failed deliveries.

   - Missing or Incorrect Postal Codes: Postal codes are essential for accurate routing and delivery. Missing or incorrect postal codes can lead to deliveries being sent to the wrong location or getting delayed.

- Incomplete Addresses: Customers may forget to include important details in their addresses, such as apartment numbers, building names, or floor numbers. Incomplete addresses can make it challenging for delivery personnel to locate the correct destination.

   -  Formatting Issues: Address formats may vary across regions or countries. Customers may not follow the proper formatting guidelines, such as including the street name, locality, city, and postal code in the correct order. This can lead to address misinterpretation and delivery errors.

Address structuring aims to standardize and validate addresses by following specific guidelines and rules. By implementing address structuring techniques, businesses can:

Validate and verify addresses to ensure they are accurate and complete.
Standardize address formats to improve delivery efficiency.
Correct spelling mistakes and inconsistencies.
Append missing address components or fill in incomplete information.
Geocode addresses to obtain latitude and longitude coordinates for precise location identification.

Transaction category prediction plays a vital role in personal finance management. By accurately categorizing transactions, individuals can gain insights into their spending patterns, identify areas where they are overspending, and make informed decisions about budgeting and saving. It allows users to track their expenses across different categories and understand their financial habits.


## Table of Content
  * [About Loginext]
  * [Problem Statement](#problem-statement)
  * [Dataset](#dataset)
  * 
  * [Installation](#installation)
  * [Project Structure](#project-structure)
  * [Tools Used](#tools-used)
  * [Performed Model Result](#performed-model-Result)
  * [Project Summary](#project-summary)
  * [Conclusion](#conclusion)


## Problem Statement
* We are given a data about transactions. Our goal is to categorise those transaction to their Category and SubCategories
* Total rows provided in the dataset are 53000 and 8 columns
* In the fast-paced world of banking and finance, transaction categorization has emerged as a crucial tool for banks to efficiently manage financial data and empower their customers. By automatically classifying transactions into specific categories, such as groceries, utilities, entertainment, or travel, banks can streamline financial processes, provide personalized insights, and enhance overall customer experience. This blog explores the significance of transaction categorization for banks and the benefits it offers to both the institutions and their customers.
* A study conducted by McKinsey & Company found that transaction categorization plays a crucial role in improving customer experience by providing personalized financial insights and recommendations. This leads to higher customer satisfaction and increased loyalty.




## Objective
The classification goal is to predict the Category and SubCategory of the transaction based on given features


## Dataset
The dataset about villages is taken from Govt. open resources. The dataset provides the various information about Locality, PostOffice Name, SubDistrict Name, District Name, StateName and Pincode.
Dataset is taken from  -  [!Link](https://data.gov.in/resource/villagelocality-based-pin-mapping-16th-march-2017)

## API 

Postal PIN Code API


Postal PIN Code API allows developers to get details of Post Office by searching Postal PIN Code or Post Office Branch Name of India.


It has following format:


1. Get Post Office(s) details search by Postal PIN Code

GET https://api.postalpincode.in/pincode/{PINCODE}


2.Get Post Office(s) details search by Post Office branch name

GET https://api.postalpincode.in/postoffice/{POSTOFFICEBRANCHNAME}


Postal PIN Code API returns the response in JSON format. "Status" field in response is set to SUCCESS or ERROR, "Message" field will return message against the request and "PostOffice" field will return data.


Example 1 (Search by Postal PIN Code):

To get details of a PIN Code (110001), use following query

https://api.postalpincode.in/pincode/110001

You will get the response in json format


## About the Proeject Requirements

- I have implemented this project on Kaggle.
- You can access this on Kaggle using - [!Link](https://www.kaggle.com/jayeshdahiwale/loginext-case-study)
- Note : This project requires atleast 15 GB ram to execute. Because dataset has in total 10 Lakhs rows. Vecotorzing all the data even by dividing it on the smaller dataset require this much RAM
- On Colab it will not run. Because google colab provide only 12 GB free ram
- Make sure that you must install fuzzywuzzy library. 
- Rest of the things are built in on any IDE. e.g. Jupyter, paid google colab





## Project Structure
```
├── README.md
├── Dataset 
│   ├── Villaage_Location_Database
│
│
├── Files_For_Input(Json Format)
│   ├── One Line Input
│   ├── Two Line Input
│  
│   
├── loginext_case_study.ipynb (Source Code File)
├── Instructions
└── 
```




## Project Summary
Importing necessary libraries and dataset. Tehn perform data preprocessing , Data Cleaining. Transformation of data was done in order to ensure it fits well into machine learning models. Integrate Indian Post API to trace the info about locations. Designed recommender system which can trace the info if Pincode is not available. Then check all the model_result in order to evaluate the perfomrance of the  business application.


## Conclusion

1. I have made an application which can structure the address in correct format.
2. While correcting the structure we followd the input should be flow like-
  * First Step - Checking whether pincode is present in the adress or not
  * Second Step - Pincode Present - Address will be fetched using Postal Service of India
  * If not able to fetch the correct address -> Then we will try our second way -> Get the address coresponding to pincode through DB-> Will apply some designend algorithm to get the output
  * Even if DataBase not able to get the output, we will use recommendation system for it.

  * Third Step : If pincode is not present in data we will use Recommendation system directly.
  * The final results were pretty descent.
  * Our model can able to insert the correct spellings for location
  * It determines the correct pincode if the provided pincode is not acccoding to the address
    


***************************THANK You*****************************************