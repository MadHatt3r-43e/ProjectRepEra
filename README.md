# PROJECT REP ERA  ⬛🐍⬛  
#### Last Update Date:  01.23.2025  


*A fun, safe place for collaborating on building data applications to pursue 'Swiftie interests'*  

### SEEKING.  
I'm seeking activist-minded content creators to collaborate with me:
- give input/feedback during the application development life cycle.  
- Develop with the team an intimate understanding of high-level congressional activity.  
- A law student, reader, or constitutionally-intrigued and energetic person to help cognate the significance of legislation and augment the application dataset by using the application.  ie.  Tag a bill as a women's right's threatening piece of legislation.  
- Social media creators that would use the tool as creators to say, as an example,  "HEY!  Mr. Cotton!  You SUCK HARD!" and loudly share this opinion and why you have it.  


Please engage with content on TT or Bluesky to express interest.

## 119th Congress.  
Listing of current legislators  
https://github.com/MadHatt3r-43e/ProjectRepEra    (data folder in this repo)  


## Boilerplate stuff  

*Unicode for emojis*  

Black box: U+2B1B  
Snake box: U+1F40D  

'Project REP ERA' aims to increase visibility of Congressional activity.  

Other locations...  

Discord:  
https://discord.com/channels/1331018805618540645/1331018805618540648  


BlueSky:  
@softwareswiftie.bsky.social  

GitHub:  (a software code repository store for development collaboration.  a good place for devs to share what they're building)
https://github.com/MadHatt3r-43e/ProjectRepEra

Observable:  



## Overview  
I am building a data application for monitoring Congressional activity.  This software building activity will be subsequently referred to as 'Swiftie interests'.   

I would like to find some creators interested in particicating in the thought process of ideating all the things an application should have.  

## Details  

1.  The application will read from the online congressional registry of activity, retrieve and prepare for the application to use.  
2.  The application will contain data information for every congress person in the United States.  
3.  When legislation is introduced, when it is to next be acted upon is stated in the Congressional record.

## Desire  
Create a system allowing congress persons to know we see their activity; for us to apply pressure via digital communication to be adherent to constitutional principles **before** they vote.  

- Keep a scorecard on legislators' voting.  
- Brodcast to media and content followers the actions of legislators.  


## Presidential Executive Orders  
https://federalregister.gov/presidential-documents/executive-orders  

## Legislation  
Example source:  
https://www.congress.gov/bill/119th-congress/house-resolution/7  

Resolution data:  
https://www.congress.gov/119/bills/hres7/BILLS-119hres7ih.xml  

## 117th Congress  
Hres 22  Impeachment of Donald Trump.
https://www.congress.gov/117/bills/hres24/BILLS-117hres24rds.xml 


# Technical notes for Eric  

## ETL execution stack location.  
C:\ProjectRepEra_ETL  
node index.js to execute job.  



Legislation iterates multiple process states as it proceeds to the President.  
Legislation Status  

Introduced  
Committee Consideration  
Floor Consideration  
Failed One Chamber  
Passed One Chamber  
Passed Both Chambers  
Resolving Differences  
To President  
Became Law  
	

A == Create
B == Copy Code.
C == Change Code.
D == Execute.  

Data Extraction ethos: Week 1, iteration two completed on Thursday.  
ETL to run on T, R of each week as Week N, iteration X.  


- [x] First data extraction successful.  

Regarding HRB, as of 01.23.2025, the ETL stack for grabbing HR bills is complete as only three states of the data are present.  

Regarding SB, as of 01.23.2025, the ETL stack for grabbing Senate bills is complete as only five states of the data are present. 

HRB.  
    - A. B. C. D. Introduced  
	- A. B. Committee Consideration  
	- A. B. C. D. Floor Consideration 
	- A. B. Failed One Chamber  
	- A. B. C. D. Passed One Chamber  
	- A. B. Passed Both Chambers  
	- A. B. Resolving Differences  
	- A. B. To President  
	- A. B. Became Law  

SB.  
    - A. B. C. D. Introduced  
	- A. B. Committee Consideration  
	- A. B. C. D. Floor Consideration 
	- A. B. Failed One Chamber  
	- A. B. C. D. Passed One Chamber  
	- A. B. C. D. Passed Both Chambers  
	- A. B. Resolving Differences  
	- A. B. C. D. To President  
	- A. B. Became Law  
	


 
