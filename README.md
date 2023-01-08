# Overview of Election Audit
The goal of this audit was to see which canidate won the election with the total votes, and percentage of votes they received. The election commission has also requested that we compile the voter turnout for each county, percentage from each county out of the total count, and the county with the highest turnout.

# Election Audit Results
## County Data
The total amount of votes casted in this election were 369,711. Their was a total of 3 counties (Jefferson, Denver, Arapahoe) and with these totals:
Jefferson: 10.5% (38,855)
Denver: 82.8% (306,055)
Arapahoe: 6.7% (24,801)

The county with the largest turnout was Denver with 306,055 votes, which accounted for 82.8% of the total votes.

## Caniddate Data
Charles Casper Stockham: 23.0% (85,213)
Diana DeGette: 73.8% (272,892)
Raymon Anthony Doane: 3.1% (11,606)

The data above shows how many votes each canidate received, along with the percentage of the votes based off the total. As you can see from the data above, Diana DeGette won the vote with 73.8% (272,892 votes) of the votes going to her. 

# Election Audit Summary
The code used for this analysis can be used for for any election given some small modifications. 

## 1rst code
As long as the data is given in a Csv format, we can use this code to grab the total amount of votes in a given election.

<img src= "https://github.com/DAsInDavid1/Module_3_Challenge/blob/main/Total_vote_counter.png" width=30% height=30%>

In the first line the csv file is opened, and then read with the .reader function. We then go past the header row with the "header = next(reader)" line and finaly we get to the "for loop". For every row with data in it past the header, it will add 1 to the total_votes counter to see the total votes casted. So if we get another election data sheet with a vote in each colomn, we can easily see how many total votes were casted.

## 2nd code
Another code we can use for other elections is this one to count the total votes for each county (can be modified to count for each canidate).

<img src= "https://github.com/DAsInDavid1/Module_3_Challenge/blob/main/County_vote_counter.png" width=50% height=50%>

This code will first see every every county listed in the county_votes dictionary, and since we previously listed each county in it, it knows that thier are 3 counties we need to keep track of. The C-votes = county_votes[county] line will add up all the votes casted in that county. Next the we will get the percentage of the votes casted in that county by using C_votes / total_votes * 100. We make sure to have the votes as float variables since percentages are always floats. Nest we seee each coutny results using the dictioanry {county}, having the percentage of the county as C_vot_percentage come out to 1 decimal point with .1f. then we make sure the total votes coutned in that county with C_votes has a comma to cleary indicate when the vote is in the thousands. The very last "if" statement shows the winnning county by going through all them and if one county is bigger then the other, then that county becomes "largest_county_turnout" variable.

These codes will easily be able to show the total number of votes, along with how many votes each county casted for any election.

