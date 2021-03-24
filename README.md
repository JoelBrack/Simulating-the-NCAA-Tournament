# Simulating-the-NCAA-Tournament
Simulating the 2020 NCAA Tournament

I was very upset that my favorite sporting event, March Madness, was cancelled this year. It didn't feel right for there not to be a champion named, so I used some of the time I would be watching the games to make a basic simulator of the tournament. A brief explanation with code included can be found on the pdf.


### 2021 Update: ###
This year, instead of running my algorithm once and declaring a champion, I used it to calculate probabilities of each team advancing in the tournament. Using the same logic as before to predict tournament games, I simulated the entire tournament 10,000 times after each day concluded and results were finalized. By dividing the number of apperances a team had in each round by 10,000 , I could determine their probability of reaching that round. 

One interesting problem here was what to do as the tournament shrank without changing a lot of code each time I updated. At the end of the day, the tournament is not always balanced: for example, some teams could already be in the Elite 8 while some Sweet 16 games have yet to be played. My solution to account for this was to create a fake team named 'Out'. I added them to the KenPom file and gave them an adjusted efficiency of -10000 (for reference, the lowest rated real team has an ADJ EFF of -40.5). Simply put, this made up team named 'Out' was so bad that they would lose every single game they played. Now for updates I just replace each team name that lost with the team 'Out' and all my probabilities calculate correctly.

I posted the list of the Top 16 teams ordered by 'Champion' probablitiy on my Twitter (@WVStatsGuy) each day. It's been fun watching the list evolve as the madness continues, especially in this very upset heavy year! I've also added some examples in the 2021 update folder.
