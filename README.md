# Recidivism Machine Learning Project
Exploratory Data Analysis and Machine Learning Model Development of Recidivism Data


## Abstract
This study uses machine learning to develop a random forest model predicting success rates for individuals post-release, achieving 73% accuracy. Feature importance analysis identified program attendance as a crucial factor, emphasizing the effectiveness of rehabilitation programs in facilitating post-release employment and reducing recidivism. Positive impacts include enhanced financial stability, skill development, and social integration. Challenges such as barriers to employment and program effectiveness variations underscore the need for comprehensive support services.
Results demonstrate the model's effectiveness through feature importance validation, optimal n-estimator selection, and cross-validation. Key takeaways underscore the dependence of program efficacy on attendance, highlighting the random forest model's utility in analyzing feature importance. This research contributes valuable insights for policymakers, criminal justice practitioners, and researchers working towards reducing recidivism and improving rehabilitation outcomes. Future research aims to explore additional factors influencing rehabilitation program efficacy and complementary interventions for comprehensive support

## Methodology
Data Acquisition:
We decided to utilize a dataset from the National Institute of Justice. There are a variety of benefits in using this dataset, including but not limited to:
1. Dataset is updated, with the most recent update on July 15, 2021.
2. Dataset is very large, with 25.8k rows each representing a different person.
3. Dataset has many variables that could affect success rates, with 54 different factors recorded. 4. Dataset does not contain many missing data.
5. Dataset is from a trusted source.
Data Preparation and Cleaning:
Since the dataset did not have many errors or missing data in the beginning, not much preparation had to be done before beginning analysis.
1. Casted correct data types for variables such as Dependents, Prison_Years, the various types of Prior_Arrest and
Prior_Conviction, and others.
1. Solved problem regarding data being saved as more than... or less than... instead of a value.
2. Determined presence of missing, invalid, and null data. There were very few numbers of null data, so those rows
could be disregarded if columns were to be used in final model creation.
Initial EDA:
1. We plotted race distribution since historically models have been known to show racial bias. We disregarded race in our final model to avoid racial bias, especiallAy sinbce osnlty brlaack acndtwhite are represented in this data (no other
3. Finally, we looked at gang-affiliation, and most people were not gang-affiliated 3 years post-release.
Feature Selection:
We chose a variety of features for our model, paying careful attention to those that may contribute to racial bias. For that reason, while we disregarded values such as race, we included items like age, prior convictions, and education to see what programs would have the greatest possibility of reducing recidivism rates across all released people.
Model Development:
We developed three different models for this data set to determine which was the most effective. KNN-algorithm, Random forest, and Support vector machine.
Hyperparameter Tuning:
In the case of the k-NN algorithm, we tested a range of values for the number of neighbors. We found generally increasing the number of neighbors increased the accuracy of the model. For k-NN, we consistently achieved an accuracy of 0.73 at around 38 neighbors. For the random forest algorithm, we tested 100, 500, and 1000 for the number of estimators. For all three values, we found the model had an accuracy of around 0.73, so we consider them about the same. Finally, SVM has the hyper parameters of C and gamma, and through a grid search, we found a C of 0.1 and 1 resulted in an accuracy of 0.72.
Decision:
At face value, the k-NN and random forest algorithms performed about the same. Since we want to evaluate the importance of different features, such as program attendances, we will only be able to do so using the random forest algorithm as it is not possible for the k-NN model. For this reason, we will continue with the random forest algorithm.

## Impacts

Several studies indicate a positive correlation between employment rehabilitation programs and reduced recidivism rates. Successful reintegration into the workforce can positively influence an individual's life trajectory, contributing to lower recidivism rates and safer communities. However, there are still considerations to be made regarding the effectiveness of programs and other barriers that those released could face.
Positive Impacts:
1. Employment and Financial Stability: Access to stable employment provides individuals with an alternative
means to support themselves financially, reducing the likelihood of returning to criminal activities to meet their
needs.
2. Skill Development: Rehabilitation programs often offer job training, skill development, and education,
empowering individuals with marketable skills that increase their employability and opportunities for legitimate
work.
3. Social Integration: Employment can facilitate social integration, helping individuals establish positive social
networks and a sense of belonging within their communities, reducing isolation and exposure to criminal
motivation to lead a law-abiding life.
influences.
4. Sense of Purpose: Having a job can provide a sense of purpose and direction, promoting self-worth and
Abstract
Considerations:
1. Barriers to Employment: Individuals with a criminal history often face challenges in securing employment due to
stigmatization, lack of skills, or legal barriers.
2. Program Effectiveness: The effectiveness of employment rehabilitation programs can vary based on the quality of
the program, the types of services offered, and individual participant needs.
3. Support Services: Comprehensive support services (counseling, mentorship, housing assistance) alongside
employment assistance are crucial for sustained success.
4. Long-Term Sustainability: The long-term impact of employment programs may depend on ongoing support
after individuals secure employment to prevent relapse into criminal behavior.
Overall, there are many benefits to improving rehabilitation programs regarding employment, but further steps must be taken to ensure an individuals proper return and integration into society, Improving rehabilitation programs without taking the steps to improve other aspects of an individual’s life such as housing or mental health would prove to be ineffective. Although our model demonstrates that rehabilitation programs can help individuals retain jobs, other steps must also be taken.

Created in collaboration with Alton Banushi and Miti Patel
