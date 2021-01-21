# global-curricula-input
A repository for curricula documents collected from around the world to be used as input by our curriculum parsing utility.

Source URLs for documents are found in "Curricula Documents.csv".

Documents are stored in /Curricula in the format of /Country/Region/Curriculum Name/Date Downloaded/Subject/Grade

| Label | Notes |
|-----------------|-------------------------------|
| Country | (required) |
| Region | eg. State/Province/City (optional) |
| Curriculum Name | (optional) |
| Date Downloaded | yyyy-mm-dd, automatially added by downloader (required) |
| Subject | (required) |
| Grade | eg. 1, 8-9, K-12 (required) |



Curriculum parsing utility
	
	Summary
		The Curriculum parsing utility takes a CSV file with information on the different curriculum. For each row in the 
		CSV file, the utility will download the curriculum from the source URL and save it to a directory. The directory
		is formatted based on the information given on the curriculum as follows: /Country/Region/Curriculum Name/Date Downloaded/Subject/Grade
		If any of the optional fields are omitted, they will not be present in the directory path.
	
	Requirements
		The CSV files columns must be in the following order: country, region, curriculum name, year, subject, grade, URL
		If any of the required fields are missing, the utility will display the missing element(s), and the row number
	
	usage: 
		./curriculumParsingUtility <FILE>
		
		./curriculumParsingUtility -h
