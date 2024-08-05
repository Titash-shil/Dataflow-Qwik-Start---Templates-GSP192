# Dataflow: Qwik Start - Templates || [GSP192](https://www.cloudskillsboost.google/focuses/1101?parent=catalog) ||

# # Like, comment, share & Don't forget to subscribe [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN) 👍😄🤝

* ### Run the following Commands in CloudShell
```
gcloud services disable dataflow.googleapis.com

gcloud services enable dataflow.googleapis.com

bq mk taxirides
bq mk \
--time_partitioning_field timestamp \
--schema ride_id:string,point_idx:integer,latitude:float,longitude:float,\
timestamp:timestamp,meter_reading:float,meter_increment:float,ride_status:string,\
passenger_count:integer -t taxirides.realtime

gsutil mb gs://$DEVSHELL_PROJECT_ID/

sleep 45

gcloud dataflow jobs run iotflow \
--gcs-location gs://dataflow-templates/latest/PubSub_to_BigQuery \
--region $REGION \
--staging-location gs://$DEVSHELL_PROJECT_ID/temp \
--parameters inputTopic=projects/pubsub-public-data/topics/taxirides-realtime,outputTableSpec=$DEVSHELL_PROJECT_ID:taxirides.realtime
```

# Congratulations ..!!🎉  You completed the lab shortly..😃💯

# *Well done..!* 👏

# Thank you for visiting.... :) 🗯️

# [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN) 
