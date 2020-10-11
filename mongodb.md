```
use dbname;
db.dropDatabase();
```

```
mongodump --host 1.2.3.4 -d database --port 27017 --username username --password password --out dump
```

```
mongo 1.2.3.4 -u username --authenticationDatabase admin -p
```

```
mongoexport --db database --collection collection --out filename.json --host 1.2.3.4 --username username --password password --authenticationDatabase admin
mongoimport --db database --collection collection --file filename.json --host 127.0.0.1
```

```
db.collection.update({name: {$ne: null}}, { '$set': { name: null } }, {multi: true});
```