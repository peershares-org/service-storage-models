_**Notice**: Development on this repo is deprecated as we continue our v3 rearchitecture. Please see https://github.com/storj/storj for ongoing v3 development._

Czarcoin Service Storage Models
============================

[![Build Status](https://img.shields.io/travis/Storj/service-storage-models.svg?style=flat-square)](https://travis-ci.org/Storj/service-storage-models)
[![Coverage Status](https://img.shields.io/coveralls/Storj/service-storage-models.svg?style=flat-square)](https://coveralls.io/github/Storj/service-storage-models?branch=master)
[![GitHub license](https://img.shields.io/badge/license-LGPLv3-blue.svg?style=flat-square)](https://raw.githubusercontent.com/Storj/service-storage-models/master/LICENSE)

Common storage models for various Storj services

```
npm install storj-service-storage-models --save
```

```js
var Storage = require('storj-service-storage-models');
var db = new Storage(
  'mongodb://127.0.0.1:27017/storj-bridge-database-name',
{
  auth: {
    user: 'myuser',
    pass: 'mypassword'
  },
  mongos: {
    ssl: true
  }
},
{
  logger: myAwesomeLogger
});

db.models.User.findOne({ email: 'gordon@storj.io' }, function(err, user) {
  if (err) {
    console.error(err.message);
  } else {
    console.info(user);
  }
});
```


#### Coinpayments Integration 

You'll have to set Coinpayments environment variables `CP_PUBLIC_KEY` and `CP_SECRET_KEY` in order to get coinpayments client working with the payment processor adapter. 



#### Billing Specific

If using billing functionality, be sure to include your own `.env` file with necessary environment variables.
