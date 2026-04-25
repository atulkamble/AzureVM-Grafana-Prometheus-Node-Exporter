```
Azure VM Alerting 

1. Azure VM Lauch 
2. Settings >> Monitoring >> Create Alert Rule >> CPU Utilization < 40% 
3. Create Action Group >> email, mobile
4. ssh to VM

sudo apt update -y 
sudo apt install stress -y 
stress --version 

stress --cpu 8 --io 4 --vm 2 --vm-bytes 128M --timeout 1s
stress --cpu 4 --io 4 --vm 2 --vm-bytes 128M --timeout 2s
stress --cpu 8 --io 4 --vm 2 --vm-bytes 128M --timeout 1s
stress --cpu 4 --io 4 --vm 2 --vm-bytes 128M --timeout 2s
stress --cpu 8 --io 4 --vm 2 --vm-bytes 128M --timeout 1s

5. check mail

6. Install Node Exporter, Prometheus, Grafana 

https://github.com/atulkamble/AzureVM-Grafana-Prometheus-Node-Exporter

7. Data Sources >> Prometheus import 

8. Create Dashboard 

6417
11074
405
10180
3662
1860





```
