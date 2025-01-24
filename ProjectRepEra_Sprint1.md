# Project Rep Era : Sprint 1  
## Last Update Date:  01.23.2025  



*Sprint 1 aims to create a data report reflecting how Congress voted on the TikTok ban.  The programming used to generate the report will be a core component of the congressional monitoring application to come.  Software development has a lifecycle referred to as Agile.  Iterative steps take place, building value additions each step of the way towards building a big picture.*  

https://www.congress.gov/legislative-process  

## TODOS:  
 
voting records reveal an lis number.  (A congress member primary key or something of this sorts).  


- [ ] Find this number and augment.  


## Sprint 1 achievements:  
- Created and executed ETL stack extracting congressional data for each Congressional body -- House of Representatives and Senate -- for Congressional bills.  
- Explored and built code "report" function for iterating vote data on TikTok voting case.  
    - this data presented as well-formed XML and is automatable.  
    - report isn't really a report, just an exercise in prototyping possibility.  This direction is achieveable and workable.
    - Explored Senate bill vote record and found substantial variation from above-mentioned line.
       - All vote data is not created equally.

## Sprint 1 thoughts: Epilogue.  
- Work on integration of Stage 2 data and complete for Sprint 2.  
- Work on integrating React component as a 'View' embedded in an Observable Framework container.  
    - Data will be manually delivered to this stage after excecuting Manual triggered data pull in Sprint 2 and exercising Stage 2 augmentation.  





## At face value, 7521 seems the ticket to find out what's up.  It's not, see further below.  

H.R.7521 - Protecting Americans from Foreign Adversary Controlled Applications Act  
118th Congress (2023-2024)  

https://www.congress.gov/bill/118th-congress/house-bill/7521  

https://en.wikipedia.org/wiki/Restrictions_on_TikTok_in_the_United_States#Biden_administration_(2021%E2%80%932025)  

On March 13, 2024, the United States House of Representatives passed the Protecting Americans from Foreign Adversary Controlled Applications Act (H.R. 7521) with largely bipartisan support from Democrat and Republican-party representatives.[44][45] It would ban operations related to the app completely within the country unless ByteDance makes a qualified divestiture as determined by the US president.[46] After modifications, the act passed the House again[47][48] and the United States Senate[49] before it was signed into law by Joe Biden on April 24, 2024. The ban went into effect on January 19, 2025. An additional 90 days could be issued on the deadline.[50]  


https://www.congress.gov/bill/118th-congress/house-bill/7521/all-info  


* The Protecting Americans from Foreign Adversary Controlled Applications Act did not pass Congress and become law.  The spirit of the ban got hoisted into an Appropriations bill seen below.  *  


Related: 

H.R.815 - Making emergency supplemental appropriations for the fiscal year ending September 30, 2024, and for other purposes.
118th Congress (2023-2024)  

https://www.congress.gov/bill/118th-congress/house-bill/815  

https://www.congress.gov/bill/118th-congress/house-bill/815/text  




## *snippet from bill text that enacts the ban*  

DIVISION H-- PROTECTING AMERICANS FROM FOREIGN ADVERSARY CONTROLLED APPLICATIONS ACT

Protecting Americans from Foreign Adversary Controlled Applications Act

(Sec. 2) This division prohibits distributing, maintaining, updating, or providing internet hosting services for a foreign adversary controlled application (e.g., TikTok). However, the prohibition does not apply to a covered application that executes a qualified divestiture as determined by the President.

Under the division, a foreign adversary controlled application is an application directly or indirectly operated by (1) ByteDance, Ltd., TikTok, their subsidiaries, successors, related entities they control, or entities controlled by a foreign adversary country; or (2) a social media company that is controlled by a foreign adversary country and determined by the President to present a significant threat to national security. (Here, a social media company excludes any website or application primarily used to post product reviews, business reviews, or travel information and reviews.)

For the purposes of this division, a foreign adversary country includes North Korea, China, Russia, and Iran.  

A qualified divestiture is a transaction that the President has determined (through an interagency process)

would result in the relevant foreign adversary controlled application no longer being controlled by a foreign adversary, and
precludes the establishment or maintenance of any operational relationship between the U.S. operations of the relevant application and any formerly affiliated entities that are controlled by a foreign adversary (including any cooperation with respect to the operation of a content recommendation algorithm or a data-sharing agreement).
The prohibition applies 270 days after the date of the division’s enactment. The division authorizes the President to grant a one-time extension of up to 90 days to a covered application when the President has certified to Congress that (1) a path to executing a qualified divestiture of the covered application has been identified, (2) evidence of significant progress toward executing such qualified divestiture of the covered application has been produced, and (3) relevant legal agreements to enable execution of such qualified divestiture during the period of such extension are in place.

Additionally, the division requires a covered foreign adversary controlled application to provide a user with all available account data (including posts, photos, and videos) at the user's request before the prohibition takes effect. The account data must be provided in a machine-readable format.

The division authorizes the Department of Justice to investigate violations and enforce its provisions. Entities that that violate the division are subject to civil penalties for violations. An entity that violates the prohibition on distributing, maintaining, updating, or providing internet hosting services for a covered application is subject to a maximum penalty of $5,000 multiplied by the number of U.S. users who have accessed, maintained, or updated the application as a result of  the violation. An entity that violates the requirement to provide account data to a user upon request is subject to a maximum penalty of $500 multiplied by the number of U.S. users impacted by the violation.

(Sec. 3) The division gives the U.S. Court of Appeals for the District of Columbia exclusive jurisdiction over any challenge to the division. A challenge to the division must be brought within 165 days after the division’s enactment date. A challenge to any action, finding, or determination under the division must be brought with 90 days of the action, finding, or determination.



## Technical details of retrieving ballot results  

NOTE: lis member number.  
voting records reveal an lis number.  Find this number and augment  




https://www.congress.gov/bill/118th-congress/house-bill/815/all-actions  


- 03/07/2023-5:29pm	House	On motion to suspend the rules and pass the bill, as amended Agreed to by voice vote. (text: CR H1126)  
- 04/23/2024	Senate	Senate agreed to the House amendment to the Senate amendment to H.R. 815 by Yea-Nay Vote. 79 - 18. Record Vote Number: 154.  

https://www.senate.gov/legislative/LIS/roll_call_votes/vote1182/vote_118_2_00154.htm#top  

Pages displaying voting summary have an xml link for downloading well-defined vote data.  


## Report format  + schema  





    .roll_call_vote  
       .congress {content: "118"}  
       .session {content: "2"}  
       .congress_year {content: "2024"}  
       .vote_number {content: "154"}  
       .vote_date  {content: "date-placeholder"}  
       .vote_question_text   {content: "text-placeholder"}
       .vote_result_text  {content: "result-placeholder"}
       .vote_title  {content: "title-placeholder"}
       .vote_result  {content: "vote-result-placeholder"}
       .document
         .document_type  "HR"
         .document_number:  815  
         .document_name  H.R. 815  
         .document_title
         .document_short_title
       .members  
           .member  
           .last_name {content: "Baldwin"}  
           .first_name {content: "Tammy"}  
           .party {content: "D"}  
           .state {content: "WI"}  
           .vote_cast{content: "Yea"}  
           .lis_member_id {content: "S354"}








