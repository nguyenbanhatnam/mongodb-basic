mongoimport "location of file json" -d namDatabase -c namCollection --jsonArray --drop
mongoimport "C:\Users\namde\Downloads\MOCK_DATA.json" -d namDatabase -c namCollection --jsonArray

 use('test');

 db.createCollection("weather",{timeseries: {timeField: "timestamp",granularity: "hours",bucketMaxSpanSeconds: 60,bucketRoundingSeconds: 60}})