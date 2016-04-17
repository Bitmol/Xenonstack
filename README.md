# Xenonstack-Internship

## Instructions :-

**Collecting** and **transferring** system metrics in real time.The softwares used are:-
  
  1. Elasticsearch
  2. Topbeat
  3. Kibana

## Metrics :-

The various metrics which were recorded include :-
  
**1. System-wide statistics** :- 

  - System load: in the last minute, in the last 5 minutes, and in the last 15 minutes 
  - System wide CPU usage: user (and percentage), system, idle, IOWait, and so on at both per
    CPU and overall level 
  - System wide memory usage: total, used (and percentage), free, and so on 
  - System wide swap usage: total, used (and percentage), free, and so on 
 
**2. Per-process statistics** :-
 
  - Process name 
  - Process parent pid 
  - Process state 
  - Process pid 
  - Process CPU usage: user (and percentage), system, total, and start time 
  - Process Memory usage: virtual memory, resident memory (and percentage), and shared   memory 

**3. File system statistics** :- 
 
  - List of available disks 
  - For each disk, the name, type, and where it is mounted 
  - For each disk, the total, used (and percentage), free, and available space 

## Installation and Description :-

- Installation of the software was done as per the guidelines given in the documentation.Elasticsearch was used as the analytics engine, and topbeat is primarily used in montitoring the statistics of system-wide and per-process performance of the server in real time.The data thus obtained is stored and indexed in the form of nodes in elasticsearch.Visualization and charting of the data is done using a GUI called kibana.

- Files included in this repo contain :-

  - **Instructions.pdf** :- Instructions which was to be carried out.
  
  - **Kibana snapshots folder** :- Contain the monitored results in the form of html pages of kibana, while running the server.
  
  - **Kibana.yml** :- YAML configuration file for kibana, modifications were done for working with Elasticsearch.Inherent elasticsearch port is 9200 when initially enabled,hence ,kibana is made to point to that url by enabling the elasticsearch url field in the yaml file and specifying the url.Other options are kept as default.
  
  - **Topbeat.yml** :- YAML configuration file for topbeat, modifications were done for implementing data capture using Topbeat and Elasticsearch.Template name is given as "topbeat" and the path provided is the `/Users/anmol/Downloads` directory on my machine.Elasticsearch output is enabled and monitoring is done on 1-minute basis (60 seconds,parameter is given in seconds).System,processes and filesystem statistics monitoring is enabled.Other options are kept as default.
  
  - **Topbeat.template.json** :- JSON file containing the general index template which is loaded in the `topbeat.yml` file.Generally present as default in the topbeat directory,for which slight modifications must be introduced.
   


- The ETK stack (Elasticsearch,Topbeat,Kibana) was found to be running optimally on the following configuration :-
  
  - Test machine configuration :-
  
    - OS :- OSX El Capitan --version 10.11.2
    - Processor :- 2.5 GHz Intel Core i5
    - Memory :- 16 GB 1600 MHz DDR3
    - Graphics :- Intel HD Graphics 4000 1536 MB


 
  
