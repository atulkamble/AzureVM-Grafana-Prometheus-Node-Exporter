```
{
  "annotations": {
    "list": []
  },
  "editable": true,
  "gnetId": null,
  "graphTooltip": 0,
  "panels": [
    {
      "type": "stat",
      "title": "CPU Usage (%)",
      "targets": [
        {
          "expr": "100 - (avg by (instance) (irate(node_cpu_seconds_total{mode=\"idle\"}[5m])) * 100)"
        }
      ],
      "gridPos": { "h": 4, "w": 6, "x": 0, "y": 0 }
    },
    {
      "type": "stat",
      "title": "Memory Usage (%)",
      "targets": [
        {
          "expr": "(node_memory_MemTotal_bytes - node_memory_MemAvailable_bytes) / node_memory_MemTotal_bytes * 100"
        }
      ],
      "gridPos": { "h": 4, "w": 6, "x": 6, "y": 0 }
    },
    {
      "type": "stat",
      "title": "Disk Usage (%)",
      "targets": [
        {
          "expr": "(node_filesystem_size_bytes{fstype!=\"tmpfs\"} - node_filesystem_free_bytes{fstype!=\"tmpfs\"}) / node_filesystem_size_bytes{fstype!=\"tmpfs\"} * 100"
        }
      ],
      "gridPos": { "h": 4, "w": 6, "x": 12, "y": 0 }
    },
    {
      "type": "stat",
      "title": "Load Average",
      "targets": [
        {
          "expr": "node_load1"
        }
      ],
      "gridPos": { "h": 4, "w": 6, "x": 18, "y": 0 }
    },
    {
      "type": "timeseries",
      "title": "CPU Usage Trend",
      "targets": [
        {
          "expr": "100 - (avg by (instance) (irate(node_cpu_seconds_total{mode=\"idle\"}[5m])) * 100)"
        }
      ],
      "gridPos": { "h": 8, "w": 12, "x": 0, "y": 4 }
    },
    {
      "type": "timeseries",
      "title": "Memory Usage Trend",
      "targets": [
        {
          "expr": "(node_memory_MemTotal_bytes - node_memory_MemAvailable_bytes) / node_memory_MemTotal_bytes * 100"
        }
      ],
      "gridPos": { "h": 8, "w": 12, "x": 12, "y": 4 }
    },
    {
      "type": "timeseries",
      "title": "Network RX",
      "targets": [
        {
          "expr": "rate(node_network_receive_bytes_total[1m])"
        }
      ],
      "gridPos": { "h": 8, "w": 12, "x": 0, "y": 12 }
    },
    {
      "type": "timeseries",
      "title": "Network TX",
      "targets": [
        {
          "expr": "rate(node_network_transmit_bytes_total[1m])"
        }
      ],
      "gridPos": { "h": 8, "w": 12, "x": 12, "y": 12 }
    },
    {
      "type": "timeseries",
      "title": "Disk Read",
      "targets": [
        {
          "expr": "rate(node_disk_read_bytes_total[1m])"
        }
      ],
      "gridPos": { "h": 8, "w": 12, "x": 0, "y": 20 }
    },
    {
      "type": "timeseries",
      "title": "Disk Write",
      "targets": [
        {
          "expr": "rate(node_disk_written_bytes_total[1m])"
        }
      ],
      "gridPos": { "h": 8, "w": 12, "x": 12, "y": 20 }
    }
  ],
  "schemaVersion": 38,
  "style": "dark",
  "tags": ["linux", "node-exporter"],
  "templating": { "list": [] },
  "time": {
    "from": "now-15m",
    "to": "now"
  },
  "title": "Linux Monitoring Dashboard",
  "version": 1
}
```
