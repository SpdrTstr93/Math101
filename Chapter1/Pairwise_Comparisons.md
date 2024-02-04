Also known as **Copeland's Method**, use a preference schedule to count how many times candidate X is ranked above candidate Y. The winner gets 1 point, the loser gets 0, and if it is a tie they each get 0.5 points. After all comparisons are complete then whichever candidate has the most amount of points wins.

>[!important]
>Pairwise comparisons using example table
>
>| Number of voters | 14 | 10 | 8 | 4 | 1|
> | --- | :---: | :---: | :---: | :---: | :---: |
> | 1st | A | C | D | B | C |
> | 2nd | B | B | C | D | D |
> | 3rd | C | D | B | C | B |
> | 4th | D | A | A | A | A |

| Pairwise Comparison | Votes | Winner |
| :--- | :--: | :--: |
| (1) A vs B | A: 14 votes<br>B: 23 votes | B |
| (2) A vs C | A: 14 votes<br>C: 23 votes | C  |
| (3) A vs D | A: 14 votes<br>D: 23 votes | D |
| (4) B vs C | B: 18 votes<br>C: 19 votes | C |
| (5) B vs D | B: 28 votes<br>D: 9 votes | B |
| (6) C vs D | C: 25 votes<br>D: 12 votes | C |
**Total Points**: C = 3, B = 2, D = 1, A = 0

This method always ends up choosing the [Condorcet candidate](Fairness_Criteria_and_Arrow's_Impossibility_Theorem.md), when there is one, as the winner. In everyday life through, this method is not used much at all. If you want to figure out how many comparisons you need to make you can use the following formula.
$$
\frac{N(N-1)}{2}
\tag{1}
$$
