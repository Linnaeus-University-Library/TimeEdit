

#### Examples


get all the types available
```javascript

const TimeEdidApi = require('timeeditApi');

TimeEdidApi.getAllTypes(
        'https://se.timeedit.net/web/lnu/db1/schema1/')
    .then((result) => {
        console.log(JSON.stringify(result, null ,2));
    }).catch((er) => {
        console.log(er);
    });
```

Get schedule
```javascript
const TimeEdidApi = require('timeeditApi');

const timeEdidApi = new TimeEdidApi(
    'https://se.timeedit.net/web/lnu/db1/schema1/',
    4
);

// todays schedule
timeEdidApi.getTodaysSchedule('ny105')
    .then((roomSchedule) => {
        console.log(JSON.stringify(roomSchedule, null ,2));
    }).catch((er) => {
        console.log(er);
    });

// full schedule
timeEdidApi.getSchedule('ny105')
    .then((schedule) => {
        console.log(JSON.stringify(schedule, null ,2));
    }).catch((er) => {
        console.log(er);
    });

// search and se if exists
timeEdidApi.search('ny105')
    .then((result) => {
        console.log(JSON.stringify(result, null ,2));
    }).catch((er) => {
        console.log(er);
    });

```

Get schedule by schedule url
```javascript

const TimeEdidApi = require('timeeditApi');

// get schedule by schedule url
TimeEdidApi.getScheduleByScheduleUrl(
        'https://se.timeedit.net/web/lnu/db1/schema1/s.html?i=6Y7XYQQ7wZ36QvZ5071875y7YQ8')
    .then((result) => {
        console.log(JSON.stringify(result, null ,2));
    }).catch((er) => {
        console.log(er);
    });


```
