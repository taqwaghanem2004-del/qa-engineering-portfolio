# Performance Testing (Apache JMeter)

## Overview
A load test run with Apache JMeter 5.6.3 on the public demo site BlazeDemo (blazedemo.com), comparing 100 and 300 virtual users. The first site tried (demo.opencart.com) blocked the automated requests with HTTP 403, so BlazeDemo was used instead.

## Test setup
- One Thread Group with 5 HTTP Request samplers: Home Page, Reserve Flight, Purchase Page, Confirm Purchase, blazedemo.com
- Run 1: 100 users, ramp-up 60 s, duration 600 s
- Run 2: 300 users, ramp-up 90 s, duration 600 s
- Listener: Aggregate Report

## Results

| Metric | 100 users | 300 users |
|---|---|---|
| Samples | 500 | 1500 |
| Average response time | 1558 ms | 1564 ms |
| Median | 795 ms | 757 ms |
| 90th percentile | 4365 ms | 4009 ms |
| 95th percentile | 7027 ms | 7537 ms |
| 99th percentile | 8703 ms | 9554 ms |
| Error % | 0.80% | 0.00% |
| Throughput | 7.2 / sec | 20.1 / sec |

In the 100-user run the errors were on three steps: Home Page 1%, Reserve Flight 2% and Purchase Page 1%.

## Analysis
- Going from 100 to 300 users did not change the average response time (1558 ms vs 1564 ms), and the error rate was 0% in the larger run.
- Throughput grew with the load (7.2/s to 20.1/s), so the site handled the extra users in this test.
- Response times vary a lot: the maximum was about 10 seconds in both runs, and the 95th and 99th percentiles are much higher than the average.

## Files
- `ecommerce_test.jmx`: the JMeter test plan (Thread Group, HTTP Header Manager, 5 HTTP requests, Summary Report, Aggregate Report, View Results Tree)

## Evidence
- `jmeter_100_users_aggregate_report.png`
- `jmeter_300_users_aggregate_report.png`

## Limitations
- BlazeDemo is a public demo site, so the results say nothing about a real application.
- The saved `.jmx` is currently set to 300 users, ramp-up 60 s, duration 600 s. This differs from the ramp-up listed for run 2 above (90 s). Change the settings to repeat a run.
- Each run was done once.