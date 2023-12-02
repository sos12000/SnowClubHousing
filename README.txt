This is how to use the SnowClubHousing.exe file:
- Double click the .exe file to run it 
INPUT:
- Please locate the input format and duplicate it
Please note:
	- The input must contain two sheets of exact names "Requests" and "Housing Officer Groups"
	- The Requests input sheet must contain three columns with header names "Name", "Request 1", "Request 2"
		- A person's name should be identical when in the "Name" Column and when being requested in either Request column
		- NICKNAMES WILL RESULT IN SEARCH MISSES LEADING TO YOU NOT GETTING YOUR REQUEST
	
	- The Housing Officer Groups sheet must contain three columns with header names "ID", "Max Size", "Officers"
	- The ID column is where the name of the house will be, you can have a little fun with this names
	- The Max Size column is where you put the house specific max number of occupants to that specific house
		- Please ensure the sum of max size is greater than, but close to, the number of people going
	- The Officer column is where you put a house specific list of officer names 
		- Officer names MUST be seperated by a comma AND a space! DO NOT include leading or EXTRA spaces
		Good = "Billy Bob, Jane Doe"
		Bad = "Billy Bob Jane Doe" or "Billy Bob,Jane Doe" or " Billy Bob , Jane Doe"
		- Officer names should be EXACTLY the same names as seen in the "Requests" sheet (Capitalization should not matter)
	- A house MAY contain no officers, but this does not gaurentee that it will have officers once filled. It is best to place the officers in each house before execution.
	- Officer names must be in the Names column of the Requests sheet, even if no requests are given in column Request 1 or Request 2
	
- Once data has been properly filled in on both sheets, please SAVE the input file
- Drag and drop this input file from file explorer to the first box under the text "Drag and drop entry file in the box"
- Type a new name for the output file in the box under the text "Name new Housing List"
	- Providing a name of a output file that already exists will OVERWRITE its contents
	- If providing the name of an existing file, please ensure this file is CLOSED before running
	- DO NOT include a file format when naming
	Good = "Test Name"
	Bad = "Test Name.xlsx"
- Once both the input file and new file name boxes have been filled, please press the "Create New Housing List" button
	- This may take a moment as the Random Pick algorithem runs 100 times to find the highest satisfaction order

OUTPUT:
- The output file should be a .xlsx file with the name previously provided located in the same directory as the .exe file
- The output file should have a number of sheets, one for each algorithem used.
- Houses will have names listed under each sorted in alphabetical order
- Statistics are listed under each house with Overall statistics for the algorithem on the right
	- These can be mostly ignored unless you are curious about satisfaction of the houses
- The most important statistic is the "Overall" "R1 or R2 Satisfaction"
	- This statistic tells you what percentage of the all the people in each house were placed with atleast one of their requests
- From here you may select any of the housing lists
	- The algorithem with the highest "Overall" "R1 or R2 Satisfaction" rate is recommended


RERUN:
This program should run fine over successive inputs of properly formatted input files if you would like to rerun or produce multiple outputs

CONFIGURATION:
- You may change the number of tries the random pick algorithem attempts by modifying the config.txt file, changing the 100 in "NumberOfRandomIterations=100" to another number
- You may change the output destination of the program by changing the "OutputPathname = "output" " line