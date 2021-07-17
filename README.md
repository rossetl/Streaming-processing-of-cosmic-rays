# Streaming processing of cosmic rays' signal
The aim of this project was to build a dashboard for the live monitoring of Drift Tube Detectors in a distributed fashion.

To this end, we were given 5 virtual machines hosted in the Cloud Veneto infrastructure in order to build a small cluster.</br>
Data are extracted from an S3 bucket by the `Producer` notebook and injected inside a Kafka topic as a continuous stream. In the `Spark-cluster` notebook, we then access those data and process them to get some high-level features that give a visual clue of the detecting process. The results are then sent into another Kafka topic and eventually extracted and visualized in the dashboard of the `Consumer` notebook. 


All the details about the cluster and the processing can be found in the `Spark-cluster` notebook.

<p align="center">
<img src="https://github.com/rossetl/Streaming-processing-of-cosmic-rays/blob/main/images/preview.png" alt="schema" width="600"/>
</p>
