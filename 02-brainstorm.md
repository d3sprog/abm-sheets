# Three-dimensional Table (Ideas)

## Overview
Since we are modeling an agent-based simulation, the model is a three-dimensional structure, where:
- the 1. dimension are individual agent instances (agent 1, agent 2, agent 3, ...)
- the 2. dimension are agents' properties (property 1, property 2, property 3, ...)
- the 3. dimension is the time progression (step 1, step 2, step 3, ...)

Based on this observation, we can model three two-dimensional spreadsheets, each representing one combination of two dimensions of the three-dimensional model:
1. [Agent-Property view](#the-agent-property-view)
    - rows represent individual agent instances
    - columns represent agents' properties
2. [Time-Agent view](#the-time-agent-view)
    - rows represent time steps
    - columns represent individual agent instances
3. [Time-Property view](#the-time-property-view)
    - rows represent time steps
    - columns represent agents' properties

### The Agent-Property View
The Agent-Property view is the most natural view for the agent-based model. \
It scales only vertically, since the length of the property list is constant, however, new agents can be generated or existing agents can be removed. \
The dimension of time is not visible, however, it can and in fact should be implemented to cache/store previous steps upon which the simulation can be retrospectivelly examined.

<table>
    <thead>
        <th>ID</th>
        <th>x</th>
        <th>y</th>
        <th>speed</th>
        <th>angle</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>5</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>6</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>8</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>9</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>10</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>11</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>165</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>166</td>
                        </tr>
                    </tbody>
                </table>
            </td>
        </tr>
        <tr>
            <td>2</td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>14</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>15</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>3</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>4</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>8</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>9</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>92</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>93</td>
                        </tr>
                    </tbody>
                </table>
            </td>
        </tr>
        <tr>
            <td>3</td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>24</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>25</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>68</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>69</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>3</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>4</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>Step</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>342</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>343</td>
                        </tr>
                    </tbody>
                </table>
            </td>
        </tr>
    </tbody>
</table>

Simplified table (without the time step dimension) looks like this:

<table>
    <thead>
        <th>ID</th>
        <th>x</th>
        <th>y</th>
        <th>speed</th>
        <th>angle</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>5</td>
            <td>8</td>
            <td>10</td>
            <td>165</td>
        </tr>
        <tr>
            <td>2</td>
            <td>14</td>
            <td>3</td>
            <td>8</td>
            <td>92</td>
        </tr>
        <tr>
            <td>3</td>
            <td>24</td>
            <td>68</td>
            <td>3</td>
            <td>342</td>
        </tr>
    </tbody>
</table>

### The Time-Agent View
The Time-Agent view is also quite natural to the way we see agent-based models. \
It scales both vertically and horizontally, since the time moves forward and new agents can be generated as well as existing agents can be removed. \
The dimension of agent properties is not visible, however, it can be stored as a hash map in each cell (for each agent at the given time).

<table>
    <thead>
        <th>Step</th>
        <th>Agent 1</th>
        <th>Agent 2</th>
        <th>Agent 3</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>
                <table>
                    <thead>
                        <th>x</th>
                        <th>y</th>
                        <th>speed</th>
                        <th>angle</th>
                    </thead>
                    <tbody>
                        <td>5</td>
                        <td>8</td>
                        <td>10</td>
                        <td>165</td>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>x</th>
                        <th>y</th>
                        <th>speed</th>
                        <th>angle</th>
                    </thead>
                    <tbody>
                        <td>14</td>
                        <td>3</td>
                        <td>8</td>
                        <td>92</td>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>x</th>
                        <th>y</th>
                        <th>speed</th>
                        <th>angle</th>
                    </thead>
                    <tbody>
                        <td>24</td>
                        <td>68</td>
                        <td>3</td>
                        <td>342</td>
                    </tbody>
                </table>
            </td>
        </tr>
        <tr>
            <td>2</td>
            <td>
                <table>
                    <thead>
                        <th>x</th>
                        <th>y</th>
                        <th>speed</th>
                        <th>angle</th>
                    </thead>
                    <tbody>
                        <td>6</td>
                        <td>9</td>
                        <td>11</td>
                        <td>166</td>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>x</th>
                        <th>y</th>
                        <th>speed</th>
                        <th>angle</th>
                    </thead>
                    <tbody>
                        <td>15</td>
                        <td>4</td>
                        <td>9</td>
                        <td>93</td>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>x</th>
                        <th>y</th>
                        <th>speed</th>
                        <th>angle</th>
                    </thead>
                    <tbody>
                        <td>25</td>
                        <td>69</td>
                        <td>4</td>
                        <td>343</td>
                    </tbody>
                </table>
            </td>
        </tr>
    </tbody>
</table>

### The Time-Property view
The Time-Property view is perhaps the least useful view. \
In this view, we see the time progression, we see the individual agents' properties, however, they are encoded as a list of agents (for instance indexed by the agent's ID). \

<table>
    <thead>
        <th>Step</th>
        <th>x</th>
        <th>y</th>
        <th>speed</th>
        <th>angle</th>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>
                <table>
                    <thead>
                        <th>ID</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>5</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>14</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>24</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>ID</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>8</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>3</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>68</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>ID</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>10</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>8</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>3</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>ID</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>165</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>92</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>342</td>
                        </tr>
                    </tbody>
                </table>
            </td>
        </tr>
        <tr>
            <td>2</td>
            <td>
                <table>
                    <thead>
                        <th>ID</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>6</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>15</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>25</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>ID</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>9</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>4</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>69</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>ID</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>11</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>9</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>4</td>
                        </tr>
                    </tbody>
                </table>
            </td>
            <td>
                <table>
                    <thead>
                        <th>ID</th>
                        <th>Value</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>166</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>93</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>343</td>
                        </tr>
                    </tbody>
                </table>
            </td>
        </tr>
    </tbody>
</table>

## Summary
From my point of view, the most natural way is to use the Agent-Property view in combination with the Time-Agent view due to the below reasons:
1. data analysts need to (?) model the agent's behaviour, run the simulation and get results step by step. The steps therefore need to be cached/stored either way and the output of the simulation should be the list of agents and their property values at each step of the simulation.
2. The Time-Property view does not make natural sense, I cannot think of a reason anyone would need this view for data analysis purposes
3. The Time-Agent view may make sense and can be added as a feature, because it feels quite natural to look at the individual steps of the simulation and compare values between steps.

However, the Time-Agent view scales both vertically and horizontally, potentially resulting in a different number of agents each step, making the spreadsheet view a little bit non-spreadsheet.

A possible addition to the combination of these two views could be further filtering by the final (hidden) dimension.
1. when we are in the Agent-Property view, we could filter by step and see a simplified, two-dimensional table of agents and their properties at the given time step.
2. when we are in the Time-Agent view, we could filter by property and see a simplified, two-dimensional table of only one property per agent of each time step.

The simulation could be run either with certain delay between steps (and visualised using a visualisation module) or at once. \
If the simulation is run at once, we could then switch between the views, filter out further parameters and inspect the simulation from different angles.

## Experimental features
After running the simulation, we could perhaps generate new tables with new values calculated using formulas based on the simulation results. \
For instance, after running the MOVEMENT simulation, we could select two agents (for instance Agent 1 and Agent 2), create a new Time-Property table where the property would be the distance between the two agents calculated using a new formula `DIST(x1, y1, x2, y2)`. In this way, we could inspect the change in distance between two agents as the time progresses.

As far as the "least useful" view is concerned - the Time-Property view, we could perhaps use it to calculate the average position of the flock in each time step. In this way, it could be useful in the final data analysis.

These final tables that we could create and inspect based on the data could be visualised in real time or used for final results.