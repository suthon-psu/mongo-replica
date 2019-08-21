# Run
... make sure that mongodb1, mongodb2, mongodb3 directories are created.
```
>> docker-compose up -d
```
---
```
>> docker exec -it mongo1 mongo
```
```javascript
rs.initiate( {
   _id : "rs0",
   members: [
      { _id: 0, host: "mongo1:27017" },
      { _id: 1, host: "mongo2:27017" },
      { _id: 2, host: "mongo3:27017" }
   ]
})
```