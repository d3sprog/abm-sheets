# ABM Sheets User Study

**Author**: Bc. Tomáš Boďa \
**Supervisor**: Mgr. Tomáš Petříček, Ph.D.

ABM Sheets is a research project that aims to create a new software system that allows the users to model agent-based simulations using a well-know spreadsheet interface resembling popular spreadsheet software systems such as Microsoft Excel. This allows for the modeling of agent-based simulations without prior programming knowledge, only using a simple spreadsheet interface controlled by click & drag interactions.

This user study aims to find gaps and limitations of current spreadsheet software (Microsoft Excel) in order to build the most suitable & usable software system interface for this problem.

In this study:
1. you will first be briefly introduced to the concept of agent-based modeling
2. you will be asked to model four simple agent-based models in Microsoft Excel
3. we will dicsuss your approach and thinking process to the solution of the previous tasks

## Agent-based Modeling
Agent-based modeling is a simulation technique used in many scientific fields to model and understand complex simulations. In an agent-based model, a system is modeled using a set of autonomous entities called agents. An agent represents a single, meaningful unit of a system, such as a person in an epidemic or a bird in a flock. Each agent individually assesses the current situation and makes decisions based on a set of defined rules. The main idea of agent-based modeling is to describe the system from the perspective of its constitutent units. This approach allows us to uncover novel emergent phenomena within the system that were previously unknown or considered improbable.

In technical terms, the simulation consists of three main dimensions:
1. agents - a set of agents in the simulation
2. attributes - a set of attributes for each agent representing the rules based on which the agent decides
3. time - the time progression of the simulation represented in individual steps

For instance, in a pandemic simulation, an agent could have properties such as `x` and `y` coordinates, `speed` and `angle` for movement purposes, `neighbours` that represents a set of neighbouring agents and is calculated based on the agents' positions and finally `infected` that represents whether the current agent is currently infected or not. The `infected` attribute could change based on whether any of the neighbouring agents is infected.

## Assignment
The assignment is to model a very simple agent-based simulation in Microsoft Excel. The simulation represents a race, where individual agents represent runners that run from the starting point to the finish line. These agents move with a certain speed and the first agent to cross the finish line wins. This assignment comes in four steps, each gaining more difficulty.

> [!IMPORTANT]
> We would like to ask you to briefly document your thinking process within these assignments, most importantly what was challenging or too difficult to simulate. These information help us discover the gaps and limitations of the current spreadsheet software that is essential for this research project.

> [!WARNING]
> We advise you to not spend more than 1-2 hours on the tasks. If you cannot come up with a solution within a reasonable time frame, please document what challenges you faced and on which problem you stumbled.

### Part 1 (Tireless runners)
Generate a set of agents, where each agent has a position (in one-dimensional space, meaning only one number) and speed. Each agent starts at point 0 and is assigned a random speed between 1 and 5 (which is constant throughout the race). In each new time step, each agent's new position is calculated as its previous position plus its speed. There is no finish line, the agents move indefinitely, based on how many steps we run the simulation for.

> [!TIP]
> Create a table where columns represent individual agents (and the values their positions) and rows represent time steps. In this way, the positions of agents in the new time step can be calculated from positions in the previous time step (the row above it).

### Part 2 (Being competitive)
In this task, we introduce the finish line - a constant number, for instance 100. If an agent crosses the finish line, it finishes the race and does not move anymore (its position stays the same, equal to the finish line position). Additionally, if an agent's left or right neighbour finishes the race (crosses the finish line), the agent stops moving and instead of displaying its position it displays STOP.

This task simulates the behaviour that an agent loses the race if any of its neighbouring agents win, therefore stops moving.

### Part 3 (Let's change it up)
In this task, we want the speed of each agent to change in each time step. Each agent is assigned a random speed at the beginning of the race. However, in each time step the speed is incremented or decremented by a random small amount, however, not going below 1. The rules stay the same, so if an agent crosses the finish line, it wins and stops moving or if any of an agent's neighbours win, it stops.

This task introduces a new speed attribute to each agent, which is similarly to the agent's position recalculated in each new time step from the value of the previous time step.

### Part 4 (One winner to rule them all)
In the final task, we want all agents to stop moving if any agent wins the race. So if any of the agents reaches the finish line, we want all the other agents to stop and instead of displaying their new position, we display STOP.

This task represents a realistic race where we only care about the winner (the first one to cross the finish line) and we do not care about the order of the remaining agents, which lost the race.

## Next Steps
When you are finished with the tasks, please send us an e-mail with your solution (Excel `.xlsx` file). We will contact you shortly about the next steps, such as invite you to a short Zoom call where we will discuss your approach to the solution.

## Contact Us
In case of any questions or unclarities regarding the tasks or the study in general, do not hesitate to contact us at our e-mail addresses:
- Tomáš Boďa - [tominoboda@gmail.com](mailto:tominoboda@gmail.com).
- Tomáš Petříček - [tomas@tomasp.net](mailto:tomas@tomasp.net)