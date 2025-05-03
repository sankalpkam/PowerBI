# Churn Analysis

### Dashboard Link : 
https://app.powerbi.com/groups/me/dashboards/093b0303-af8a-43c4-bbe5-e808853d8df0?experience=power-bi&clientSideAuth=0
## Problem Statement

This dashboard helps the bank to understand their customers better. It helps the bank know if their customers are satisfied with their services. Through different ratings, they get to know their improvement area, & thus they can improve their services by identifying these area. It also lets them know the churned rate, thus since by using this dashboard they have identified this problem, they can further work on factors responsible for these churns.


Also since target rate is 15% and the churn rate is 20.4% , thus they must try to reduce it.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present.
- Step 5 : For calculating balance, we made groups. so as to calculate age and credit score we made groups to identify as per the index values. 
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various ratings, thus in order to represent ratings, a new visual was added using the three ellipses in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for two fields named "churned", "Not churned.
- Step 9 : Two card visuals were added to the canvas, one representing total number of customers & other representing churned rate
           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
           Although, by default, while calculating average, blank values are ignored.
- Step 10 : A bar chart was also added to the report design area representing the number of churned customers. While creating this visual, field named "Gender" was also added to the Legends bucket, thus number of customers are also seggregated according the gender. 
- Step 11 : Donut chars was used to represent different ratings mentioned below,

  (a) Total customers by gender

  (b) Total customers by activity(Active/Not Active)
  
  (c) Total customers by Credit card owned
  
  (d) Total customers by country
  
  (e) Total customers by product
  
  (f) Graphical representation of Total customers and rate of age groups

  (g) Graphical representation of Total customers and churned rate by Credit score groups
  
  (h) Graphical representation of Total customers and churned rate by Account balance
  
   
In our dataset, Some parameters were assigned value 0, representing those parameters are not applicable for some customers.

All these values have been ignored while calculating average rating for each of the parameters mentioned above.

- Step 12 : Calculated column was created in which, customers were grouped into various age groups.
        
- Step 13 : New measure was created to find total count of customers.

Following DAX expression was written for the same,
        
        Count of Customers = COUNT(customer data(customer[ID]))
        
A card visual was used to represent count of customers.
        

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 10K

   Number of satisfied Customers (Female)= 4543 (45.43%)

   Number of satisfied Customers (Male) = 5457(54.57%)

   Number of active customers = 5151 (51.51%)

   churned rate = 20.40%


           thus, higher number of customers of age group 51-60 are churned (56.20%).
