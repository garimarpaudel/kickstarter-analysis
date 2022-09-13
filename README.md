# Fundraising Campaign Launch Date Affects the Theater/plays Fundraising Success.
## 1. Overview
#### The fundraising for Louise’s play Fever was very successful in very short amount of time and fundraising team wonders, if the fundraising campaign launch date affects the fundraising activity. The purpose of this analysis is to determine how the different fundraising campaign launch date affects the success and failure of fundraising in theater/plays.

## 2. Analysis and Challenge
#### We were provided with Kickstarter_Challenge datasheet which contained raw data of fundraising campaign launch data, fundraising goals, and pledged amount for Theater/plays. The campaign launch date was provided as serial number where we had to use UNIX conversion to convert date as serial number to the date format that is mm/dd/yyyy. Following UNIX formula was plugged in Excel Cell to generate mm/dd/yyyy date from serial number: 

 	Date created conversion=((“Date_as_serial_Number”/60/60)/24)+DATE(1970,1,1)
  
#### Converted campaign launch date was formatted to get date in mm/dd/yyyy and Excel formula 

        Years=years(Date created Conversion) 
        
 #### was used yo geterate campaign launch daye in YYYY format
 
 ### 2.1 Outcomes Based on campaign launch Date
 #### After the launch date was converted to format YYYY date format, pivot table was created to study overall fundraising outcomes based on campaign launch date, by selecting entire dataset where no filter were applied. In the column section of pivot table field, column outcomes were dragged and values of count of column outcome were used for counting of successful, failed and live fundraisings. In the pivot table fields, year was dragged into rows and changed to month in order to understand the success, failure and cancellation of fundraising goals based on month. The following pivot table was generated.
 
 <img width="279" alt="image" src="https://user-images.githubusercontent.com/108683284/189793208-53cf10df-1638-476c-b3c0-7c96aae0c27a.png"> <img width="160" alt="image" src="https://user-images.githubusercontent.com/108683284/189793285-ebc8b1d9-69eb-4f69-838f-b4837d7663c7.png">
 
 ### 2.2 Theater outcomes Based on Campaign launch Date
#### Subsequently, pivot table was created to study theater outcomes based on campaign launch date, by selecting entire dataset where table was filtered by Parent category (_theater_)and YEARS to analyze the fundraising outcomes as success, failure and, canceled. In the column section of pivot table field, column outcomes were dragged and values of count of column outcome were used for counting of success, failure and cancellation of fundraisings. In the pivot table fields, year was dragged into rows and changed to month in order to understand the success, failure and cancellation of fundraising goals based on month. The following pivot table was generated.

 <img width="217" alt="image" src="https://user-images.githubusercontent.com/108683284/189791959-d64243b5-34cf-482c-856a-81a18fb35f42.png"> <img width="158" alt="image" src="https://user-images.githubusercontent.com/108683284/189793369-3e6af4d0-c572-4d73-b38a-f4fe952e131b.png">
 
 ### 2.3 Outcomes Vs Goal
 #### There were 12 different fundraising goals for goals in dollar amount ranging from less than $1000.00 to more than $50,000.00 to find out number of successful, failed and canceled outcomes. We used the condition COUNTIFS to find the successful, failed or canceled outcomes based on plays which we used later to find the percentage successful and failed. The number of successful, failed, and canceled outcomes were calculated using following formula in Excel.
 
     No of successful= COUNTIFS(Kickstarter!$D$2:$D$4115,”<1000”, Kickstarter!$R$2:$R$4115,”*plays*”, Kickstarter!$F$2:$F$4115,”*successful*”)
#### For calculation of failed, and canceled simply "*successful*" was replaced by failed and cancled and the goal condition was changed accordingly. After number of successful,failed and cancled were determined, the sum of total project was calculated using SUM function as follows and dragged down throughout the columns.

        Total projects=SUM(Number successful:Number Failed:Number Canceled)
 #### Percentage successful and percentage failed was calculated using following formula in Excel:
        Percentage Successful=(Number Successful/Total Projects)*100
        Percentage Failed=(Number Failed/Total Projects)*100
        
 #### There were zero counts of number canceled,thus, percentage would be zero and no calculation would be required. 
 #### After the calculation following table was generated. 
 <img width="601" alt="image" src="https://user-images.githubusercontent.com/108683284/189798503-490b96c9-5db5-4274-8ff1-59d6a0f048d5.png">

### 2.4 Challenge
#### The calculation of outcomes Vs Goal was challenging to me sa there were multiple conditions to be satisfied for example, dollar amount goal, subcategory of plays, and outcomes of successful, failed and cancled, i struggled couple of times to figure out why i was not able to generate the graph as illustrated in the module. Since, we have large data set and multiple conditions to be satisfied there is always a change to have error and this turned out to be huge challenge in this work. 


## 3. Results
### 3.1 Conclusions from Theater outcome by Launch date
#### The result generated demonstrates that in the month of May, the number of successful fundraising campaign for theater is in its peak. As we move forward towards june through december , the success of fundraising for theater sharply declined by more than 60%. This indicates that, when season changes from winter to spring, there is high number of people interested in theater plays and more inclined to donations for fundraising campaigns. 

#### There is no significant change in failed outcomes of fundraising throughtout the year which indicates that failed outcomes could be the result of the theater act whose story,characters, and acting were not appealing and interesting to the people..

### 3.2 Conclusions from outcomes based on goals
#### The result generated from outcome based on Goals indicates that it is easier to raise funds that is lower in amount than raising higher amounts. As the fundraising goal amount increases the percentage of successful fundraising decreased this indicates that fundraising goals of higher amount is difficult. However, for fundraising amount between $35000.00 to $44999.00 was more success compared to  amount between $5000.00 to 34999.00. This increment in the fundraising despite being the higher amount could be due the goog play that fundraising is for.

### 3.3 Limitation of this data set
#### the limitation of this dataset is there is no reviews and ratings for any category and subcategory for which fundraising campaign was conducted. If there were reviews and ratings for each category and subcategory it would provide strong validation of the data set for fundraising based on campaign launch date and campaign fundraising goal. So far, the data set left us speculating the reasons for the successful, failed and canceled outcome. The dataset on reviews and rating would help us strongly corroborate our analysis. 

### 3.4 Other possible tables/Charts
### The other possible charts and graphs we could have used to illustrate the outcomes would be bar graph which is easily readable and provides more insights on how the outcomes are differing based on launch date and fundraising goal. 



    

 
 


 







