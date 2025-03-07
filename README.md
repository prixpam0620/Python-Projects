Exploratory Data Analysis of the dataset Social Media Tourism

EXECUTIVE SUMMARY
Problem Statement:-
“An aviation company that provides domestic as well as international trips to the customers now  wants to apply a targeted approach instead of reaching out to each of the customers. This time  they want to do it digitally instead of tele calling. Hence they have collaborated with a social  networking platform, so they can learn the digital and social behaviour of the customers and  provide the digital advertisement on the user page of the targeted customers who have a high  propensity to take up the product. 
Propensity of buying tickets is different for different login devices. Hence, you have to create 2 models separately for Laptop and Mobile. [Anything which is not a laptop can be considered as  mobile phone usage.] 
The advertisements on the digital platform are a bit expensive; hence, you need to be very accurate while creating the models. “      
Basing upon the given problem statement the focus is on users demonstrating a high propensity to purchase tickets, categorized by their login device (preference laptop or mobile).
The dataset includes various user related variables such as User ID, taken product (target variable), yearly travel related activities, preferred device, demographics of the user.
We will develop two separate machine learning models - one for laptop users and the other for mobile users.  The models will predict the likelihood of a user purchasing tickets based on their digital behavior.  This approach aims to optimize digital advertising expenditures by accurately targeting potential customers.
The high cost of digital advertising necessitates highly accurate predictive models to reach out the customers using the digital devices easily that enable the customers to approach their tourism services.  To attain this, the company must effectively utilize customer data to identify the high potential customers.

Main steps:
1)  Data preprocessing:
o   Address missing values and encode.
o   Standardize or normalize numerical features.

2)  Data splitting:
o   Divide the data into training and testing
 3) Model Building:
                          Employ classification algorithms (eg: logistic regression, decision trees etc.) for each device style.
4)  Model Evaluation:
o   Assess model performance using metrics like accuracy, precision, recall and F1 Score.
o   Fine tune models or explore alternative algorithms needed.

5)     	Digital Advertising Targeting:
o   Utilize trained models to predict the propensity to buy tickets
o   Direct digital advertisements to users with a high proper on their social networking platform pages.

6)  Monitoring and Iteration:
o   Regularly monitor model performance and update as necessary.
o   Gather feedback on advertising effectiveness and refine models.

7)  Cost Management:
o   Monitor advertising costs and optimize targetting strategy to ensure cost effectiveness.

Conclusion for Executive Summary

Increased marketing efficiency: - Reduced marketing expenses by targeting the most likely customers.

Enhanced customer engagement: - Improved customer engagement through personalized digital advertisements.

Boosted ticket sales: - Increased ticket sales by focusing on customers with a high propensity to purchase.







![image](https://github.com/user-attachments/assets/d2f6e9e4-16ce-4f56-86f9-fdb90b53b895)
When dealing with data for building machine learning models, it's essential to consider the sampling method to ensure that your model is trained on a representative dataset.
On visual inspection, we observed that the data-set has less than 10% missing values, we used KNN imputer to replace the data using clustering algorithm.
The output of the KNN imputer was validated before doing the analysis. 
Data was checked in excel to understand numerical and string, float, missing value – and then the categorical values were replaced using a ‘. replace function’ 
Data were also mapped to convert categorical to numerical values, they were encoded in binary numbers 0, and 1 for the model to interpret them correctly.

2.2.4. DATA CLEANING
I.	Information of data, by using data.head() and df.tail(), we will be able to see if the right set of data is imported for our analysis.
This is how it will look-
 

 

II.	 Checking more about the data by data.info()
 
Observation: The dataset has total 17 features and few missing values in some of the columns.

III.	Checking Data Shape
 
Observation: Data has 17 columns and 11770 rows

IV.	Checking Null Values 
 
Observation:  Dataset has some missing values and the sum of all missing values in each feature are displayed here. 
There are several techniques to take care of missing values to make them valuable. In our dataset we will use KNN imputer to handle missing values.

V.	Data Manipulation
In our dataset there are varied values under features like ‘preferred devices’, Yearly_avg_view_on_travel_page', 'total_likes_on_outstation_checkin_given', 'Yearly_avg_comment_on_travel_page’ are found. 
Checking Unique values and further mapping/manipulating them for our analysis
 
Observation: Preferred devices have various values, whereas we need only laptop and mobile for our analysis. So, we found them by using panda function 
df [‘preferred_device’].unique()
 and now we will map these devices between laptop and mobile as per problem statement requirement. We have performed similar actions for other categories as shown above to get unique values.
 V(a).   Mapping values:
 
Observation: After running the above code, data will be aggregated to mobile and laptop

VI.	Imputation of feature categories
We will use KNN imputer to work with them.
 
For our analysis and modeling we are dividing our dataset into train and test set and then by executing following codes: 
 
We now will perform our models by using Logistic Regression, DecisionTree, Random Forest, Support Vector Machine, KNN, Naive bayes models to understand which machine learning algorithm will fetch us with maximum accuracy.

2.2.5. DATA ANALYSIS TOOLS
There are various tools available for data analysis, and the choice often depends on factors such as the complexity of the analysis, the size of the dataset, and the preference of the analyst or data scientist. Here are some popular data analysis tools
Python with Libraries:
●	NumPy and SciPy: Fundamental packages for scientific computing with support for large, multi-dimensional arrays and matrices.

●	Pandas: Provides data structures for efficiently manipulating large datasets, including data cleaning, exploration, and transformation.

●	Matplotlib and Seaborn: Libraries for creating static, animated, and interactive visualizations in Python.

●	Jupyter Notebooks: Interactive computing environment that allows you to create and share documents containing live code, equations, visualizations, and narrative text.

●	Microsoft Excel: Widely used spreadsheet software that supports data analysis, visualization, and basic statistical functions.

●	Power BI: A business analytics service by Microsoft that provides interactive visualizations and business intelligence capabilities.
●	
●	Google Sheets: Similar to Excel, it's a cloud-based spreadsheet tool that supports collaboration and basic data analysis.

Often, a combination of tools is used throughout the data analysis process, depending on the tasks at hand. 
2.3. PERIOD OF STUDY
A data analysis and machine learning project may take weeks to months, depending on the scope and objectives. Here's a general breakdown of potential phases and their durations:
●	Data Exploration and Preparation: This phase involves understanding the dataset, cleaning data, and preparing it for analysis. It might take 2 to 3 weeks

●	Model Development: Creating and fine-tuning machine learning models can take some time. The duration depends on the complexity of the models, the size of the dataset, and the computational resources available. This phase might take 2 to 3 weeks

●	Evaluation and Fine-Tuning: After training the models, there's a need to evaluate their performance, fine-tune hyperparameters, and optimize for accuracy. This process may take another 2 to 3 weeks

●	Deployment: Deploying models for digital advertising involves integrating them into the collaboration with the social networking platform. This phase might take another 2 to 3 weeks, considering testing and validation.

●	Monitoring and Updating: Ongoing monitoring of model performance and potential updates based on new data or changing requirements is a continuous process.
                       hence we got the total of 3 months to complete this project
The study will be conducted over a 3 month time frame .The duration should be sufficient to capture seasonal and temporal variations in customer behavior.

2.4 UTILITY OF RESEARCH
The utility of research is multifaceted and far-reaching. It plays a crucial role in advancing human understanding, improving decision-making, and driving innovation. Here are some specific examples of the utility of research:
1.	Advancing knowledge:
                       Research is the foundation of scientific progress. Through systematic inquiry and rigorous methods, researchers continuously expand our understanding of the world around us, from the smallest particles to the vast universe. This knowledge enables us to make sense of our observations, develop new theories, and solve complex problems.
2.	Improving decision-making:
                                  Research provides valuable evidence and insights that can inform decision-making in various aspects of life, from personal choices to public policy. By understanding the underlying causes and consequences of various phenomena, we can make more informed decisions about our health, education, environment, and other critical areas.
3.	Driving innovation: 
                             Research is the driving force behind technological advancements and new discoveries. By exploring new frontiers and pushing the boundaries of knowledge, researchers pave the way for groundbreaking inventions, innovative solutions, and improved products and services.
4.	Solving problems:
                                Research provides the tools and methodologies to address pressing challenges and solve complex problems facing society. From environmental sustainability to healthcare disparities, research plays a vital role in developing effective solutions to improve the well-being of individuals and communities.
5. Enhancing human understanding:  
                           Research fosters critical thinking, creativity, and problem-solving skills. By engaging in the process of research, we learn to question assumptions, analyze information objectively, and develop innovative solutions. This intellectual growth contributes to a more informed and engaged citizenry.
The impact of research extends far beyond the realm of academia. It permeates every aspect of our lives, from the products we use to the policies that govern us. Research is the cornerstone of progress, innovation, and a better understanding of the world around us.
![image](https://github.com/user-attachments/assets/550b46e1-eaf0-49f1-af61-0d5d180ec0bf)

