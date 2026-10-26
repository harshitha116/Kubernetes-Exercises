# Exercise 6: Grafana Real-Time Monitoring of Quick Commerce App

## Objective
Monitor application metrics using Prometheus and Grafana.

## Technologies Used
- Python
- Docker
- Prometheus
- Grafana

## Implementation
1. Created a Python application to expose delivery metrics.
2. Ran the metrics application on port 8000.
3. Configured Prometheus to collect application metrics.
4. Verified the `pending_deliveries` metric in Prometheus.
5. Created a Grafana dashboard to visualize the metrics.

## Verification
- Confirmed that Prometheus returned values for `pending_deliveries`.
- Set up a Grafana dashboard for monitoring application metrics.

## Conclusion
This exercise demonstrated how Prometheus collects application metrics and Grafana displays them in a monitoring dashboard.