# ObjectStore
This project is created using Mule 4.2.2 and Anypoint Studio 7.4.2 to demonstrate the different capabilities of Object Store.

Sample URLs:
============

1. To store the object store key value pairs:
http://localhost:8081/objectstore?key=familyKey (POST)
Sample data: {
	"familyname":"Parashar's",
	"sector":"Service"
}

2. SpecificKey retrieve:
http://localhost:8081/objStoreOps?op=specificRetrieve&key=familyKey (GET)

3. empty the object store
http://localhost:8081/emptyObjStore

4. cleanup based on a specific key
http://localhost:8081/emptyObjStore?op=remove&key=familyKey

Tips:
1. in Store option, if you wan to restrict the key,value option to check for duplicates (should fail if exists), use the configuration "Fail if present -> true"
Similarly if you want to make flow to fail if there is no value to key(during startup or shutdown), use the configuration "Fail on null value -> true"
