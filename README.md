# Election_Analysis
Defining election's winner using Python and VS code.

## Project Overview
This is an election audit of the tabulated results for U.S. Congressional precinct in Colorado.<br> 
A Colorado Board of Elections employee, Tom, has requested the following parameters to be included in the audit:<br>
  1. The total number of votes cast. 
  2. The complete list of counties involved in the election. 
  3. The total number of votes colleced from each county. 
  4. The percentage of the each county's voters turnout. 
  5. The county with the largest voter turnout in this election. 
  6. The complete list of candidates who received votes. 
  7. The total number of votes each candidate received. 
  8. The percentage of votes each candidate won. 
  9. The winner of the election based on popular vote. 
  
## Resources: 
- Data Source: [election_results.csv](https://github.com/Magzzie/Election_Analysis/blob/main/Resources/election_results.csv)
- Software: Python (3.9.7), Visual Studio Code (1.65.2).
- Code file: [PyPoll_Challenge_starter_code.py](https://github.com/Magzzie/Election_Analysis/blob/main/PyPoll_Challenge_starter_code.py)
- Output text file: [election_analysis.txt](https://github.com/Magzzie/Election_Analysis/blob/main/analysis/election_analysis.txt)

## Summary of Audit Results:
The analysis of the election shows that: 
- There were (369,711) votes cast in this Congressional precint election in Colorado. 
- The votes included in this election data were collected from three counties: 
  - Jefferson county with (38,855) votes accounting for "10.5%" of the total vote. 
  - Denver county with (306,055) votes accounting for "82.8%" of the total vote.
  - Arapahoe county with (24,801) votes accounting for "6.7%" of the total vote. 
- The county that had the largest voter turnout in this election was ***Denver***.
- The candidates were: 
  - Candidate 1: *Charles Casper Stockham*
  - Candidate 2: *Diana DeGette*
  - Candidate 3: *Raymon Anthony Doane*
- The candidate results were: 
  - Charles Casper Stockham received "23.0%" of the vote and (85,213) number of votes.
  - Diana DeGette: "73.8%" of the vote and (272,892) number of votes.
  - Raymon Anthony Doane: "3.1%" of the vote and (11,606) number of votes.
- The **winner** of the election was: 
  - Candidate ***Diana DeGette***, who received "73.8%" of the vote and (272,892) number of votes. 

## Challenge Overview
The challenge demanded a similar analysis of the vote count and percentage for each county, as it was done for the candidates.<br>
In addition, it required saving all the results of this audit as a concise summary in a text file. 

## Challenge Summary 
The election votes analysis using Python code, and VS text editor entailed the use of:
- CSV and OS libraries
- With statements: to open different file objects to read from and write in, examples:<br>
    `with open(file_to_load) as election_data:`<br>
    `with open(file_to_save, "w") as txt_file:`
- For loops: to loop through the rows of data and tally the counts for each county and each candidate, examples:<br> 
    `for row in reader:`<br>
      `candidate_name = row[2]`<br>
      `county_name = row[1]`  
- If statements and membership conditionals: to determine the unique values for both counties and candidates,<br>
  and track the counts for each, in addition to deciding the winner, examples:<br>
    `if county_name not in county_options:`<br>
    `if (turnout > highest_turnout) and (turnout_percentage > highest_percentage):`<br>
    `if (votes > winning_count) and (vote_percentage > winning_percentage):`
- Print statements to get the output of the code in the terminal, examples:<br>
    `print(election_results, end="")`<br>
    `print(winning_county_summary)`
- F-string format: to formulate the analysis results in a concise and organized way in the output file.<br>
    `election_results = (`<br>
    `f"\nElection Results\n"`<br>
    `f"-------------------------\n"`<br>
    `f"Total Votes: {total_votes:,}\n"`<br>
    `f"-------------------------\n\n"`<br>
    `f"County Votes:\n")`
  
## Election-Audit Recommendations Summary
The code used in this project, to analyze the data collected from the congressional precint elections in Colorado,<br>
could be expanded on to include additional objectives, such as:
  - Calculating candidate's votes per county, to determine each county's favored candidate. 

Limitations of the dataset: there is no data on the voting methods used in this election.<br>
Such information would permit further analysis of the popularity of each method in the cohort.<br>

Furthermore, the code built for this project could be repurposed and tailored to analyze other elections,<br>
for example: 
  - Variable names and lists could be changed and appended.
  - Output style and organization could be easily reformatted, by editing the F-strings.

In summary, this is an adaptable code and can be utilized for various analyses on CSV data files.
