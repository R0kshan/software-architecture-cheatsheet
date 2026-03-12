> [!NOTE] How to read the following table
>  - The table below maps common NFRs to architecture pillars, highlighting where they align ✅ and where trade-offs ⚖️ require design decisions.
>- The core pillars for a robust architecture are **Security, Reliability, Performance, Maintainability.**
>- Some NFRs are subsets of others and are listed explicitly for granularity and practical reference. 

| **NFR / Pillars**                                                | **Operational excellence** | **Security** | **Reliability** | **Performance** | **Maintainability** | **Cost Opt.** | **Sustainability** |
| ---------------------------------------------------------------- | -------------------------- | ------------ | --------------- | --------------- | ------------------- | ------------- | ------------------ |
| **[[Identification & Authorization]]**                           |                            | ✅            |                 | ⚖️              | ⚖️                  |               |                    |
| **[[Data Encryption]]**                                          |                            | ✅            |                 | ⚖️              |                     | ⚖️            | ⚖️                 |
| **[[Data integrity]]**                                           |                            | ✅            | ✅               | ⚖️              |                     |               |                    |
| **[[Audit Logging]]**                                            | ✅                          | ✅            |                 | ⚖️              |                     | ⚖️            |                    |
| **[[Non Functional Requirements/Observability\|Observability]]** | ✅                          | ✅            | ✅               | ✅               | ✅                   | ⚖️            |                    |
| **[[High Availability]]**                                        |                            |              | ✅               |                 |                     | ⚖️            | ⚖️                 |
| **[[Fault Tolerance]]**                                          |                            |              | ✅               |                 | ⚖️                  | ⚖️            | ⚖️                 |
| **[[Recoverability]]**                                           | ✅                          |              | ✅               |                 |                     |               |                    |
| **[[Scalability]]**                                              |                            |              | ✅               | ✅               | ⚖️                  | ⚖️            | ⚖️                 |
| **[[Elasticity]]**                                               |                            |              | ✅               | ✅               | ⚖️                  | ✅             | ⚖️                 |
| **[[Testability]]**                                              | ✅                          |              | ✅               |                 | ✅                   |               |                    |
| **[[Reusability]]**                                              |                            |              |                 |                 | ✅                   | ✅             |                    |
| **[[Flexibility]]**                                              |                            |              |                 |                 | ✅                   |               |                    |
| **[[Portability]]**                                              |                            |              |                 |                 | ✅                   | ✅             |                    |
| **[[Lifetime]]**                                                 |                            |              |                 |                 | ✅                   | ✅             |                    |
| **[[Simplicity]]**                                               | ✅                          | ⚖️           | ✅               | ✅               | ✅                   | ✅             | ✅                  |
| **[[Cost Efficiency]]**                                          |                            |              |                 | ⚖️              |                     | ✅             | ✅                  |
| **[[Cost Predictability]]**                                      |                            |              |                 |                 |                     | ✅             |                    |
| **[[Resource Opt.]]**                                            |                            |              | ⚖️              | ✅               |                     | ✅             | ✅                  |
| **[[Network Opt.]]**                                             |                            |              |                 | ✅               |                     | ✅             | ✅                  |
| **[[Interoperability]]**                                         |                            |              |                 | ⚖️              | ✅                   |               |                    |
| **[[Compliance & Regulatory]]**                                  |                            | ✅            |                 |                 |                     | ⚖️            |                    |
| **[[Latency]]**                                                  |                            |              | ⚖️              | ✅               |                     | ⚖️            | ⚖️                 |
| **[[Automation]]**                                               | ✅                          |              | ✅               | ✅               | ✅                   | ✅             | ✅                  |
