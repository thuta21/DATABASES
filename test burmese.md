Documentations  
[MongoDB Methods Reference](https://www.mongodb.com/docs/manual/reference/method/js-collection/)

## 1. Launch Mongo Shell

Terminal မှာ `mongosh` ရိုက်ပြီး စမ်းလို့ရပါပြီ။

```bash
mongosh
```

ဒါပေမယ့် ကိုယ့် project တစ်ခုရှိပြီး Cluster တစ်ခု setup လုပ်ထားရင် `connect` ကို နှိပ်ရပါမယ်။

![01_Clusters](images/01_Clusters.png)

`Connect` ပြီးတဲ့အခါမှာ အောက်ပါ dialog ပေါ်လာပြီး အဲ့ဒီထဲက `Shell` ကိုရွေးပါ။

![02_Clusters](images/02_Clusters.png)

ပြီးရင် `Shell` ကို စနစ်တကျ setup လုပ်နိုင်ပါပြီ။

![03_Clusters](images/03_Clusters.png)

---

## 2. `show` and `use` Databases

MongoDB Shell မှာ databases တွေကို `show dbs` command ရိုက်ပြီး ကြည့်နိုင်ပါတယ်။

```bash
show dbs;
```

![04_Clusters](images/04_Clusters.png)

`mongo_testing` database ကို ဆောက်ထားမို့ အဲ့ဒီ database ကို သုံးမယ်။

```bash
use mongo_testing
```

![05_Clusters](images/05_Clusters.png)

---

## 3. `create database` and `drop database`

Database တစ်ခု အသစ်တည်ဆောက်ဖို့ လွယ်ကူပါတယ်။ `use <database_name>` command သုံးရုံပါပဲ။ ဥပမာ `books` database အသစ်တစ်ခု ဆောက်ချင်တယ်ဆိုရင်

```bash
use books
```

![06_create_dbs](images/06_create_db.png)

Database မှာ documents မရှိသေးတဲ့အတွက် `show dbs` မှာမတွေ့နိုင်ပါဘူး၊ အဲ့ဒါကြောင့် collections တစ်ခုဆောက်ပါမယ်။

```bash
db.createCollection('biography')
```

![07_create_collection](images/07_create_collection.png)

Database တွေပြန်စစ်ကြည့်မယ်ဆိုရင်

```bash
show dbs;
```

![08_showDBs](images/08_showDBs.png)

Database ကိုဖျက်ချင်ရင် `db.dropDatabase()` command သုံးနိုင်ပါတယ်။

```bash
db.dropDatabase();
```

---

## 4. `Insert` and `InsertMany`

`mongo_testing` database ထဲမှာ `users` collection တစ်ခု ဆောက်ပြီး စမ်းကြည့်ပါမယ်။

![09_insert](images/09_insert.png)

```bash
db.users.insert({name: "Thuta Min Thway", age: 23, height: "5foot 9inches", isStudent: true})
db.users.find()
```

တစ်ခါတည်းမှာ records အများကြီး ထည့်ချင်ရင် `insertMany()` ကို သုံးနိုင်ပါတယ်။

```bash
db.users.insertMany([
  { name: "Aung Aung", age: 25, height: "5foot 10inchs", isStudent: false },
  { name: "Su Su", age: 22, height: "5foot 5inchs", isStudent: true },
  ...
]);
```

---

## 5. `find` / `findOne` / `count` / `limit` / `toArray`

Records တွေရှာချင်ရင် `find()` သုံးနိုင်ပါတယ်။

```bash
db.users.find()
```

တစ်ခုလောက်တင်ရှာချင်ရင် `findOne()` သုံးပါ။

```bash
db.users.findOne()
```

Filters လုပ်ချင်ရင် parameter ထည့်နိုင်ပါတယ်။

```bash
db.users.find({age: 25})
```

Counting လုပ်မယ်ဆိုရင် `count()` သုံးပါ။

```bash
db.users.count({age: 25, isStudent: true})
```

Data တွေကို တစ်ခုပဲ ပြချင်ရင် `limit()` သုံးပါ။

```bash
db.users.find().limit(10)
```

Array ပြောင်းချင်ရင် `toArray()` သုံးပါ။

```bash
db.users.find().limit(10).toArray()
```

---

## 6. Querying Operators

Filters တွေ အသုံးပြုနိုင်သလို operators တွေသုံးလို့လည်းရပါတယ်။ အသက် 25 နှစ်အောက် ကျောင်းသားမဟုတ်တဲ့သူတွေ ရှာကြည့်ရအောင်။

```bash
db.users.find({
  isStudent: false,
  age: { $lt: 25 }
})
```

- $gt - greater than  
- $gte - greater than or equal to  
- $lt - less than  
- $lte - less than or equal to  
- $eq - equals  
- $ne - not equals  
- $in - has the value in the array  
- $nin - does not have the value in the array  

---

## 7. Logical Query

Documentation: [MongoDB Logical Query Operators](https://www.mongodb.com/docs/manual/reference/operator/query-logical/)

- $and  
- $not  
- $nor  
- $or  

ဥပမာ အသက် 23 ကနေ 25 အထိ ကျောင်းသားတွေကို ရှာကြည့်ပါ။

```bash
db.users.find({
  isStudent: true,
  $and: [{ age: { $gte: 23 } }, { age: { $lte: 25 } }]
})
```

---

## 8. Sorting (`sort`)

Ascending နဲ့ Descending အလိုက် Data တွေကို sort လုပ်နိုင်ပါတယ်။

Ascending by Age:

```bash
db.users.find().sort({ age: 1 })
```

Descending by Age:

```bash
db.users.find().sort({ age: -1 })
```

---

## 9. Datatypes

Datatypes မျိုးစုံထည့်ပြီး record တစ်ခု လုပ်ကြည့်ပါမယ်။

```bash
db.users.insertOne({
  name: "Thuta Min Thway",
  age: 23,
  height: 5.9,
  isStudent: true,
  birthDate: new Date("2000-01-01"),
  address: { street: "123 Main St", city: "Yangon", zipCode: 11011 },
  hobbies: ["reading", "coding", "gaming"],
  contact: null,
  score: NumberLong("9223372036854775807"),
  randomBytes: new BinData(0, "1234"),
  idNumber: ObjectId(),
  grades: { math: Decimal128("85.75") },
  extraInfo: undefined
});
```

---

## 10. Projection

Projection သုံးပြီး Specific keys တွေကို filter လုပ်နိုင်ပါတယ်။

```bash
db.users.find({}, {name: true})
```

ID မပါစေချင်ရင်:

```bash
db.users.find({}, {_id: false, name: true})
```

> false အစား 0 သုံးလို့ရပါတယ်  
> true အစား 1 သုံးလို့ရပါတယ်

---

## 11. `updateOne` / `updateMany` / `delete`

Update ပြင်ဖို့ `$set` သုံးပါ။

```bash
db.users.updateOne({_id: ObjectId("66e7b28c83faebe98283f728")}, {$set: {name: "tony Tun Tun"}})
```

> Update, Delete and more manipulation commands can be done similarly to Insert.