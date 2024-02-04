So how do you know which voting method is the best for your election? Well if you just have two candidates then there is no real problem with any method. With three or more candidates, there is no clear best method. In an election with more than three candidates there are always limitations.

## Arrows Impossibility Theorem
Kenneth J. Arrow came up with these **fairness criteria** to help determine whether an election is fair.
1. **The Majority Criterion**: The candidate with the majority of first place votes should win the election
>[!important]
>How [Borda Count Method](Borda_Count_Method.md) violates Majority criterion
>
>| Number of voters | 6 | 2 | 3 |
>| ---- | :----: | :----: | :----: |
>| 1st | A | B | C |
>| 2nd | B | C | D |
>| 3rd | C | D | B |
>| 4th | D | A | A |
>
>A is the winner by having the majority of the first place votes. Using Borda count the resulting happens: A = 29 points, B = 32 points, C = 30 points, and D = 19 points. So according to Borda, B should be the winner.

>[!caution]
>This is a violation!

2. **The Condorcet Criterion**: The Condorcet candidate (the candidate that wins the most amount of pairwise comparisons) should win the election
>[!important]
>How [Plurality Method](Plurality_Method.md) violates the Condorcet criterion
>
>| Number of voters | 49 | 48 | 3 |
>| ---- | :----: | :----: | :----: |
>| 1st | R| H | F |
>| 2nd | H | S | H |
>| 3rd | F | O | S |
>| 4th | O | F | O |
>| 5th | S | R | R |
>
>Using [Pairwise Comparisons](Pairwise_Comparisons.md) the Condorcet candidate is found to be H. Yet using Plurality the candidate that should win is R.

>[!caution]
>This is a violation!
 
3. **The Monotonicity Criterion**: The outcome of the election should not change if the elected candidate is moved up on a preference ballot
>[!important]
>How [Plurality-with-Elimination](Plurality-with-Elimination.md) violates the Monotonicity criterion
>This is the preference table before any votes change. Using Plurality-with-elimination, candidate C is the winner.
>
>| Number of voters | 7 | 8 | 10 | 2 |
>| ---- | :--: | :--: | :--: | :--: |
>| 1st | A | B  | C | A |
>| 2nd | B | C  | A | C |
>| 3rd | C | A | B | B |
>
>But maybe some people changed their votes. In this case the last column decided to switch A and C. Not the winning candidate is B.
>
>| Number of voters | 7 | 8 | 10 | 2 |
>| ---- | :--: | :--: | :--: | :--: |
>| 1st | A | B  | C | C |
>| 2nd | B | C  | A | A |
>| 3rd | C | A | B | B |

>[!caution]
>This is a violation!

4. **The Independence-of-irrelevant-alternatives (IIA) criterion**: If candidate X is the winner in the election normally then the result shouldn't change if one or more of the losing candidates were to have not been in the race.
>[!important]
>How [Pairwise Comparisons](Pairwise_Comparisons.md) violates the IAA
>In this original preference schedule performing a Pairwise comparison results in candidate A being the winner. 
>
>| Number of voters | 2 | 6 | 4 | 1 | 1 | 4 | 4 |
>| ---- | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
>| 1st | A | B | B | C | C | D | E |
>| 2nd | D | A | A | B | D | A | C |
>| 3rd | C | C | D | A | A | E | D |
>| 4th | B | D | E | D | B | C | B |
>| 5th | E | E | C | E | E | B | A |
>
>Candidate C dropped out of the race. Now applying Pairwise comparisons results in candidate B winning. 
>
>| Number of voters | 2 | 6 | 4 | 1 | 1 | 4 | 4 |
>| ---- | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
>| 1st | A | B | B | B | D | D | E |
>| 2nd | D | A | A | A | A | A | D |
>| 3rd | B | D | D | D | B | E | B |
>| 4th | E | E | E | E | E | B | A |

>[!caution]
>This is a violation!

Each of the examples provided above is just one way that each method violates Arrow's fairness criteria. Below is a full summary table of each of the voting systems covered and what they violate.

| Criterion | Plurality | Borda Count | Plurality-with-<br>elimination | Pairwise<br>comparisons |
| ---- | ---- | ---- | ---- | ---- |
| Majority | Pass | Fail | Pass | Pass |
| Condorcet | Fail | Fail | Fail | Pass |
| Monotonicity | Pass | Pass | Fail | Pass |
| IIA | Fail | Fail | Fail | Fail |
