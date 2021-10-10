# Research Project for Econometrics 20, Winter 2021

## Authors: Saksham Arora, Foster Burnley, Griffin Kozlow, Sophie Kwon, and Anna Martin

### Abstract 
This paper explores the effects of alcohol consumption on the use of hard drugs, especially in relation to the increase in access to alcohol at 21 years of age, the minimum legal drinking age (MLDA) in the US. To explore this relationship, we created a new data set from the National Longitudinal Study of Youth 1997 (NLSY97), limited to the years 1998-2008, which merges variables related to alcohol consumption and hard drug use. We limited the data to respondents who provided information about their alcohol consumption and hard drug use, meaning substances other than marijuana, such as crack, cocaine, and heroin. Initially, we ran OLS and fixed effects regressions to examine the effects of alcohol consumption on hard drug use, both of which were dummy variables equal to 1 if the respondent had consumed alcohol or used hard drugs since their last interview, the year prior. Some of these models provided statistically significant results, but we felt we didn’t have the full story. Ultimately, by using a regression discontinuity model, we found that alcohol consumption sharply increased at 21 years of age, and hard drug use generally decreased around this same threshold. However, we could not conclude that there exists a discontinuity in hard drug use at 21 years of age, so we cannot definitively claim that alcohol and hard drugs are used as substitutes. All of our estimates are robust to various specifications and clustered by individuals, which will be expanded upon in our Data section.

### Variables
1. `Pubid` : unique id for each respondent \
2. `Demographic Variables` : \
    -`Female` : dummy variable, 1 if assigned as female at birth, 0 otherwise \
    -`Black` : dummy variable, 1 if identified as belonging to the african american race, 0 otherwise 
    -`White` : dummy variable, 1 if identified as belonging to the white race, 0 otherwise \
    -`Hispanic` : dummy variable, 1 if identified as belonging to the hispanic ethnicity, 0 otherwise \
    -`Non_white` : dummy variable, 1 if identified as not belonging to the white race, 0 otherwise \
    -`Other_races` : dummy variable, 1 if identified as belonging to native american, asian american or other races apart from black and white, 0 otherwise 
3. `Age` : continuous variable, age of respondent on day of interview 
4. `Over_21` : dummy variable, 1 if age >= 21, 0 otherwise 
5. `Drugs_dli` : continuous variable, frequency of cocaine/hard drug consumption since day of last interview
6. `Alc_participation_month` : continuous variable, frequency of alcohol consumption in the last month from date of interview 
7. `Smoking_month` : continuous variable, frequency of smoking/cigarette consumption in the last month from date of interview 
8. `Mar_month` : : continuous variable, frequency of marijuana consumption in the last month from date of interview 
9. `Ever_alc` : dummy variable, 1 if respondent said yes to ever consuming alcohol in the chosen time frame of 1998 to 2008, 0 otherwise
10. `Ever_drugs` : dummy variable, 1 if respondent said yes to ever consuming cocaine/hard drugs in the chosen time frame of 1998 to 2008, 0 otherwise
11. `Ever_smoke` : dummy variable, 1 if respondent said yes to ever consuming cigarettes in the chosen time frame of 1998 to 2008, 0 otherwise
12. `Ever_mar` : dummy variable, 1 if respondent said yes to ever consuming marijuana in the chosen time frame of 1998 to 2008, 0 otherwise
13. `Alc_init` : dummy variable, 1 if respondent said yes to consuming alcohol since the date of last interview, 0 otherwise 
14. `drugs_init` : dummy variable, 1 if respondent said yes to consuming cocaine/hard_drugs  since the date of last interview, 0 otherwise 
15. `smoke_init` : dummy variable, 1 if respondent said yes to consuming cigarettes/ smoking since the date of last interview, 0 otherwise 
16. `mar_init` : dummy variable, 1 if respondent said yes to consuming marijuana since the date of last interview, 0 otherwise 
17. `Yrdum` : dummy variable, one for each year between 1998 to 2008.
18. `Region` : categorical variable, 1 for  Northeast (CT, ME, MA, NH, NJ, NY, PA, RI, VT). 2 for North Central (IL, IN, IA, KS, MI, MN, MO, NE, OH, ND, SD, WI), 3 for South (AL, AR, DE, DC, FL, GA, KY, LA, MD, MS, NC, OK, SC, TN , TX, VA, WV), 4 for West (AK, AZ, CA, CO, HI, ID, MT, NV, NM, OR, UT, WA, WY)

**Data processing, cleaning and regression done in STATA by Saksham Arora**.
