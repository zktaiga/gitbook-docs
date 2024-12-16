# Monitoring

## SSV Node Observability

### Introduction

In this section, we will go over all the necessary steps to have enhanced observability for your SSV node. We aim for this section to be an all-stop shop so that you can self-service and diagnose any issues you may have.

The dashboards cover many of the subsystems that make up the SSV node, which may seem a bit overwhelming at first; however, we will try to simplify the processes that we use to diagnose issues as well as things to look out for.

The SSV node is instrumented with [OpenTelemetry](https://opentelemetry.io/) metrics, where the default exporter is [Prometheus](https://prometheus.io/).

### A quick note on Prometheus with Grafana

#### Interpreting Rates

Some panels may look confusing at first glance; for example, how is it possible that my SSV node has connected to 34.7 peers over the last minute? Why does it have decimal points?

This is where the Prometheus `rate()` function comes in. `rate()` is a function that calculates the rate of change of a metric over a given time interval, and it is displayed on a per-second basis.

For example, if we have a calculation of `rate(ssv_network_peers_connected[1m])`, this means that the rate of peers connected is calculated as the number of peers connected over the last minute, and it is displayed on a per-second basis. We sometimes multiply this by 60 to get a rate over a minute. This should clarify why many panels have decimal points over metrics that, in theory, should be whole numbers.

#### Calculating Rates

Rates are a powerful way to see how a metric changes over time, but they force us to specify a time interval to calculate the rate. Rather than hardcoding intervals in our dashboards, we leverage `__rate_interval` all across our dashboards to calculate rates over a given time interval. You can read more about `__rate_interval` it in [Grafana's post](https://grafana.com/blog/2020/09/28/new-in-grafana-7.2-__rate_interval-for-prometheus-rate-queries-that-just-work/). This, however, means that you need to configure your Prometheus data source to match Prometheus's scrape interval. You can do this in the Grafana UI by clicking on the Prometheus datasource and then changing it under `Interval behaviour`. Having a mismatch between those two will result in incorrect rate calculations and dashboards not being displayed correctly.

{% hint style="info" %}
The default scrape interval for Prometheus is 1 minute, whereas the default interval for a Prometheus data source in Grafana is 15 seconds.
{% endhint %}

### Set up and requirements

Since different operators may be running infrastructure in different ways or platforms, we will go over three different ways to set up observability.

#### Requirements

The dashboards we provide use `pod` as a label to template across the Grafana panels. This is a common label for Kubernetes, but if you are running your SSV node on a different platform, you will need to change this to the correct label. This is useful if you are running more than one SSV node as it allows you to see performance metrics for each SSV node. In this section we will also provide snippets for different platforms to help you get started.

#### Running the sample repository

The easiest way to set up observability is to run the sample repository. It is based on Docker Compose and it will do everything for you, including setting up the SSV node, Prometheus, and Grafana.

To run the sample repository, you can follow the instructions in the [README](https://github.com/ssvlabs/ssv-repo-template/blob/main/README.md).stack

#### Using an existing monitoring stack

If you are already running a monitoring stack, scraping metrics from your SSV node has not changed. You will need to ensure that your Prometheus instance is scraping metrics from your SSV node.

The following is an example of a Prometheus configuration that will scrape metrics from your SSV node. It is important to note that the `pod` label is not added to the metrics by default, so you will need to add it manually. Prometheus by default adds an `instance` label to the metrics. To have consistency across platforms, we use the `pod` label with a simple configuration that will add the `pod` label to the metrics.

```yaml
scrape_configs:
  - job_name: ssv
    metrics_path: /metrics
    static_configs:
      - targets:
          - "localhost:15000"
    relabel_configs:
      ## Two options to choose from:
      ## 1. If you want a static name, perhaps because you are running 
      ## multiple instances of ssv-node, or want to set a specific name, uncomment these:
      # - target_label: pod
      #   replacement: ssv-node-1

      ## 2. This will use the host specified in the targets list by uncommenting the following lines
      # - source_labels: [__address__]
      #   target_label: pod
```

#### Kubernetes

If you are running your SSV node on Kubernetes, you will need to ensure that your Prometheus instance is scraping metrics from your SSV node. For this, we often recommend a project called [kube-prometheus-stack](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack).

Due to the dynamic nature of Kubernetes, a common pattern is to use a `ServiceMonitor` or `PodMonitor` to scrape metrics from your SSV node. `kube-prometheus-stack` by default adds the `pod` label to the metrics, so dashboards should work out of the box.

You can read more on ServiceMonitors and PodMonitors in the [Prometheus Operator documentation](https://github.com/prometheus-operator/prometheus-operator/blob/main/Documentation/api.md).
