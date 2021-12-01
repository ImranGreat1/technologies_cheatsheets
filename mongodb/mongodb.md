## Creating Document

**Creating single document**
~~~bash
    db.collectionName.insertOne(documentObject)
~~~

**Creating multiple documents at once**
~~~bash
    db.collectionName.insertMany(arrayOfDocumentsObject)
~~~

## Queries

**Find all documents in a collection**

_This will return an array of all the documents in the collection_
~~~bash
    db.collectionName.find()
~~~

_This will return an array of all matched documents in the collection_
~~~bash
    db.collectionName.find(queryObject)
~~~
