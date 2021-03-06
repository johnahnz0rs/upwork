# Instructions

The goal of this test is to create an API for finding the nearest coffee shop by providing an address. You may use any language to build your API server.

You are provided with a list of coffee shops with their geo locations and must read in this file to populate an initial data set. You may use a database if you wish, but in the interest of time a simple data structure in memory is expected.

The file (locations.csv) is in comma separated value format with 5 columns and looks like:
```
id, name, address, latitude, longitude
```

After reading in the initial data set, you should build a server with a REST API that can create a new coffee shop, return the details of a coffee shop given its id, update, or delete a coffee shop.

Finally, you will build an endpoint that takes in an address and returns the nearest coffee shop that is currently in the list.

In total there are 5 endpoints to implement that will return JSON responses to the client:

**Create** - Accepts name, address, latitude, and longitude, adds a new coffee shop to the data set, and returns the id of the new coffee shop.

**Read** - Accepts an id and returns the id, name, address, latitude, and longitude of the coffee shop with that id, or an appropriate error if it is not found.

**Find nearest** - Accepts an address and returns the closest coffee shop by straight line distance.
- For example, based upon the initial data set, if the user passes in an address of "535 Mission St., San Francisco, CA", the correct response from your server should be Red Door Coffee (id: 16).
- Another example, using the address "252 Guerrero St, San Francisco, CA 94103, USA", would return Four Barrel Coffee.
- Hint: Google provides a free geocoding API.

**Update** - Accepts an id and new values for the name, address, latitude, or longitude fields, updates the coffee shop with that id, or returns an appropriate error if it is not found.

**Delete** - Accepts an id and deletes the coffee shop with that id, or returns an error if it is not found

---

The data set does not need to be persisted back to the data file, it is ok to simply update the data structure in memory and lose any changes when the server is stopped.

Please provide a readme file in the code base that contains instructions on how to compile and run your server as well as the urls and structure of your API. We should be able to follow your instructions to run the server locally, and test out your API.
