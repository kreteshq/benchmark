# Benchmark

|                  | Version | Language   | Type       | Router | Requests/s | Latency | Transfer/s |
| :--              | :-:     | :--        | :--        | :-:    | --:        | --:     | --:        |
| **[Huncwot][1]** | 0.40.0  | JavaScript | High-Level | ✓      | 85,167     | 1.17    | 8.77MB     |
| Fastify          | 2.3.0   | JavaScript | High-Level | ✓      | 54,068     | 1.85    | 8.46MB     |
| Node.js Bare     | 11.14.0 | JavaScript | Low-Level  | ✗      | 54,257     | 1.84    | 8.49MB     |
| Trek             | 0.0.1   | JavaScript | High-Level | ✓      | 43,777     | 2.28    | 6.22MB     |
| uWebSockets      | 15.10.0 | JavaScript | Low-Leve   | ✓      | 170,266    | 0.58    | 19.97MB    |
| Kemal            |         | Crystal    | High-Level | ✓      | 93,217     | 1.07    | 11.82MB    |
| Turbo HTTP       | 0.3.2   | JavaScript | Low-Level  | ✗      | 80,123     | 1.25    | 9.70MB     |

## Conditions

### Machine

Bare Metal from [Vultr](https://www.vultr.com/?ref=8058254-4F) (<-- this is my affilate link: I will receive up to 25 USD for each referral. This will help me out a bit continue making these tests).

* **Processor**: E3-1270v6
* **CPU**: 8 CPU @ 3.8Ghz
* **Memory**: 32GB
* **Disk**: SSD

### Node -> `11.14.0`

### Method

Using two rounds: first to warm-up, second to measure.

```
wrk -c 100 -d 45s -t 25 http://localhost:3000
```


[1]: https://huncwot.org/