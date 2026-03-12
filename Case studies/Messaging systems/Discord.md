## How discord turned 10000 reads into 1

![[how-discord-stores-trillions-of-messages.png|506]]

Source : [Discord turned 10000 database reads into 1  - LinkedIn post by ALexandre Zajac](https://www.linkedin.com/posts/alexandre-zajac_discord-turned-100000-database-reads-into-activity-7429563071133679617-nWtB?utm_source=share&utm_medium=member_desktop&rcm=ACoAAB8DTKUB8Xj7CQE5kXG8bLN4kN0bmTH_sOo)
### Summarized architecture takeaway 
Eliminate redundant work at the service layer before scaling databases—techniques like request coalescing can reduce thousands of identical backend operations into a single request.

