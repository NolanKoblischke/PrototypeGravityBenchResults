# Results for a prototype version of Gravity Bench

### Overview

Gravity Bench v1 is a benchmark designed to evaluate the capability of AI models to uncover hidden physics through simulated physics environments. This benchmark specifically focuses on binary star systems, providing a series of physics-related tasks in partially-observable environments that require exploration, complex reasoning and scientific understanding.

### Benchmark Structure

- Dynamic rebound (machine-precision) simulation of the binary star systems
- Questions that require a physical understanding of the simulation and smart observational scheduling. For example:
  - What is the total mass and period of the system?
  - Is the system bounded or unbounded?
  - Is Kepler’s third law satisfied?
    - We can make this scenario OOD by modifying gravitational law to 1/r^2.1
- Multiple versions of observations:
  - Full simulation table provided
    - tabular positions of each star over time provided ot the agent
  - Row-wise observations
    - Agent is provided tabular positions at times it chooses to observe
  - Frame-wise observations
    - Agent is provided an image frame of the simulation from `matplotlib` at times it chooses to observe
    - (Results not yet available)

### Results
Download and open the `HTML` files for an interactive view of the **agent traces** from each baseline agent.

| Model | Version | Percent Correct |
| --- | --- | --- |
| GPT-4o | Full table | 49% |
| Claude 3.5 Sonnet | Full table | 33% |
| GPT-4o | Row-wise | 21% |
| Claude 3.5 Sonnet | Row-wise | 24% |

Here is a visualization of an example simulation the agent must observe and reason about:
![Example](example_binary.gif)