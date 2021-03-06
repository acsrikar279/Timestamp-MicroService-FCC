
# API Project: Timestamp Microservice for FCC

### User stories :

1. The API endpoint is `GET [project_url]/api/timestamp/:date_string?`
2. A date string is valid if can be successfully parsed by `new Date(date_string)` (JS) . Note that the unix timestamp needs to be an **integer** (not a string) specifying **milliseconds**. In our test we will use date strings compliant with ISO-8601 (e.g. `"2016-11-20"`) because this will ensure an UTC timestamp.
3. If the date string is **empty** it should be equivalent to trigger `new Date()`, i.e. the service uses the current timestamp.
4. If the date string is **valid** the api returns a JSON having the structure 
`{"unix": <date.getTime()>, "Date is " : <date.toUTCString()> }`
e.g. `{"unix": 1479663089000 ,"Date is ": "Sun, 20 Nov 2016 17:31:29 GMT"}`.
5. If the date string is **invalid** the api returns a JSON having the structure `{"unix": null, "Date is " : "Invalid Date" }`. It is what you get from the date manipulation functions used above.

#### Example usage:
* https://time-rainstorm.glitch.me/api/timestamp/2015-12-15
* https://time-rainstorm.glitch.me/api/timestamp/1450137600000
* https://time-rainstorm.glitch.me/api/timestamp/

#### Example output:
* {"unix":1535786291939,"Date is ":"Sat, 01 Sep 2018 07:18:11 GMT"}
