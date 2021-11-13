# BankMarketingCampaign
The data is related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The classification goal is to predict if the client will subscribe a term deposit (variable y).

### Feature Description
**Bank client data:**
1 - age (numeric)<br>
2 - job : type of job (categorical: 'admin.','blue-collar','entrepreneur', 'housemaid', 'management', 'retired','self-employed', 'services', 'student', 'technician', 'unemployed', 'unknown')<br>
3 - marital : marital status (categorical: 'divorced', 'married', 'single', 'unknown'; note: 'divorced' means divorced or widowed)<br>
4 - education (categorical: basic.4y', 'basic.6y', 'basic.9y', 'high.school', 'illiterate', 'professional.course', 'university.degree', 'unknown')<br>
5 - default: has credit in default? (categorical: 'no', 'yes', 'unknown')<br>
6 - housing: has housing loan? (categorical: 'no', 'yes', 'unknown')<br>
7 - loan: has personal loan? (categorical: 'no', 'yes', 'unknown')<br>

**Related with the last contact of the current campaign:**

8 - contact: contact communication type (categorical: 'cellular', 'telephone')<br>
9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')<br>
10 - day_of_week: last contact day of the week (categorical: 'mon', 'tue', 'wed', 'thu', 'fri')<br>
11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no').<br>
Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model. other attributes:

**Campaign Attributes:**

12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)<br>
13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)<br>
14 - previous: number of contacts performed before this campaign and for this client (numeric)<br>
15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure', 'nonexistent', 'success') social and economic context attributes

**Socio-Economic Attributes:**

16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)<br>
17 - cons.price.idx: consumer price index - monthly indicator (numeric)<br>
18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric)<br>
19 - euribor3m: euribor 3 month rate - daily indicator (numeric)<br>
20 - nr.employed: number of employees - quarterly indicator (numeric)<br>

**Ouput Target Variable**

21 - y - has the client subscribed a term deposit? (binary: 'yes','no')

### EDA
**Total Observations of Numeric variables**<br>
<img src="./Reports/Total_Obs.png" alt="drawing" width="900"/>

**Client Subcribed by Age**<br>
<img src="./Reports/Dist_by_Age.png" alt="drawing" width="300"/>

**Comparing Working and a Breakdown of Each Job**<br>
<img src="./Reports/Job_vs_Working.png" alt="drawing" width="700"/>

**Campaign Duration Data**<br>
<img src="./Reports/Campaign_EDA.png" alt="drawing" width="800"/>

**Do cell phones lead to longer or shorter calls than home phones?**<br>
<img src="./Reports/Telephone_vs_CellPhone.png" alt="drawing" width="1000"/>

**Correlation between all Socio Eco Data**<br>
<img src="./Reports/Socio_corr.png" alt="drawing" width="600"/>

**Other Data**<br>
<img src="./Reports/Other_Data_EDA.png" alt="drawing" width="1000"/><br>

>Previous Outcome is a good predictor, if they have previously converted they are likely to convert again.

**Campaign**<br>
<img src="./Reports/Campaign_by_Y.png" alt="drawing" width="400"/><br>

>Number of times client has been contacted for this campaign. People usually convert within the first couple of calls.

**Previous Calls**<br>

<img src="./Reports/Previous_Calls.png" alt="drawing" width="400"/><br>
>First time call recipients are less likely to convert for this campaign.

**Mean of Y by Month and Day**<br>
<img src="./Reports/Total_Calls_Month_Day.png" alt="drawing" width="1000"/>

**Histogram for all Numeric Variables**<br>
<img src="./Reports/Histograms.png" alt="drawing" width="1000"/>

**Mean Across all groups of Categorical Variables**<br>
<img src="./Reports/Mean_Y_cat.png" alt="drawing" width="1000"/>

**Correlation between all Kept Columns**<br>
<img src="./Reports/Columns_Kept_corr.png" alt="drawing" width="600"/>

**Final KNN Avg Precision**<br>
<img src="./Reports/KNN_AUC.png" alt="drawing" width="1000"/>

