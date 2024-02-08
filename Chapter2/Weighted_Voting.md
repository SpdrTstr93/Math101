A **weighted voting system** is any voting system where the voters do not have an equal say in an election. In this section, we will consider voting systems that only have *yes-no* votes, known as **motions**.

## The Three Elements of Weighted Voting

1. **The players (P)**: These are the voters in a weighted voting system. They could be people, institutions, districts, states, or even countries. The total number of players will be called **N**.
2. **The weights (w)**: This is the weight of the votes that each player has. The total number of votes will be called **V**.
3. **The quota (q)**: It is simply the number of votes to pass a motion. You can think about this like the majority although it could be greater than or less than the majority.

## Notation

For a weighted voting system with **N** players: 
$$[q: w_1, w_2, ..., w_n](\text{with   }w_1\geq w_2\geq ...\geq w_N) \tag{1}$$

## Important Terms

>[!important]
>EXAMPLE: Suppose four partners $(P_1, P_2, P_3, P_4)$ issue 20 shares for their new company. $P_1$ buys 8 shares, $P_2$ buys 7 shares, $P_3$ buys 3 shares, and $P_4$ buys 2 shares. They agree that two-thirds of the partnership's votes are needed to pass a motion. 
>
>This system can be written as follows. Total votes, V=20, and the quota, q=14. The final system can be written as \[14: 8, 7, 3, 2].

>[!tip]
>What happens if we vary the quota in the example above?
1. **Anarchy**, q=10
	- This quota is to small which allows for there to be a stalemate if $P_1$ and $P_4$ both vote yes, 10 votes, and $P_2$ and $P_3$ vote no, also 10 votes. This happens because the quota is ***below*** the majority.
2. **Gridlock**, q=21
	- Now the quota is ***above*** the total number of votes which is a mathematical impossibility and no motion will ever be passed. 
So in order to not have **Anarchy** or **Gridlock** happen we should restrict our quota to the following:
$$V/2 < q \leq V \text{ } (\text{where }V=w_1+w_2+...+w_N) \tag{2}$$
>Lets define a few more terms.
3. **Few Votes, Much Power**, \[19: 8, 7, 3, 2]
	- In this case the quota is high enough to where all members must agree in order for a motion to pass. This could be simplified down to \[4: 1, 1, 1, 1] and work exactly the same.
4. **Many Votes, Little Power**, \[30: 10, 10, 10, 9]
	- In this case $P_4$ has no power in any motions as long as $P_1, P_2, \text{and }P_3$ vote against them.
5. **Dictators**, \[11: 12, 5, 4]
	- This case is self explanatory, $P_1$ is able to pass a motion all by themselves. A dictator exists when a single player as the same or more votes as the quota.
6. **Veto Power**, \[12: 9, 5, 4, 2]
	- In this case, $P_1$ is known as a "spoiler". All the other players do not have enough votes to pass a motion, which means that $P_1$ has veto power. They are a required vote for a motion to pass.
	- Here is a formal definition. In this case *w* represents the player of interests weight.
$$V-w < q \tag{3}$$
