### Chapter 1
### Introduction

- Conventional divide between Dev and Ops creates a natural conflict
  between the two groups, as the goals of these two groups are
conflicting themselves.

- Devs want to ship fast hence inducing more entropy in the system and
  increasing the chance of a failure.

- Ops is tasked with making the system reliable, and is inclined more
  towards not changing a well running system

#### SRE approach

- **Conflict isn't inevitable**

- SRE is what happens when a software engineer design an operations team

- Google's SRE team is 50-60% Software devs, and 40-50% Devs who are
  80-90% there with additional technical skills like deep system's and
UNIX knowledge

- **Two facets of an ideal SRE:**
  a. Easily gets bored with doing manual work
  b. Possesses the know-how of how to write software to replace the
manual tasks

- Traditional minded ops-team scale linearly by hiring more people as
  the task grow with scale.

- Systems should be **automatic**, not just **automated**

- Max 50% time on ops work with a goal to reducing it further, and 50% time on actual development in order to help the former objective

- SRE comes with it's own challenges, like around hiring and requiring
  strong support from management around the unorthodox approaches like
error budgets.

#### Tenets of SRE

- **Ensuring a Durable focus on Engineering**
  - the 50% rule
  - maximum 2 events for the person on-call, allowing them enough time
    for post-mortems
  - Blame-free postmortems, with goal of exposing faults in system. And
    applying engineering to mend them

- **Pursuing Maximum Change Velocity, without violating Service SLO's**
  - Error Budgets
    - 100% is wrong reliability target
    - Things that determine error-budget:
      - Level of availability the user is happy with
      - Alternative available to user, dissatisfied with product's
        availability
      - Usage pattern at various availability levels
    - Business/Product must establish a system's error budget
    - What to spend error budgets on?
      - Making the possible to ship faster with feature like phased
        rollout

- **Monitoring**
  - System that depends heavily on a human to interpret alerts are inherently flawed, software should do the interpreting

  - 3 kinds of monitoring output
    - **Alerts**: signifies human intervention is required to fix it.
    - **Tickets**: intervention needed, but not-immediately
    - **Logging**: for audit purposes


- **Emergency Response**
  - Mean Time To Failure(MTTF)
  - Mean Time To Recovery(MTTR)

  - Human adds latency

  - **Human + Playbook >> Winging it** , 3X improvement

  - Wheel of MisFortune (Exercise for practicing failure scenarios)

- **Change Management**
  - 70% outages are caused due to changes in live system

  - Best practices:
    - Implement progressive rollouts
    - Quickly and accurately detecting problems
    - Rolling back faulty changes safely

- **Demand Forecasting and Capacity Planning**
  - To ensure availability of sufficient capacity for future demand

  - Take into account both organic(natural adoption) and inorganic(promos) growth

  - Capacity is critical to availability
  - SRE team must be in-charge of capacity-planning

- **Provisioning**
  - It combines change management and capacity planning

  - Provisioning must be quick and only when necessary

  - Ad-hoc provisioning is expensive, in terms of time. And is riskier
    operation than load-shifting.

- **Efficiency and Performance**
  - SRE controls provisioning so, it should take care of improving
    utilization

  - Utilization is a big lever on a **service cost**

  - Resource Utilization is function of Load, Capacity and Software
    Efficiency

  - **SREs predict demand, provision capacity and can modify the software
    for efficiency**

  - Provision to meet capacity at a specific response speed

- SRE represent a significant breakout from existing industry practices
  to manages large and complicated systems

