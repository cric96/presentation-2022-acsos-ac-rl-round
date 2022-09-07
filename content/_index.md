 
+++

title = "Addressing Collective Computations Efficiency"
description = "A Hugo theme for creating Reveal.js presentations"
outputs = ["Reveal"]
aliases = [
    "/guide/"
]
+++


# Addressing Collective Computations Efficiency {.r-fit-text}
## Towards a Platform-level Reinforcement Learning Approach {.r-fit-text .highlight}
**Talk @ ACSOS 2022** 
{.accent}

🎤 **Gianluca Aguzzi**, Roberto Casedei, Viroli Mirko

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
## Execution Model 
---

{{% slide auto-animate=true %}}
## Execution Model 
### How
### When
---

{{% slide auto-animate=true %}}
## Execution Model
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
## Execution Model 
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
## Execution Model 
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
## Execution Model
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
## Execution Model 
### How 
### When {.accent}

- {{%highlight c=Reactive %}}
   - Messaged-based
   - Sensor-based
   - Event-based
- Proactive
---
{{% slide auto-animate=true %}}
## Execution Model 
### How 
### When {.accent}

- Reactive
    - Messaged-based
    - Sensor-based
    - Event-based
- {{%highlight c=Proactive %}}
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