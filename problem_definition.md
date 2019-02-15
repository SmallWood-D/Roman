Problem definition

I will try to define a new variant of MAPF problem, MAAPF (Multiple Agent Adversarial path finding) is very similar to the origin problem of MAPF with one change the path between positions are under threat – meaning there is a possibility of agent destruction – stop participant in the solution.

Terminology
Graph G = (V, E), graph define the map (area, zone) , and A – agents (a_i).
Vertices – all possible positions.
Edges – connection between two position* each edge has a time and a threat value.
Time defined t > 0; Threat defined 0 < p < 1.

Agents n agents (a_0… a_n) each agent has start and target point (a_i,s_i,t_i). 
Path – (〖s_i v〗_i…v_j t_i) represent all the vertices agent travers between start and target positions.
Time concept in path is for each vertex in the path has a serial time unit from 0… n.
Start position is 0 and target position is the last step for the specific robot.
All the agents step one step at a time. 
There is a possibility the agent will stop moving for one step or more in that case the path will contain the same vertex number of times, 〖(…v〗_i,v_i,v_i…).

*Between each two vertices there is only one edge.

Input 
Graph and agents (G, A).
Target function - The function use to approximate a value from vertex to the target vertex of an agent.
f: (v, t) -> R.
The value returned (score) will be use to pick the edge in every step.

MAAPF target
Find P non-conflicts path for each agent from start to target position. 
The output should be as minimal or close to minimal as possible.
The catachrestic of a path is time and survivability chance.
Both need to be minimalize as possible.

No two agents can be in the same vertex in the same time.

