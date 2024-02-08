As seen in [[Weighted Voting]] the relative power of some players are stronger than others and it can be hard to pick out who has the most power. Back in 1965 John Banzhaf III developed a way to calculate the power of players in a weighted voting system.

## Important Terms

1. **Coalition**: This is a set of players who join together and all vote the same way. This can range from just a single player to all players (**Grand Coalition**).
	- The easiest way to define a set of players mathematically is using something called a set. A set can be rearranged in any order.
$$\{P_1, P_2, P_3\}=\{P_3, P_1, P_2\}$$
2. **Winning Coalition**: This is a *coalition* that have enough votes to win the motion. Subsequently there is also a **losing coalition** for the coalition that lost the motion. All *grand coalitions* are *winning coalitions*.
>[!note] Fun fact! as long as there are two or more players in a coalition there is no [[Weighted Voting|dictator]].
3. **Critical Player**: This is a player in a coalition that without their vote the coalition would fail to pass a motion. It can be more formally written as:
$$\text{If } W_{total}-w_{cp}<q \text{ then the player is a critical player}$$
4. **Critical count**: This is a count of the amount of times a player is critical in a coalition
>[!example] Below is an example of what we learned above.
>Here is a weighted voting setup for a mock US Senate where there are 49 Republicans, 48 Democrats, and 3 Independents.
>$$[51: 49, 48, 3]$$
>Below is a table of all possible winning coalitions with the critical player italicized.
>
>| Coalition | Weight |
>| :----: | :----: |
>| {R, D, I} | 100 |
>| {*R*, *D*} | 97 |
>| {*R*, *I*} | 52 |
>| {*D*, *I*} | 51 |
>Looking at the table we can see that all the players have a equal *critical count* of 2.

## Banzhaf Power Index (BPI)

- Let $P_1, P_2, ..., P_N$ be the players in the weighted voting system like normal.
- Let $B_1+B_2+...+B_N$ be the *critical counts* of each respective player and the total of the critical counts be denoted as T.
- Use the following equation to calculate the BPI of each player.
$$\beta_x = \frac{B_x}{T} \tag{1}$$

## Banzhaf Power Distribution

This is how big of a slice of the pie each players BPI has. This is simply just a list of the BPI numbers in order.

>[!note]
> - BPIs all have a common denominator of T so its good practice to keep this common denominator to make comparisons easier.
> - The sum of the Banzhaf Power Distributions will always be 1

## In Summary

>[!summary] Computing the [[Banzhaf Power#Banzhaf Power Index (BPI)|Banzhaf Power Distribution]] 
> - **Step 1**: Make a list of all *winning* coalitions.
> - **Step 2**: In each coalition determine the *critical players* and mark them.
> - **Step 3**: Compute the *critical counts* (B).
> - **Step 4**: Find the total of the critical counts (T).
> - **Step 5**: Compute the Banzhaf power indexes ($\beta$).

## Example

>[!example] In the weighted voting system \[6: 4, 3, 2, 1] determine the Banzhaf power distribution.
>Below is a table with all the possible combinations of coalitions. The winning coalitions are highlighted and the critical players identified.
>
>| Coalition | Weight | Critical Players | Coalition | Weight | Critical Players |
>| :----: | :----: | :----: | :----: | :----: | :----: |
>| $\{P_1,P_2\}$ | ==7== | $P_1,P_2$ | $\{P_1,P_2,P_3\}$ | ==9== | $P_1$ |
>| $\{P_1,P_3\}$ | ==6== | $P_1,P_3$ | $\{P_1,P_2,P_4\}$ | ==8== | $P_1,P_2$ |
>| $\{P_1,P_4\}$ | 5 | None | $\{P_1,P_3,P_4\}$ | ==7== | $P_1,P_3$ |
>| $\{P_2,P_3\}$ | 5 | None | $\{P_2,P_3,P_4\}$ | ==6== | $P_2,P_3,P_4$ |
>| $\{P_2,P_4\}$ | 4 | None | $\{P_1,P_2,P_3,P_4\}$ | ==10== | None |
>| $\{P_3,P_4\}$ | 3 | None |  |  |  |
>Critical counts: $B_1=5, B_2=3, B_3=3, B_4=1$
>Banzhaf power: $\beta_1=\frac{5}{12}, \beta_2=\frac{3}{12}, \beta_3=\frac{3}{12}, \beta_4=\frac{1}{12}$

If you are struggling with how to find the winning coalitions head to [[Subsets and Permutations]] to see a shortcut to finding them!


