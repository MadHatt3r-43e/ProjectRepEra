# Voting record Schema.  
## Eric Strickland  
### 01.28.2025  


// JSON target definition.  

'Vote meta'  (Object with the below values as NVP.  )  
	Congress 
	Session  
	Chamber  
	Legislation Number ((FK))
	Legislation Title (Laken Riley Act)
	Roll Call Number  
	Vote Question
	Action Date  
	Action Time  
	Vote Type
	Vote Result  
'Vote Data'  (Object containing array named RecordedVotes.  )  
  RecordedVotes []  
    Member Full Name  ie.  Angela Alsobrooks (D-MD)  	
	Member First Name  
	Member Last Name  
	Party  
	State  (string)  
	State ID (int) // lookup in ETL from ____.  
	Vote Cast  
	LIS Member ID  
	Name ID 
	

*Notes on what's present in xml from Case study that at this point shall be ignored*  
// xml data present in source.  

	// House
	<vote-totals>, <totals-by-party>, <totals-by-vote>

	// Senate  
	<ammendment>, <count>, <tie_breaker> 

// Voting Info 

 
	
	




