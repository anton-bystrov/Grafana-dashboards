# MongoDB Grafana Dashboards for `mongodb_exporter`

This repository contains Grafana dashboards for MongoDB metrics collected through Prometheus.

These dashboards are based on the original Percona MongoDB Grafana dashboards:

- https://github.com/percona/grafana-dashboards

They were adapted for use with:

- https://github.com/percona/mongodb_exporter

## Contents

The `dashboards/` directory currently includes:

- `mongodb_cluster_summary_exporter.json`
- `mongodb_collections_overview_exporter.json`
- `mongodb_inmemory_details_exporter.json`
- `mongodb_instance_summary_exporter.json`
- `mongodb_instances_overview_exporter.json`
- `mongodb_mmapv1_details_exporter.json`
- `mongodb_oplog_details_exporter.json`
- `mongodb_replset_summary_exporter.json`
- `mongodb_router_summary_exporter.json`
- `mongodb_wiredtiger_details_exporter.json`

## Import into Grafana

1. Open Grafana and import a dashboard JSON file from the `dashboards/` directory.
2. Select your Prometheus datasource during import.
3. After import, the dashboards use the `datasource` variable for Prometheus-backed panels.

## Notes

- These dashboards are intended for `percona/mongodb_exporter` metric names and label conventions.
- Depending on your Prometheus relabeling and exporter setup, some panels may require small adjustments to label selectors.
