# mtd_mern_26
Author:Nithyashree
Microsoft Windows [Version 10.0.26200.8037]
(c) Microsoft Corporation. All rights reserved.

C:\Users\nithy>mongosh "mongodb+srv://nithyashree:1234@cluster0.i9oriqt.mongodb.net/"
Current Mongosh Log ID: 69d31b11d5d560a4b43682d0
Connecting to:          mongodb+srv://<credentials>@cluster0.i9oriqt.mongodb.net/?appName=mongosh+2.8.2
MongoNetworkError: certificate is not yet valid

C:\Users\nithy>mongosh "mongodb+srv://nithyashree:1234@cluster0.i9oriqt.mongodb.net/"
Current Mongosh Log ID: 69d369d1ff3247e3893682d0
Connecting to:          mongodb+srv://<credentials>@cluster0.i9oriqt.mongodb.net/?appName=mongosh+2.8.2
Using MongoDB:          8.0.20
Using Mongosh:          2.8.2

For mongosh info see: https://www.mongodb.com/docs/mongodb-shell/


To help improve our products, anonymous usage data is collected and sent to MongoDB periodically (https://www.mongodb.com/legal/privacy-policy).
You can opt-out by running the disableTelemetry() command.

Atlas atlas-kvowqz-shard-0 [primary] test> show dbs
admin  360.00 KiB
local   33.17 GiB
Atlas atlas-kvowqz-shard-0 [primary] test> C:\Users\nithy>mongosh "mongodb+srv://nithyashree:1234@cluster0.i9oriqt.mongoAtlas atlas-kvowqz-shard-0 [primary] test> exit

C:\Users\nithy>mongosh "mongodb+srv://nithyashree:1234@cluster0.i9oriqt.mongodb.net/"
Current Mongosh Log ID: 69d375846a785377553682d0
Connecting to:          mongodb+srv://<credentials>@cluster0.i9oriqt.mongodb.net/?appName=mongosh+2.8.2
Using MongoDB:          8.0.20
Using Mongosh:          2.8.2

For mongosh info see: https://www.mongodb.com/docs/mongodb-shell/

Atlas atlas-kvowqz-shard-0 [primary] test> show dbs
admin  360.00 KiB
local   33.17 GiB
Atlas atlas-kvowqz-shard-0 [primary] test> use db.trainers.insertOne({"name":"nithin","skills":"javascript","photo":""})
MongoshInvalidInputError: [COMMON-10001] Invalid database name: db.trainers.insertOne({"name":"nithin","skills":"javascript","photo":""})
Atlas atlas-kvowqz-shard-0 [primary] test> use trainer_app_db
switched to db trainer_app_db
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> show database
MongoshInvalidInputError: [COMMON-10001] 'database' is not a valid argument for "show".
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> show databases
admin  360.00 KiB
local   33.17 GiB
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.trainers.insertOne({"name":"sanvi","skills":"javascript","photo":""})
{
  acknowledged: true,
  insertedId: ObjectId('69d377206a785377553682d1')
}
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> show databases
trainer_app_db   40.00 KiB
admin           360.00 KiB
local            33.17 GiB
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> show collections
trainers
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.trainers.find()
[
  {
    _id: ObjectId('69d377206a785377553682d1'),
    name: 'sanvi',
    skills: 'javascript',
    photo: ''
  }
]
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.trainers.insertOne({"name":"sanu","skills":"python","photo":""})
{
  acknowledged: true,
  insertedId: ObjectId('69d3779e6a785377553682d2')
}
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.trainers.find()
[
  {
    _id: ObjectId('69d377206a785377553682d1'),
    name: 'sanvi',
    skills: 'javascript',
    photo: ''
  },
  {
    _id: ObjectId('69d3779e6a785377553682d2'),
    name: 'sanu',
    skills: 'python',
    photo: ''
  }
]
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.trainers.find({name:"sanvi"})
[
  {
    _id: ObjectId('69d377206a785377553682d1'),
    name: 'sanvi',
    skills: 'javascript',
    photo: ''
  }
]
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.trainers.updateOne({"name":"sanu"},{$set:{"skills":"c#"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> show dbs
trainer_app_db   72.00 KiB
admin           360.00 KiB
local            33.17 GiB
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.admins.insertMany([{"email":"devikack2020@gmal.com","password":"1234","role":"manager"},{"email":"nithyapankaja@gmail.com","password":"1234","role":"agent"}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('69d379346a785377553682d3'),
    '1': ObjectId('69d379346a785377553682d4')
  }
}
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.admins.find()
[
  {
    _id: ObjectId('69d379346a785377553682d3'),
    email: 'devikack2020@gmal.com',
    password: '1234',
    role: 'manager'
  },
  {
    _id: ObjectId('69d379346a785377553682d4'),
    email: 'nithyapankaja@gmail.com',
    password: '1234',
    role: 'agent'
  }
]
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.admins.find({"email":"devikack2020@gmail.com"})

Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.admins.findOne({"email":"devikack2020@gmail.com"})
null
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> db.admins.findOne({"email":"devikack2020@gmal.com"})
{
  _id: ObjectId('69d379346a785377553682d3'),
  email: 'devikack2020@gmal.com',
  password: '1234',
  role: 'manager'
}
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> show dbs
trainer_app_db  144.00 KiB
admin           360.00 KiB
local            33.17 GiB
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> use db.mobile.insertOne({"id":"123","name":"samsung","model":"samsungm14","price":"30000","photo":""})
MongoshInvalidInputError: [COMMON-10001] Invalid database name: db.mobile.insertOne({"id":"123","name":"samsung","model":"samsungm14","price":"30000","photo":""})
Atlas atlas-kvowqz-shard-0 [primary] trainer_app_db> use mobile_db
switched to db mobile_db
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> show databases
trainer_app_db  144.00 KiB
admin           360.00 KiB
local            33.17 GiB
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> show collections

Atlas atlas-kvowqz-shard-0 [primary] mobile_db> use db.mobile.insertOne({"id":"123","name":"samsung","model":"samsungm14","price":"30000","photo":""})
MongoshInvalidInputError: [COMMON-10001] Invalid database name: db.mobile.insertOne({"id":"123","name":"samsung","model":"samsungm14","price":"30000","photo":""})
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> use db.mobile_db.insertOne({"id":"123","name":"samsung","model":"samsungm14","price":"30000","photo":""})
MongoshInvalidInputError: [COMMON-10001] Invalid database name: db.mobile_db.insertOne({"id":"123","name":"samsung","model":"samsungm14","price":"30000","photo":""})
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.insertOne({"id":"123","name":"samsung","model":"samsungm14","price":"30000","photo":""})
{
  acknowledged: true,
  insertedId: ObjectId('69d37fbc6a785377553682d5')
}
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> show collections
mobile_db
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.find()
[
  {
    _id: ObjectId('69d37fbc6a785377553682d5'),
    id: '123',
    name: 'samsung',
    model: 'samsungm14',
    price: '30000',
    photo: ''
  }
]
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.insertOne({"id":"1234","name":"vivo","model":"vivo x90 pro/x100 pro","price":"50000","photo":""})
{
  acknowledged: true,
  insertedId: ObjectId('69d380c96a785377553682d6')
}
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.find()
[
  {
    _id: ObjectId('69d37fbc6a785377553682d5'),
    id: '123',
    name: 'samsung',
    model: 'samsungm14',
    price: '30000',
    photo: ''
  },
  {
    _id: ObjectId('69d380c96a785377553682d6'),
    id: '1234',
    name: 'vivo',
    model: 'vivo x90 pro/x100 pro',
    price: '50000',
    photo: ''
  }
]
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.insertOne({"id":"12345","name":"apple","model":"iphone12promax","price":"100000","photo":""})
{
  acknowledged: true,
  insertedId: ObjectId('69d382466a785377553682d7')
}
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.insertOne({"id":"12345","name":"xiaomi","model":"15 ultra","price":"100000","photo":""})
{
  acknowledged: true,
  insertedId: ObjectId('69d382686a785377553682d8')
}
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.insertOne({"id":"12345","name":"oneplus","model":"12 pro","price":"100000","photo":""})
{
  acknowledged: true,
  insertedId: ObjectId('69d382926a785377553682d9')
}
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.insertOne({"id":"12345","name":"motorola","model":"edge 70 fusion","price":"100000","photo":""})
{
  acknowledged: true,
  insertedId: ObjectId('69d382bc6a785377553682da')
}
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.insertOne({"id":"1234567","name":"POCO","model":"x8 pro max","price":"150000","photo":""})
{
  acknowledged: true,
  insertedId: ObjectId('69d382f56a785377553682db')
}
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.insertOne({"id":"12345678","name":"IQOO","model":"15 apex","price":"80000","photo":""})
{
  acknowledged: true,
  insertedId: ObjectId('69d383456a785377553682dc')
}
Atlas atlas-kvowqz-shard-0 [primary] mobile_db> db.mobile_db.find()
[
  {
    _id: ObjectId('69d37fbc6a785377553682d5'),
    id: '123',
    name: 'samsung',
    model: 'samsungm14',
    price: '30000',
    photo: ''
  },
  {
    _id: ObjectId('69d380c96a785377553682d6'),
    id: '1234',
    name: 'vivo',
    model: 'vivo x90 pro/x100 pro',
    price: '50000',
    photo: ''
  },
  {
    _id: ObjectId('69d382466a785377553682d7'),
    id: '12345',
    name: 'apple',
    model: 'iphone12promax',
    price: '100000',
    photo: ''
  },
  {
    _id: ObjectId('69d382686a785377553682d8'),
    id: '12345',
    name: 'xiaomi',
    model: '15 ultra',
    price: '100000',
    photo: ''
  },
  {
    _id: ObjectId('69d382926a785377553682d9'),
    id: '12345',
    name: 'oneplus',
    model: '12 pro',
    price: '100000',
    photo: ''
  },
  {
    _id: ObjectId('69d382bc6a785377553682da'),
    id: '12345',
    name: 'motorola',
    model: 'edge 70 fusion',
    price: '100000',
    photo: ''
  },
  {
    _id: ObjectId('69d382f56a785377553682db'),
    id: '1234567',
    name: 'POCO',
    model: 'x8 pro max',
    price: '150000',
    photo: ''
  },
  {
    _id: ObjectId('69d383456a785377553682dc'),
    id: '12345678',
    name: 'IQOO',
    model: '15 apex',
    price: '80000',
    photo: ''
  }
]
