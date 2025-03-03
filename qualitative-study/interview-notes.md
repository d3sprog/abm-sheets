# Interview Notes

## Paul Harrington
February 6, 2025

*"One of the benefits of Excel, as you probably know, is just the whip attitude of it, you know, this kind of interactive, reactive programming environment. The ability to mix data and formulas/programming in the same environment is extremely attractive."*
 
Paul Harrington

- defining constants in cells
- creating named variables (symbolic domain)
- using lambdas for everything

## James Geddes
December 12, 2024

### Key Takeaway
Why do you want to avoid time steps?

*"I guess because once you set the rows to time steps, you have lost a dimension of your spreadsheet and so now everything is one-dimensional and everything about the dynamics has to be embedded in a single formula and that can get really complicated, so I was trying to get away from not having to do that for as long as possible. You've only got two dimensions, and if you use one for time, everything else becomes miserable."*

Dr James Geddes

### Solutions

#### Task 1
Each agent has a speed attribute and we calculate the agents' positions at time `t` as `speed * t`.

#### Task 2

##### First Attempt
The first attempt was more of an analytical approach, where the time at which each agent has finished the race was calculated as `time_at_finish = finish_line / speed`.

##### Second Attempt
Columns represented time steps and rows represented agents. There were two tables, one represented the agents' positions unconstrained and the second one represented agents' positions contrained (stopped after crossing the finish line).

#### Task 3
There was one more table defibed for the changing speeds.

#### Task 4
Same as task 3 but there was one more aggregated calculation, which calculated the positions of agents that did not win at the time step where the one winning agent has crossed the finish line.

### Problems
The issue with multiple tables for each attribute is that when we need to add more agents, not only we need to define the new agents for each of the table but to move the tables so that we can define the new agents.

### Closing discussion
James thinks it would be a useful addition to embedd the third dimension of continuous time into the software system to enable travelling through the time bi-directionally and enable cell self-referrencing in a more complex and useful manner.