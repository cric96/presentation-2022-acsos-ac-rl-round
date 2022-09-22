 
+++

title = "Addressing Collective Computations Efficiency"
description = "A Hugo theme for creating Reveal.js presentations"
outputs = ["Reveal"]
aliases = [
    "/guide/"
]
+++


{{% slide preload=true background-iframe="net.html"%}}

# Addressing Collective Computations Efficiency {.r-fit-text}
## Towards a Platform-level Reinforcement Learning Approach {.r-fit-text .accent}
**Talk @ ACSOS 2022** 
{.accent}

🎤 *Gianluca Aguzzi*, Roberto Casadei, Mirko Viroli

📧 [gianluca.aguzzi@unibo.it](mailto:gianluca.aguzzi@unibo.it)

---

# Collective Adaptive Systems {.accent}
## Context {.highlight}
{{% row %}}
{{% fragment class="col" %}} 
#### Many Networked Agents
{{< image height="25" src="/network.png" >}} 
{{% /fragment %}}
{{% fragment class="col" %}} 
#### Collective Behaviour  
{{< image height="25" src="/ci.png" >}} 
{{% /fragment %}}
{{% /row %}}
{{% fragment %}}
## Challenges {.highlight}
- Distribution
- Uncertainties
- Global-to-local mapping
{{% /fragment %}}

---

# Motivating example

## Distributed and resilient sensing {.accent}
### Use cases
- Monitoring wild fires in forests
- Crowd engineering
- Avalanche monitoring
- Agriculture monitoring system

{{% row %}}
{{% col %}}
{{< image height=30 src="/crowd.png"  >}}
{{% /col %}}
{{% col %}}
{{< image height=30 src="/swarms.jpg"  >}}
{{% /col %}}
{{% col %}}
{{< image height=30 src="/wild-fire.jpg"  >}}
{{% /col %}}
{{% /row %}}

---
# How
## Collective pattern {.accent } 
### Building blocks for CAS applications {.highlight}

{{% row %}}
{{% fragment class="col" %}}
#### Gradient Cast
```scala
def diffuse(center, data, accumulator)
```
{{< image height=30 src="/network-downstream2.png"  >}}
Broadcast information from *sink* nodes
{{% /fragment %}}

{{% fragment class="col" %}}
#### Data collection
```scala
def collect(path, accumulator, data)
```
{{< image height=30 src="/network-upstream.png"  >}}
Collect data into *sink* nodes
{{% /fragment %}}

{{% fragment class="col" %}}
#### Sparse Choice
```scala
def leaderElection(grain)
```
{{< image height=30 src="/leaders.svg"  >}}
Distributed leader election
{{% /fragment %}}
{{% /row %}}
{{% fragment %}} {{< fa thumbs-up >}}  {{% accent c="**Self-organising & self-stabilising blocks**" %}} {{% /fragment %}}  

---
# High-Level specification
## General schema {.accent}

{{% col class="r-stack" %}}
{{% fragment class="fade-in-then-out" index="0"%}} {{< image height="30" src="/leaders.svg">}} {{% /fragment %}}
{{% fragment class="fade-in-then-semi-out" index="1"%}} {{< image height="30"  src="/network-downstream2.png">}} {{% /fragment %}}
{{% fragment class="fade-in-then-semi-out" index="2"%}} {{< image height="30"  src="/network-upstream.png">}} {{% /fragment %}}

{{% fragment  index="3" %}} {{< image height="30"  src="/network-regions.svg">}} {{% /fragment %}}
{{% /col %}}
{{% col class="r-stack" %}}
{{% fragment class="fade-in-then-out w50" index="0" %}} 
```scala
val centers = leaderElection(grain)
```
{{% /fragment %}} 

{{% fragment class="fade-in-then-out w50"  index="1" %}} 
```scala
val centers = leaderElection(grain)
val pathTo = diffuse(centers, 0, _ + connectionRange())
```
{{% /fragment %}} 
{{% fragment class="fade-in-then-out w75" index="2" %}} 
```scala
val centers = leaderElection(grain)
val pathTo = diffuse(centers, 0, _ + connectionRange())
val regionPerception = collect(pathTo, sense("perception"), accumulator)
```
{{% /fragment %}} 
{{% fragment class="w75" index="3" %}} 
```scala
val centers = leaderElection(grain)
val pathTo = diffuse(centers, 0, _ + connectionRange())
val regionPerception = collect(pathTo, sense("perception"), accumulator)
diffuse(centers, centerDecisionUsing(regionPerception), identity)
```
{{% /fragment %}} 
{{% /col %}}

---

{{% slide transition="slide" %}}

## Execution Model {.accent}

{{% row %}}

{{% col %}}
### Behaviour {.highlight}
**Loop** of three phases:

*Sense* <i class="fa fa-arrow-right"></i> *Compute* <i class="fa fa-arrow-right"></i> *Act*

{{< image height="30" src="/single-agent-rev-3.png">}}
- Sense deals with *neighborhood* information retrieval & *environment* perceptions
- Compute performs the *main logic* of the application
- Act executes action following the result from Compute phase
{{% /col %}}

{{% col %}}
### Scheduling {.highlight}
- *Message-based*
  - Execution triggered by messages received from the other
- *Sensor-based*
  - Changes in the **environment** *trigger* execution 
- *Time-Based*
  - With a certain rate, nodes perform an execution step 
- Event-based

{{% /col %}}
{{% /row %}}

---

{{% slide auto-animate=true %}}
# On {{% highlight c="Collective" %}} Computing Efficiency
## Goals 

## Approaches

---


{{% slide auto-animate=true %}}
# On {{% highlight c="Collective" %}} Computing Efficiency
- Same *Global* specification (e.g., Distributed Sensing & Act)

## Goals 

## Approaches

---

{{% slide auto-animate=true %}}
# On {{% highlight c="Collective" %}} Computing Efficiency
- Same *Global* specification (e.g., Distributed Sensing & Act)
- Several *Execution* strategies

## Goals 

## Approaches

---

{{% slide auto-animate=true %}}
# On {{% highlight c="Collective" %}} Computing Efficiency
- Same *Global* specification (e.g., Distributed Sensing & Act)
- Several *Execution* strategies
- Collective Execution Strategies **influence** the *Global* result
  
## Goals 

## Approaches

---
{{% slide auto-animate=true %}}
# On {{% highlight c="Collective" %}} Computing Efficiency
- Same *Global* specification (e.g., Distributed Sensing & Act)
- Several *Execution* strategies
- Collective Execution Strategies **influence** the *Global* result
## Goals {.accent}
1. Reduce power consumption {{% highlight c="{{< fa fa arrow-right 2 >}} Green computing" %}}
2. Improve **convergence time** to the desired *emergent*


 *Multi-objective* nature


## Approaches

---

{{% slide auto-animate=true %}}
# On {{% highlight c="Collective" %}} Computing Efficiency
- Same *Global* specification (e.g., Distributed Sensing & Act)
- Several *Execution* strategies
- Collective Execution Strategies **influence** the *Global* result
## Goals 
1. Reduce power consumption {{% highlight c="{{< fa fa arrow-right 2 >}} Green computing" %}}
2. Improve **convergence time** to the desired *emergent*
   
*Multi-objective* nature


## Approaches {.accent}
{{% frag-list kind="ul" %}}
{{% frag-li%}}Rule-Based Schedulers{{% /frag-li %}}
{{% frag-li%}}**Reinforcement Learning-based Schedulers**{{% /frag-list %}}

---

# On {{% highlight c="Collective" %}} Computing Efficiency
## High Consumption, fast convergence
{{< video src="/fast.mp4" >}}

---
# On {{% highlight c="Collective" %}} Computing Efficiency
## Low Consumption, slow convergence
{{< video src="/slow.mp4" >}}

---
# On {{% highlight c="Collective" %}} Computing Efficiency
## Goal: adaptive solution
{{< video src="/adaptive.mp4" >}}

---
{{% slide auto-animate=true %}}
# Contribution

Learning to reduce power consumption for *self-stabilising* building blocks (i.e., **gradient-cast**, **data collection**, **sparse choice**)
- **Reference Learning Technique** <i class="fa fa-arrow-right"></i> Value-Based Reinforcement Learning (e.g., *Q-Learning*)
- **Reference Framework** <i class="fa fa-arrow-right"></i> **Aggregate Computing**: A {{% accent c="top-down" %}} *{{% highlight c="global to local" %}}* {{% accent c=functional %}} programming approach to express {{% accent c="self-organising" %}} collective behaviours
  - Good match for expressing our solution 
  - High potential-impact in the Aggregate Computing research 

---
{{% slide auto-animate=true %}}
# Contribution

Learning to reduce power consumption for *self-stabilising* building blocks (i.e., **gradient-cast**, **data collection**, **sparse choice**)
## Benefits
- RL applied in the **middleware** -- does not change the **semantics** of Aggregate Computing
- Separation between the *Functionals* aspect (i.e., the aggregate code) and *Non-Functional* aspects (i.e., the energy consumption)

## Idea 
- **Time-based** schedulers
- Learning how/when to reduce the *round frequency* ...
- ... Maintaining a **good reactivity** with respect to *environmental changes*

---

{{% slide auto-animate=true %}}

# Learning Settings
{{% fragment index="0" %}}
**Multi (Many) Agent System**
- CASs foster systems with hundreds of computational entities
{{% /fragment %}}

{{% fragment index="1" %}}
**Homogenous Behaviour**
- Complexity emerges from interactions
- Typical choice in swarm-like system 
{{% /fragment %}}

{{% fragment index="2" %}}
**Centralised Traning Decentralised Execution**  
- Global information during learning using the Q update
- distributed control at runtime <i class="fa fa-arrow-right"></i> **state built from only local data**
- learning eased by the global view
{{% /fragment %}}

{{% col class="r-stack" %}}
{{% fragment class="fade-in" index="0" %}}
{{< image height=30 src="/algorithm-learning-1.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="1" %}}
{{< image height=30 src="/algorithm-learning-2.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="2" %}}
{{< image height=30 src="/algorithm-learning-3.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="3" %}}
{{< image height=30 src="/algorithm-learning-4.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="4" %}}
{{< image height=30 src="/algorithm-learning-5.png" >}} 
{{% /fragment %}}
{{% /col %}}

---

{{% slide auto-animate=true %}}
# Learning Settings

For each time step, each agent record a **$s_t, a_t, r_t$** trajectory, as:
- State: local output derivate
- Actions: next wake-up time
- Reward: near 0 if the output is stable, -1 in the other cases

---

{{% slide auto-animate=true %}}
# Learning Settings

For each time step, each agent record a **$s_t, a_t, r_t$** trajectory, as:
- **State**: local output derivate
  - Window of size $w$ of local changes
  - Each element could be `Rising`, `Stable`, `Decreasing`
- Actions: next wake-up time
- Reward: near 0 if the output is stable, -1 in the other cases

---

{{% slide auto-animate=true %}}
# Learning Settings

For each time step, each agent record a **$s_t, a_t, r_t$** trajectory, as:
- State: local output derivate
- **Actions**: next wake-up time
    - Fixed set: `[100ms, 200ms, 500ms, 1s]`
- Reward: weight the next-wake time and the consumption

---

{{% slide auto-animate=true %}}
# Learning Settings

For each time step, each agent record a **$s_t, a_t, r_t$** trajectory, as:
- State: local output derivate
- Actions: next wake-up time
- **Reward**: near 0 if the output is stable, -1 in the other cases
    - **Multi-objective**:
      - non-stable condition: *negative reward* (-1)
      - stable condition: weight the reward w.r.t. next wake up time -- **0 if it is near to 1s**
      - $\theta$ weights the contribution of non-stability w.r.t. consumption

---
{{% slide transition="slide" auto-animate=true %}}

# Simulation Configuration
## Goal {.accent}
- Learn to reduce *power consumption*
  - Blocks: **Gradient-cast** and **Data collection**
- Maintain a good *convergence time* 
- **Dual**: with the same power, learn to converge more quickly
- Verify if the policy generalizes (i.e., work in other deployments)
## Training

## Evaluation
---
{{% slide auto-animate=true %}}
# Simulation Configuration
## Goal
## Training {.accent}
- 100 nodes in place in a semi-random grid
- each simulation has a random seed
- performance verified in different conditions
## Evaluation
---
{{% slide auto-animate=true %}}
# Simulation Configuration
## Goal
## Training {.accent}
- 100 nodes in place in a semi-random grid
- each simulation has a random seed
- performance verified in different conditions
  - multiple seek nodes
  - multiple environmental changes
## Evaluation
---
{{% slide auto-animate=true %}}
# Simulation Configuration
## Goal
## Training {.accent}
{{% video src="/scenario.mp4" %}}
## Evaluation
---

{{% slide auto-animate=true %}}
# Simulation Configuration
## Goal
## Training 
## Evaluation {.accent}
- Control the performance by varying the nodes in the system
- Compare with a hand-mand policy as a reference
---

{{% slide auto-animate=true %}}
# Result Overview
Repository @ [https://github.com/cric96/experiment-2022-acsos-round-rl](https://github.com/cric96/experiment-2022-acsos-round-rl)
## Training Process

{{< image height="30" src="/error-and-ticks.png" >}}

## Policy Learn

{{%row %}}

{{%col%}}
{{< image height="20" src="/start.png" >}}
{{%/col%}}
{{%col%}}
{{< image height="20" src="/middle.png" >}}
{{%/col%}}
{{%col%}}
{{< image height="20" src="/end.png" >}}
{{%/col%}}
{{%/row%}}

---

{{% slide auto-animate=true %}}
# Result Overview

## Performance with different seed
{{< image height="30" src="/image-rl-500-plain.png" >}}

## Performance varying the nodes
{{< image height="30" src="/plain-gradient.png" >}}

---

# Conclusion
- The system eventually learns a policy that reduces the collective power consumption
- The same policy work for different deployments

# Future Work

- Using *scheduling policy* as action
- **Deep Learning approaches** to encode local node features
- Using **Multi-Objective Reinforcement Learning** to better represent the problem space.
- Extends Learning to a fully online & distributed version

---

{{% slide preload=true background-iframe="waves-thanks.html" transition="zoom" background-color="black" %}}

# Thank you! {.white-text }