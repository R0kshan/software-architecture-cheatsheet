## List of NFRs to Pillars Matrix

> [!NOTE] How to read the following table
>  - The table below maps common NFRs to architecture pillars, highlighting where they align ✅ and where trade-offs ⚖️ require design decisions.
>- The core pillars for a robust architecture are **Security, Reliability, Performance, Maintainability.**
>- Some NFRs are subsets of others and are listed explicitly for granularity and practical reference. 

| **NFR / Pillars**                                                | **Operational excellence** | **Security** | **Reliability** | **Performance** | **Maintainability** | **Cost Opt.** | **Sustainability** |
| ---------------------------------------------------------------- | -------------------------- | ------------ | --------------- | --------------- | ------------------- | ------------- | ------------------ |
| **[Identification & Authorization](Identification%20&%20Authorization.md)**                           |                            | ✅            |                 | ⚖️              | ⚖️                  |               |                    |
| **[Data Encryption](Data%20Encryption.md)**                                          |                            | ✅            |                 | ⚖️              |                     | ⚖️            | ⚖️                 |
| **[Data integrity](Data%20integrity.md)**                                           |                            | ✅            | ✅               | ⚖️              |                     |               |                    |
| **[Audit Logging](Audit%20Logging.md)**                                            | ✅                          | ✅            |                 | ⚖️              |                     | ⚖️            |                    |
| **[Observability](Non%20Functional%20Requirements/Observability%5C)** | ✅                          | ✅            | ✅               | ✅               | ✅                   | ⚖️            |                    |
| **[High Availability](High%20Availability.md)**                                        |                            |              | ✅               |                 |                     | ⚖️            | ⚖️                 |
| **[Fault Tolerance](Fault%20Tolerance.md)**                                          |                            |              | ✅               |                 | ⚖️                  | ⚖️            | ⚖️                 |
| **[Recoverability](Recoverability.md)**                                           | ✅                          |              | ✅               |                 |                     |               |                    |
| **[Scalability](Scalability.md)**                                              |                            |              | ✅               | ✅               | ⚖️                  | ⚖️            | ⚖️                 |
| **[Elasticity](Elasticity.md)**                                               |                            |              | ✅               | ✅               | ⚖️                  | ✅             | ⚖️                 |
| **[Testability](Testability.md)**                                              | ✅                          |              | ✅               |                 | ✅                   |               |                    |
| **[Reusability](Reusability.md)**                                              |                            |              |                 |                 | ✅                   | ✅             |                    |
| **[Flexibility](Flexibility.md)**                                              |                            |              |                 |                 | ✅                   |               |                    |
| **[Portability](Portability.md)**                                              |                            |              |                 |                 | ✅                   | ✅             |                    |
| **[Lifetime](Lifetime.md)**                                                 |                            |              |                 |                 | ✅                   | ✅             |                    |
| **[Simplicity](Simplicity.md)**                                               | ✅                          | ⚖️           | ✅               | ✅               | ✅                   | ✅             | ✅                  |
| **[Cost Efficiency](Cost%20Efficiency.md)**                                          |                            |              |                 | ⚖️              |                     | ✅             | ✅                  |
| **[Cost Predictability](Cost%20Predictability.md)**                                      |                            |              |                 |                 |                     | ✅             |                    |
| **[Resource Opt.](Resource%20Opt..md)**                                            |                            |              | ⚖️              | ✅               |                     | ✅             | ✅                  |
| **[Network Opt.](Network%20Opt..md)**                                             |                            |              |                 | ✅               |                     | ✅             | ✅                  |
| **[Interoperability](Interoperability.md)**                                         |                            |              |                 | ⚖️              | ✅                   |               |                    |
| **[Compliance & Regulatory](Compliance%20&%20Regulatory.md)**                                  |                            | ✅            |                 |                 |                     | ⚖️            |                    |
| **[Latency](Latency.md)**                                                  |                            |              | ⚖️              | ✅               |                     | ⚖️            | ⚖️                 |
| **[Automation](Automation.md)**                                               | ✅                          |              | ✅               | ✅               | ✅                   | ✅             | ✅                  |


