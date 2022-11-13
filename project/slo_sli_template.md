# API Service                                                                                                         

| Category     | SLI                                                                                                | SLO                                                                                                         |
|--------------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Availability | total # of successful requests / total # of requests for the API service                           | 99%                                                                                                         |
| Latency      | 90th percentile latency over a 5 min period                                                        | 90% of requests below 100ms                                                                                 |
| Error Budget | 1 - availability       , where availability = total # of successful requests / total # of requests | Error budget is defined at 20%. This means that 20% of the requests can fail and still be within the budget |
| Throughput   | 5 number of requests over last 5 min are handle                                                    | 5 RPS indicates the application is functioning                                                              |

