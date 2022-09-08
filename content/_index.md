 
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

🎤 *Gianluca Aguzzi*, Roberto Casedei, Viroli Mirko

📧 [gianluca.aguzzi@unibo.it](mailto:gianluca.aguzzi@unibo.it)

---

# Collective Adaptive Systems {.accent}

{{% row %}}
{{% fragment class="col" %}} 
#### Many Networked Agents
{{< image height="30" src="/network.png" >}} 
{{% /fragment %}}
{{% fragment class="col" %}} 
#### Cyber-Physical Systems
{{< image height="30" src="/cps.png" >}} 
{{% /fragment %}}
{{% fragment class="col" %}} 
#### Collective Behaviour  
{{< image height="30" src="/ci.png" >}} 
{{% /fragment %}}

{{% /row %}}

---

# Applications {.accent}

{{% row %}}
{{% fragment class="col" %}}
### Swarm Robotics
{{< image height="30" src="/swarm.jpg">}} 
{{% /fragment %}}
{{% fragment class="col" %}}
### Crowd Engineering
{{< image height="30" src="/crowd.png">}} 
{{% /fragment %}}
{{% fragment class="col" %}}
### Smart Cities
{{< image height="30" src="/smart-city.jpg">}} 
{{% /fragment %}}
{{% /row %}}


---

{{% slide auto-animate=true %}}
# Execution Model 
---

{{% slide auto-animate=true %}}
# Execution Model 
### How
### When
---

{{% slide auto-animate=true %}}
# Execution Model
### How {.accent}
{{% row %}}
{{%col%}}
#### Sense
{{%/col%}}
{{%col%}}
#### Compute
{{%/col%}}
{{%col%}}
#### Act
{{%/col%}}
{{% /row %}}

### When

---

{{% slide auto-animate=true %}}
# Execution Model 
### How {.accent}
{{% row %}}
{{%col%}}
#### Sense {.highlight}
{{< image height="30" src="/single-agent-rev-1.png">}}
{{%/col%}}
{{%col%}}
#### Compute
{{%/col%}}
{{%col%}}
#### Act
{.highlight}}
{{%/col%}}
{{% /row %}}

### When

---

{{% slide auto-animate=true %}}
# Execution Model 
### How {.accent}
{{% row %}}
{{%col%}}
#### Sense 
{{< image height="30" src="/single-agent-rev-1.png">}}
{{%/col%}}
{{%col%}}
#### Compute {.highlight}
{{< image height="30" src="/single-agent-rev-2.png">}}
{{%/col%}}
{{%col%}}
#### Act
{{%/col%}}
{{% /row %}}

### When
---
{{% slide auto-animate=true %}}
# Execution Model
### How  {.accent}
{{% row %}}
{{%col%}}
#### Sense 
{{< image height="30" src="/single-agent-rev-1.png">}}
{{%/col%}}
{{%col%}}
#### Compute
{{< image height="30" src="/single-agent-rev-2.png">}}
{{%/col%}}
{{%col%}}
#### Act {.highlight}
{{< image height="30" src="/single-agent-rev-3.png">}}
{{%/col%}}
{{% /row %}}

### When
---
{{% slide auto-animate=true %}}
# Execution Model 
### How 
### When {.accent}

- {{%highlight c=Reactive %}}
   - Messaged-based
   - Sensor-based
   - Event-based
- Proactive
---
{{% slide auto-animate=true %}}
# Execution Model 
### How 
### When {.accent}

- Reactive
    - Messaged-based
    - Sensor-based
    - Event-based
- {{%highlight c=Proactive %}}
---



{{% slide auto-animate=true %}}
# Collective Computing Efficiency
## Goals 

## Approaches

---

{{% slide auto-animate=true %}}
# Collective Computing Efficiency
## Goals {.accent}

{{% frag-list kind="ul" %}}
{{% frag-li%}}
Reduce power Consumption 
{{% frag class=highlight c="{{< fa fa arrow-right 2 >}} Green computing" %}} 
{{% /frag-li %}}
{{% frag-li%}}
Improve **Convergence time** to desired *emergent*
{{% /frag-li %}}
{{% frag-li%}}
*Multi-objective* nature
{{% /frag-li %}}
{{% /frag-list %}}  

## Approaches

---

{{% slide auto-animate=true %}}
# Collective Computing Efficiency
## Goals 
## Approaches {.accent}
{{% frag-list kind="ul" %}}
{{% frag-li%}}
Rule-Based Schedulers
{{% /frag-li %}}
{{% frag-li%}}
**Reinforcement Learning Schedulers**
{{% /frag-list %}}

---
{{% slide auto-animate=true %}}
# Aggregate Computing

---

{{% slide auto-animate=true %}}
# Aggregate Computing
 A {{% accent c="top-down" %}} *{{% highlight c="global to local" %}}* {{% accent c=functional %}} programming approach to express {{% accent c="self-organising" %}} collective behaviours
{{% row %}}
{{%col%}}

---

{{% slide auto-animate=true %}}
# Aggregate Computing
 A {{% accent c="top-down" %}} *{{% highlight c="global to local" %}}* {{% accent c=functional %}} programming approach to express {{% accent c="self-organising" %}} collective behaviours
{{% row %}}
{{%col%}}
### Computational Field {.accent }  
{{< image height=50 src="/ac.png"  >}}
{{%/col%}} 
{{% /row %}}

---

{{% slide auto-animate=true %}}
# Aggregate Computing
 A {{% accent c="top-down" %}} *{{% highlight c="global to local" %}}* {{% accent c=functional %}} programming approach to express {{% accent c="self-organising" %}} collective behaviours

{{% row %}}
{{%col%}}
### Computational Field {.accent }
{{< image height=50 src="/ac.png"  >}}
{{%/col%}} 

{{%col%}}
### Field Calculus {.accent }
{{< image height=50 src="/high-level-examples.png"  >}} 
{{%/col%}} 
 
{{% /row %}}

---

{{% slide auto-animate=true %}}
# Aggregate Computing
 A {{% accent c="top-down" %}} *{{% highlight c="global to local" %}}* {{% accent c=functional %}} programming approach to express {{% accent c="self-organising" %}} collective behaviours

{{% row %}}
{{%col%}}
### Computational Field {.accent }
{{< image height=50 src="/ac.png"  >}}
{{%/col%}} 

{{%col%}}
### Field Calculus {.accent }
{{< image height=50 src="/high-level-examples.png"  >}} 
{{%/col%}}
 
{{%col%}} 
### Composable API {.accent }
{{< image height=50 src="/full-stack.png"  >}} 
{{%/col%}}
 
{{% /row %}}

---

# Execution Model
Proactive and Periodioc execution of **{{% accent c="rounds" %}}** 
{{% row %}}
{{% col %}}
{{% frag-list kind="ol" %}}
{{% frag-li "fade-in" "0" %}} 
#### Context Acquisition {.highlight}
- Sensors Data
- Neighbourhood Information

{{% /frag-li %}}

{{% frag-li "fade-in" 1 %}}
#### Program Evaluation {.highlight} 
-  **Export** Generation 
{{% /frag-li %}}
{{% frag-li "fade-in" 2 %}} 
#### Context Action {.highlight}
- **Export** Sharing
- Actuations 
{{% /frag-li %}}
{{% /frag-list %}}
{{% /col %}}
{{% col class="r-stack" %}}

{{% fragment class="fade-in" index="0" %}}
{{< image height=30 src="/execution-steps-0.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="1" %}}
{{< image height=30 src="/execution-steps-1.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="2" %}}
{{< image height=30 src="/execution-steps-2.png" >}} 
{{% /fragment %}}

{{% /col %}}
{{% /row %}}

---

## Collective pattern {.accent } 

{{% row %}}
{{% fragment class="col" %}}
#### Gradient Cast
{{< image height=30 src="/network-downstream2.png"  >}}
Broadcast information from *sink* nodes
{{% /fragment %}}

{{% fragment class="col" %}}
#### Data collection
{{< image height=30 src="/network-upstream.png"  >}}
Collect data into *sink* nodes
{{% /fragment %}}

{{% fragment class="col" %}}
#### Sparse Choice
{{< image height=30 src="/network-candidates.png"  >}}
Distributed leader election
{{% /fragment %}}

{{% /row %}}

{{% fragment %}} {{< fa thumbs-up >}}  {{% accent c="**Self-organising & self-stabilising blocks**" %}} {{% /fragment %}}  

---

# Contribution

Learning to reduce power consumption for *self-stabilising* building block

## Benefits
- RL applied in the **middleware** -- does not change the semantic of Aggregate Computing
- Separation between the *Functional* aspect (i.e., the aggregate code) and *Non-Functional* aspects (i.e., )

## Idea 
- **Time-based** schedulers
- Reduce the *round frequency* during stable conditions...
- ... Maintaining a **good reactivity** with respect to *environmental changes*

---

## General Idea {.accent}
{{< video src="/general-idea.mp4" >}}

---

{{% slide auto-animate=true %}}

# Learning Settings

{{% row %}}
{{% fragment class="col" index="0" %}}
{{%accent c="**Multi Agent Systems**" %}}
{{% /fragment %}}

{{% fragment class="col" index="1" %}}
{{%accent c="**Homogenous Behaviour**" %}}
{{% /fragment %}}

{{% fragment class="col" index="2" %}}
{{%accent c="**Centralised Traning Decentralised Execution**" %}}
{{% /fragment %}}
{{% /row %}}

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

- State: local output derivate
- Actions: next wake-up time
- Reward: near 0 if the output is stable, -1 in the other cases

---

{{% slide auto-animate=true %}}
# Learning Settings

- **State**: local output derivate
  - Window of size $w$ of local changes
  - Each element could be `Rising`, `Stable`, `Decreasing`
- Actions: next wake-up time
- Reward: near 0 if the output is stable, -1 in the other cases

---

{{% slide auto-animate=true %}}
# Learning Settings

- State: local output derivate
- **Actions**: next wake-up time
    - Fixed set: `[100ms, 200ms, 500ms, 1s]`
- Reward: weight the next-wake time time and the consumption

---

{{% slide auto-animate=true %}}
# Learning Settings

- State: local output derivate
- Actions: next wake-up time
- **Reward**: near 0 if the output is stable, -1 in the other cases
    - **Multi-objective**:
      - non-stable condition: *negative reward* (-1)
      - stable condition: weight the reward w.r.t. next wake up time -- **0 if it is near to 1s**
      - $\theta$ weights the contribution of non-stability w.r.t. consumption

---
{{% slide auto-animate=true %}}
# Simulation Configuration
## Training
## Evaluation
---
{{% slide auto-animate=true %}}
# Simulation Configuration
## Training {.accent}
- 100 nodes in place in a semi-random grid
- each simulation as a random seed
- performance verified in different conditions
## Evaluation
---
{{% slide auto-animate=true %}}
# Simulation Configuration
## Training {.accent}
- 100 nodes in place in a semi-random grid
- each simulation as a random seed
- performance verified in different conditions
  - multiple seek nodes
  - multiple environmental changes
  - different self-stabilising blocks
## Evaluation
---

{{% slide auto-animate=true %}}
# Simulation Configuration
## Training 
## Evaluation {.accent}
- Verifying the influence of different seeds
- Control the performance by varying the nodes in the system
- Compare with a hand-mand policy as a reference
---

{{% slide auto-animate=true %}}
# Result Overview

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

# Future Work

- Using *scheduling policy* as action
  - Mix *sensing-based* and *time-based* schedulers
- **Deep Learning approaches** to encode local node features
- Using **Multi-Objective Reinforcement Learning** to better represent the problem space.
- Extends Learning to a fully online & distributed version

---

{{% slide preload=true background-iframe="waves-thanks.html" transition="zoom" background-color="black" %}}

# Thank you! {.white-text }