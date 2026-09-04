# uber_end_to_end_streaming_project
Data Engineering End to End Databricks Streaming Project

Architecture

<img width="607" height="399" alt="image" src="https://github.com/user-attachments/assets/9bf93030-93ae-4fab-85e6-f448c038eeb0" />

Application to Event Hub
<img width="711" height="317" alt="image" src="https://github.com/user-attachments/assets/50787822-c24f-4ffd-9011-6288c7982efc" />

<img width="806" height="404" alt="image" src="https://github.com/user-attachments/assets/1519ce71-b40a-43b3-a50a-cab93dcbb37b" />

Github API to ADLS gen 2
<img width="694" height="402" alt="image" src="https://github.com/user-attachments/assets/cbe6ccaa-c15e-4043-be9d-214334171311" />


Event hub to bronze using databricks 

SDP - spark declarative Pipelines 
DLT is renamed as sdp + Earlier dlt was just databricks product, databricks has contributed dlt or sdp to apache spark.

Apache Spark declarative Pipelines - take care about what and not about how.

What are the benefits of SDP?
1. automatic orchestration
2. Declarative processing - auto cdc (takes care of slowly changing dimensions)
3. Incremental Processing - Materialised views (process the incremental data)

Key concepts
1. Streaming Sources -- > Streaming Processing (Append Flow, Auto CDC flow) ---> Streaming Target (Sink, Streaming Table)
2. Batch Source --> Batch Processing (Materialised view flow) --> Batch Target(Materialised View)

   It takes care of everything
   checkpoint location, files
   schema
   state management
   idempotency


Major important
1. Streaming Tables
2. Streaming Views
3. Materialised views
4. Sink (normal tables)--> data lake
5. Normal View

Can use sql or pyspark API

SDP has a own code editor, DAG visualizations


<img width="791" height="324" alt="image" src="https://github.com/user-attachments/assets/2d06af71-f050-42c2-96a9-a6108d808d2a" />


ADLS GEN 2 to bronze - using databricks

NOTE: 

When we are reading mapping files

we dont not need to create a pyspark dataframe. why? we create because we are working with the big data. 

When we want to load the mapping or static files - always go with pandas dataframe.




