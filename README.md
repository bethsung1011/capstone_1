# Capstone 1

[Data Analyst Jobs](https://www.kaggle.com/andrewmvd/data-analyst-jobs)


![](img/0.intro.png)



Today I am going to present Glassdoor Data Analyst job posting. 

In the data there are 2253 company job postings with information below.   



## information of the dataset:

  - 2253 job listings scraped from glassdoor
  - Job title 
  - Salary Range 
  - Job Description 
  - Rating 
  - Comapny Name 
  - Location 
  - Headquarter 
  - Size
  - Founded
  - Type of ownership
  - Industry
  - Sector
  - Revenue


## Demand on Data Analysts per State 

![](img/1.data_analysts_job_demand.jpg)



## Top 20 cities Demand on Data Analysts  

<<<<<<< HEAD

=======
>>>>>>> 07bd182f039e121badb115b37922de4e7ec3aed4
![](https://github.com/bethsung1011/capstone_1/blob/main/img/2.Top_20_Cities_for_Data%20Analysts_Job_Demand.jpg)



## State Median Salary Estimate 

![](img/2.states_median.png)


## Salary Range: 24K-190K  

Min Max Salary of Data Analyst job in Glass door in general  

![](img/3.min_max_salary.jpg)

Mean of maximum salary estimate: 89 K 
Mean of minimum salary estimate:  50 K  


## Company generate high revenue 

Company generate high revenue looking for data analyst are :

- Insurance 
- Mining and Metals 
- Aerospace and Defense 
- Telecommunications
- Finance 


![](img/4.Revenue_of_Industry_Sectors_demanding_Data_Analyst.png)

Insurance industry generate most revenue and next is mining. Interestingly Information & Technology is 14th on Revenue generating wise.


## Industrial Sector Demanding Data Analyst

![](img/5.Demand_on_Data_Analyst_per_Sector.jpg)

Of course IT companies look for lots of Data Analyst as we expected. 



## Employee Size Demanding Data Analyst

![](img/5.Employee_Size_demanding_Data_Analysts.png)

Could not find the meaningful relationship between job demand for data analyst and company size(employee size).


## Relationship between Information 

There are numerically measurable data on salary estimate, company rating, company location, industrial sector, and revenue of the company that look for data analysts. 


![](img/6.scatter_matrix.jpg)



## Stastical Test 

Since people who use Glassdoor rate about how good the company is, I wonder how Company rating is positively related to salary or not. Company with high rating pays more??  To answer the question, I conducted hypothesis testing.  
 
 This is scatter plot between company rating and salary estimate. Blue is high / max salary  boundary and organge is low/min saary boundary. 

![](img/6.Glassdoor_rating_and_salary_scatter.jpg)


## hypothesis 1  
    
  ### Null: Company rating and high salary boundary are not positively correlated 
  ### Alternative: Company rating and high salary boundary are positively correlated 


![](img/7.rating_salary_corr.png)


When I conducted Pearson correlation test, it shows 0.05 correlation between Rating and Max Salary and 0.02 correlation between Rating and Min Salary with my original data. Since the dataset is around 2000 samples, we are going to do bootstrapping and conduct correlation test accordingly. 
 

![](img/7.95CI_rating_upper_salary.jpg)

As the result, With 95% confidence interval, I can say bootstrap_salary_upper correlation is from  0.101 to 0.09  
 [0.011347007366033238, 0.09074888578231032 ] 


![](img/8..95CI_rating_lower_salary.jpg)

With 95% confidence interval,  bootstrap_salary_lower correlation is from from –0.02 to 0.07.  
[-0.021413976305863825, 0.07173311436767897] 



### Conclusion:  

* I reject Null hypothesis for company rating and higher salary because  0 is laid outside of 95% confidence interval. I can say High rating company and higher salary may be positively correlated.  

* I failed to reject Null hypothesis since my 0 is laid in 95% confidence interval  and high company rating and lower salary boundary may not be positively correlated. 



## hypothesis 2  

Since it is Glass door shows in their data that what kind of companies (which industry, how many employee they have, how much revenue they generate)  when they look for data analysts, it might be interesting to look at whether high revenue generating companies offer higher salary boundary when they offer a job to data analyst.  

 

### Null - Company revenue and high salary boundary are not positively correlated.  
### Alternative- Company revenue and high salary boundary are positively correlated. I conducted Pearson Correlation with Bootstrapping.  

![](img/9.revenue_salary_corr.png)


![](img/9.95CI_revenue_upper_salary.png)

I got bootstrap_salary_upper correlation is –0.05 to 0.02 
[-0.05725261745947094, 0.022103673678014562 ] 

![](img/10.95CI_revenue_lower_salary.png)

I got bootstrap_salary_lower correlation is from –0.05 to 0.02 
[-0.054171562416393065, 0.026781082702684506]  



### Conclusion:  

I failed to reject the null hypothesis for both higher and lower salary estimate with high revenue companies because 0 correlation is laid inside of 95% confidence interval.  Both correlations are less or equal in general; company makes high revenue generating and data analyst salary estimate are not positively correlated.   


## Texas vs California vs New York 

Since CA, NY, TX are the highest Data Analysts demanding states in Glassdoor, I spent sometime to look into company rating and average salary estimate for those states. 

Glassdoor average review for the company is 3.7. Interestingly Texas is lower than statewide average and California is higher than average.   

![](img/11.company_rating.png)

In case of salary estimate, California pays most and Texas pays the least. 

![](img/12.average_salary.png)

Due to the difference on salary gap, I made a table of the cost of livings adjustment comparison reflecting average salary per state.

![](img/12.COLA.png)



## Moving forward …. 

I would like to investigate job description and job titles and correlation to salary estimate. Although I could find key words and rank about how many times the keywords are mentioned but I could not spot the information column that mentions the word. With Natural Language Process, there will be wider spectrum to explore about this data and to find more meaningful relationship.       



