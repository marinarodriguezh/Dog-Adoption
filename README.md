# Dog-Adoption
Project developed for Advanced Knowledge in Spreadsheets in UC3M

In this project I tried to simulate a web page that gives you the number of dogs available for a given breed. When someone introduces the breed that wants to adopt and the state (from the United States) they are from, different data will appear.
I decided to compare mixed and pure breeds since people wanting to adopt may be looking for a specific dog. Obtaining the results from a dataset containing information about dogs that were given for adoption in the United States. After a cleansing process, I decided that the most important data entries to achieve our goal were the dog and organization ids, primary and secondary breeds, if they are a mixed breed, age, sex, size, special needs, shots, name, status, day they were given for adoption (posted), contact city, contact state and a brief description.
I used different sheets to get what I was looking for. All Dogs is the one containing the data entries used in this project. In StatesMixed and StatesPure, there are pivot tables, about mixed breeds and pure breeds respectively. These were meant to count the number of dogs from the different breeds that are in each state. I did the same thing with Age Mixed, Age Pure, SexMixed and SexPure, but focusing in the dogs’ age and sex and counting them in the same way as in the States ones. In Months there are two pivot tables counting the number of dogs that were given for adoption in each month. And the Dashboard will show:

- The total number of dogs that are up for adoption.
- A dropdown menu to select the wanted breed.
- A dropdown menu to select the state where they want to adopt.
- Today’s date.
- Two tables, one showing the number of dogs in the selected state and with the breed
but that are mixed, and the other the same but pure breed.
- Another two tables, also showing mixed and pure breed, but in the US, in case the
person is not satisfied with the information obtained about the specific state. It shows the state where there are more dogs of that breed, the age that predominates and the sex that predominates (in the total, not only the predominant state).
- Two line graphs showing the number of dogs given up for adoption each month, again mixed and pure breed.

First, to get the total number of dogs, I used the function COUNT and today’s date, TODAY. Then to fin the number of dogs from the given breed and state I used the functions VLOOKUP and MATCH, so it has to look in the pivot tables for the two values given (breed and state). If there are not any dogs in that state, the box will get highlighted in red. To get the predominant State, Age and Sex in the US, I also used the VLOOKUP function, but in this cases in the other pivot table sheets we also used the INDIRECT, ADDRESS, ROW, MATCH and MAX functions, so from the name of a breed it will be able to find, for instance, the state in which there are more dogs. And to get the number of dogs I used VLOOKUP and MAX. Finally, for the graphs I used the pivot tables in Months to be able to see number of dogs that were given for adoption each month and that way showing that the best months to adopt one are July, August and September because there is more variety and there is a higher probability of finding the desired breed. You can also observe that the number of mixed breed dogs that are abandoned/given for adoption is much larger than the number of pure breeds.
