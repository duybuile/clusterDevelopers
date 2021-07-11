# Cluster developers
### Problems 
Identify different clusters of developers who have the same behaviours on Jira. This would help understand
- Developers who work in the same team
- Developers who have the same role (Testers/Developers/Managers)

### Data: 
1) Jira data: a connection from developer to a task (and a project)
2) Effort on task: effort data from developers on different tasks
3) Effort on repository: effort data from developers to different repositories

### Approach:
#### Graph definition
1) Define a graph with
  - Vertex: a developer or a task
  - Edge: a connection between a developer to a task
  - Weight: number of commits associated to a task/effort associated with a task
2) All the 0-weight edges are trimmed off to reduce the complexity of the network

#### Algorithms:
- **Fast greedy**: a bottom-down hierarchical approach to optimise the modularity
- **Walktrap**: random walk 
- Label propagation
- Info Map

### Some notes:
**Modularity**: measures the strength of division of a network into modules

### Conclusion
**Fast greedy** is the best algorithm with a high modularity and fast execution.
