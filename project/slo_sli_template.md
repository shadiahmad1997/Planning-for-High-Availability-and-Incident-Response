# API Service                                                                                                         

| Category     | SLI                                                                                                | SLO                                                                                                         |
|--------------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Availability | total # of successful requests / total # of requests for the API service                           | 99%                                                                                                         |
| Latency      | 90% of total buckets of requests in a histogram below 100 ms                                       | 90% of requests below 100ms                                                                                 |
| Error Budget | 1 - availability       , where availability = total # of successful requests / total # of requests | Error budget is defined at 20%. This means that 20% of the requests can fail and still be within the budget |
| Throughput   | total # of successful requests over a period of time. for example 5 RPS                            | 5 RPS indicates the application is functioning                                                              |



