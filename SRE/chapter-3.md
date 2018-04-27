### Chapter 3
### Embracing Risk

- Past a certain point increasing reliability is actually worse for a
  service.
  - It limits how fast you can ship new features
  - Dramatic cost increase

- Users typically don't notice difference between high reliability and
  extreme reliability

- Rather than simply maximizing uptime, Seek to balance the risk of
  unavailability with rapid innovation and efficient service.
- Maximize overall user experience with feature, service and
  performance.

#### Managing Risk

- Cost do not increase linearly with reliability, rather exponetially.
- Two dimensions of cost:
  - Cost of redundant compute resources
  - Opportunity cost: Engineering cost, which are not actively
    developing features
- Service should be reliable enoughm but not **more** than required

#### Measuring Service Risk

- Time based availabilty = uptime / (uptime + downtime)

- Time based doesn't work that well on a globally distributed system
- Focus on fault isolation, so that you can be up for atleast a subset
  of your users at any given time

- Aggregate Availabilty
  - Request Success Rate = sucessful requests / total requests

- Not all requests are equally important, but this gives a reasonable
  approximation of uptime

#### Risk Tolerance of Services
- Decides by the business need of the service

- Infra based services are more hard due to lack of a proper business
  owner


