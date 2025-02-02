# PROJECT REP ERA  ⬛🐍⬛  
#### Last Update Date:  01.28.2025  


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
	

01.28.2025  x == RUN.
x	- A. B. C. D. Introduced  
x 	- A. B. C. C. Committee Consideration  // BUG fixed in this job.  
x	- A. B. C. D. Floor Consideration 
	- A. B. Failed One Chamber  
x	- A. B. C. D. Passed One Chamber  
	- A. B. Passed Both Chambers  
	- A. B. Resolving Differences  
	- A. B. To President  
	- A. B. Became Law  

SB.  
x   - A. B. C. D. Introduced  
	- A. B. Committee Consideration  
x	- A. B. C. D. Floor Consideration 
	- A. B. Failed One Chamber  
x	- A. B. C. D. Passed One Chamber  
x	- A. B. C. D. Passed Both Chambers  
	- A. B. Resolving Differences  
x	- A. B. C. D. To President  
	- A. B. Became Law  
	
	
01.30.2025  x == RUN.  Stage 1.  
HRB.
x	- A. B. C. D. Introduced  
x 	- A. B. C. C. Committee Consideration 
x	- A. B. C. D. Floor Consideration 
	- A. B. Failed One Chamber  
x	- A. B. C. D. Passed One Chamber  
	- A. B. Passed Both Chambers  
	- A. B. Resolving Differences  
	- A. B. To President  
	- A. B. Became Law  

SB.  
x    - A. B. C. D. Introduced  
x	- A. B. Committee Consideration  
x	- A. B. C. D. Floor Consideration 
	- A. B. Failed One Chamber  
x	- A. B. C. D. Passed One Chamber  
x	- A. B. C. D. Passed Both Chambers  
	- A. B. Resolving Differences  
x	- A. B. C. D. To President  
x	- A. B. C. D. Became Law  	

01.30.2025 Run Stage 2 proto .  
Run HR_Intro && SB_Intro through stage 2.  
- [x] Copy intro filenames into 'orchestrating function'.  
- [x] run on HR & Senate Intro.