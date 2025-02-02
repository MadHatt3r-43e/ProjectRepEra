# Project Rep Era.  
## Last Update Date:  01.25.2025  
### Eric Strickland.  

# Congressional Record data shapes:  External and internally defined.  

HR Bill .csv file deconstruction.  
 
Column Number
1					Legislation Number	
2					URL	
3					Congress	
4					Title	
5					Sponsor	
6					Party of Sponsor	
7					Date of Introduction	?
8					Committees	
9					Latest Action		A.  // un-pivot into collection
10					Latest Action Date	A.  // These work as a tandem and are 'unique' or can be unique to the state.  
		
		
{
 "Cosponsors" : [
 {
   "Cosponsor" : "Mary",
   "State" : "WA"
 },
 {
   "Cosponsor" : "Joe",
   "State" : "ID"
 }
 ]
}		
					// unpivoted into a collection.  
					//Cosponsors exist between Latest Action Date to Number of Cosponsors.  
		Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	Cosponsor	
					
					Number of Cosponsors  // this column number will be variant.  Will be max of largest number of cosponsors for dataset.  This will be a critical number in the dataset to determine where you're at column-wise.  
					

		// un-pivoted.  
		Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	Subject	
		
		// Related bills needs to be un-pivoted into a collection.  
		Number of Related Bills	  This number indicates how many Related Bill, Related Bill Relationships Identified by pairs.
		Related Bill	Z
		Related Bill	Y
		Related Bill Relationships Identified by	Z
		Related Bill Relationships Identified by	Y
		Related Bill Latest Action	Z
		Related Bill Latest Action	Y
		
		Latest Summary	
		Amends Bill	
		Date Offered	
		Date Submitted	
		Date Proposed	
		
		Amendment Text (Latest)	// This may not be present, but will likely return or become present while still at this state.  
		Amends Amendment




## Standardized json schema

Legislation Number	// PK.  
URL	Congress	
Title	
Sponsor	
Party of Sponsor	
Date of Introduction	
Committees	
LatestActions []  
	Latest Action
	Latest Action Date
Cosponsors  []
  Cosponsor
	Field as Imported  
	(calculated columns)
Number of Cosponsors
Subjects []
	Subject 
Number of Related Bills.  
Related Bills  [] 
	Related Bill 
		Legislation Number  
		Related Bill relationships Identified by.  
		Related Bill Latest Action.   
Latest Summary	
Amends Bill	
Date Offered	
Date Submitted	
Date Proposed	
Amendment Text (Latest)	// this may be present or not present at state introduced.  
Amends Amendment  

+ Create designated augmentation columns for future use.  



# Augmented columns (even if null at Transform stage)  
Extracton Date    
Data Source Type:  House, Senate.  
BillTextAdditionDate  
ETLDate  







## NOTES:  


### HRB Analysis.  

Intro -> Floor -> Received in Senate:   is a typical workflow.  
Intro -> Floor -> Received in Senate, Refer to Committee: is a typical workflow.  


*These below two columns update when entering state* Herego, The pair need to be embedded into an [] of pairs of objects. Latest Action  
Latest Action Date  


# Senate comparison.  
Senate .csv source verified same as HoR.  

