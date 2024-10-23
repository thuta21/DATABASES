# MongoDB

  

## MongoDB ၏ အခြေခံအချက်များ

  

MongoDB သည် အရွယ်ကြီးမားသော ဒေတာများကို ထိန်းချုပ်ရန် အသုံးပြုသော NoSQL ဒေတာဘေ့စ်တစ်ခုဖြစ်ပြီး JSON-ပုံစံ ရှိသော ဒေတာများကို စနစ်တကျ သိမ်းဆည်းနိုင်ပါသည်။ MongoDB ၏အဓိကသက်ရောက်မှုများအနက် အဓိကမှာ scalability, flexibility နှင့် အမြန်နှုန်းများ ဖြစ်ပါသည်။

  

## MongoDB တွင် Collection နှင့် Document များ

  

MongoDB တွင် ဒေတာများကို Collection နှင့် Document အဖြစ် သိမ်းဆည်းသည်။ Collection သည် MySQL တွင်ရှိသော table နှင့် ဆင်တူပြီး Document သည် row နှင့် ဆင်တူပါသည်။

  

- ****Document**** - JSON ပုံစံအတိုင်း key-value ပုံစံဖြင့် သိမ်းဆည်းသည်။

- ****Collection**** - Document များ၏ စုပေါင်းမှု။

  

## MongoDB Commands

  

MongoDB တွင် အရေးကြီးသော commands များမှာ အသုံးပြုသူများ ဒေတာများကို query, insert, update, delete ပြုလုပ်ရာတွင် အသုံးပြုသည်။

  

### Create Operation

  

```javascript

db.collection.insertOne({ name: "Aung Aung", age: 25 });

```

  

- MongoDB တွင် အသစ်သော document တစ်ခုကို collection ထဲသို့ ထည့်သွင်းပါသည်။

  

### Read Operation

  

```javascript

db.collection.find({ name: "Aung Aung" });

```

  

- MongoDB မှာ ပေးထားသော query အတိုင်း document များကို ရှာဖွေပါသည်။

  

### Update Operation

  

```javascript

db.collection.updateOne({ name: "Aung Aung" }, { $set: { age: 26 } });

```

  

- MongoDB မှာ ပေးထားသော condition အတိုင်း document ကို ပြင်ဆင်သည်။

  

### Delete Operation

  

```javascript

db.collection.deleteOne({ name: "Aung Aung" });

```

  

- MongoDB မှာ ပေးထားသော condition အတိုင်း document ကို ဖျက်ပစ်သည်။

  

## Indexes

  

MongoDB တွင် indexes သည် queries များကို အရှိန်မြှင့်ခြင်းအတွက် အထောက်အကူပြုသည်။

  

```javascript

db.collection.createIndex({ name: 1 });

```

  

- `createIndex()` သည် MongoDB မှာ collection ၏ particular field ကို index ဖန်တီးပါသည်။

  

## Aggregation

  

MongoDB ၏ Aggregation framework သည် ဒေတာများကို စုစည်းရန်နှင့် ပြန်လည် ထုတ်ယူရန်အတွက် အသုံးပြုသည်။

  

```javascript

db.collection.aggregate([

  { $match: { status: "active" } },

  { $group: { _id: "$category", total: { $sum: "$amount" } } }

]);

```

  

## MongoDB Advantages

  

- ****Scalability**** - MongoDB သည် horizontal scaling ကို အထောက်အပံ့ပေးသည်။

- ****Flexibility**** - Schema-less database ဖြစ်သောကြောင့် flexible ဖြစ်သည်။

- ****Speed**** - Queries များကို အမြန်ဆုံး အချိန်အတွင်း ရယူနိုင်သည်။

  

## MongoDB Disadvantages

  

- ****Consistency**** - MongoDB ၏ eventual consistency မှာ အချို့သော application များတွင် စိန်ခေါ်မှုဖြစ်နိုင်သည်။

- ****Memory Usage**** - MongoDB သည် memory စားသုံးမှုများ ရှိသည်။