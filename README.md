# mental-health-in-tech
*Analyzed OSMI mental health survey data to evaluate the relevancy of mental health (i.e. diagnosis, healthcare coverage, open discourse) within the American tech industry.*

## Overview
The goal of this project is to explore the intersection of mental health and the technology industry by analyzing survey results regarding American workers’ perceptions and frequency of mental illness throughout the past five years. Conducting this analysis allows for greater insight into how mental health is considered within an industry that is commonly known for frequent burnouts and high stress levels. 

Nuances within this general inquiry involves exploring the potential relationships between demographic information (i.e. age, gender, race, and location) and workplace characteristics (i.e. mental health benefits in healthcare coverage, mental health discourse among co-workers and employers) in various workplace environments. 

## Data
The survey data is sourced from Open Source Mental Illness (OSMI) from 2014 to 2019 and is made accessible by Kaggle in a SQLite file (to which we converted to a .CSV file). It is important to note the limitations that exist within this survey, since anyone is able to visit the OSMI website and answer whichever questions they would like. This can lead to (sample/response) biases in the representation of the members within the tech industry.

https://www.kaggle.com/anth7310/mental-health-in-the-tech-industry

## EDA: Highlighted Visualizations

![MH_vs_race](https://user-images.githubusercontent.com/68027568/102305422-a6389d00-3f25-11eb-8eff-84bd763cfc45.png)

![MH_age_distribution](https://user-images.githubusercontent.com/68027568/102305946-c583fa00-3f26-11eb-806b-8c1f5a8232ac.png)

*Note: The age distribution histogram is not a stacked bar chart of proportions (like the others)—these are three overlaid distributions. We did this in order to understand the scale of the three distributions in comparison to each other.*

<img width="1070" alt="Screen Shot 2020-12-15 at 10 39 09 PM" src="https://user-images.githubusercontent.com/68027568/102305730-5d351880-3f26-11eb-9274-ce2e9a9a80cd.png">

## Hypothesis Tests

To reach more conclusive results, our group ran several hypothesis tests to which we compared proportions of individuals impacted by mental health disorders across different cohorts. We ran these tests via randomized permutations of mental health status for each cohort over many simulations to deduce the p-value, assuming each cohort was sampled from the same background population. The p-value was thus calculated by dividing the occurrence of proportions measured as extreme or more extreme than they appeared from this randomized sampling procedure over the number total proportions simulated. 

### Tech Workplace

*H<sub>0</sub>*: The proportion of workers with a mental health disorder is the same for both tech and non-tech workers.

*H<sub>A</sub>*: The proportion of workers with a mental health	 disorder is higher in the tech industry.

*P-value*: 0.032

*Conclusion*: We reject the null hypothesis. There is statistically significant evidence to suggest that there is a greater proportion of individuals in tech have mental health disorders than individuals not in tech. 


### Female vs. Male

*H<sub>0</sub>*: The proportions of males and females with a mental health disorder are the same.

*H<sub>A</sub>*: The proportions of males and females with a mental health disorder are different.

*P-value*: less than 0.0001

*Conclusion*: We reject the null hypothesis. There is statistically significant evidence to suggest that the proportion of females with a mental health disorder is different from that of males. 


### 'Female & Male' vs. 'Other'

*H<sub>0</sub>*: The proportions of those who identify as ‘Male or Female’ and those who identify as ‘Other’ with a mental health disorder are the same.

*H<sub>A</sub>*: The proportions of those who identify as ‘Male or Female’ and those who identify as ‘Other’ with a mental health disorder are different.

*P-value*: less than 0.0001

*Conclusion*: We reject the null hypothesis. There is statistically significant evidence to suggest that the prop. of those who identify as ‘Other’ with a mental illness is different from those who identify as ‘Male or Female.’


### Age Means

*H<sub>0</sub>*: The mean age of individuals with a mental health disorder is the same as the mean age as individuals who do not have a mental health disorder.

*H<sub>A</sub>*: The mean age of individuals with a mental health disorder is different than the mean age as individuals who do not have a mental health disorder.

*P-value*: 0.668

*Conclusion*: We do not reject the null hypothesis. There is no evidence to suggest a statistically significant difference in mean age between those who are diagnosed and those who are not. 
