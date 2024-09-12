
Content 
1. What is NoSQL?

------------------------------------------------------------------------

1. What is NoSQL?
   
   NoSQL ဆိုတဲ့ အတိုင်းပဲ Basically Relational Database မဟုတ်ဘူးပေါ့။ NoSQL ကို "Non-SQL", "Non-Relational" ဒါမှမဟုတ် "Not Only SQL" ဆိုပြီး အခေါ်အဝေါ်တွေ ရှိပါတယ်။ 
   
   NoSQL မစခင်မှာ NoSQL ကို မသုံးပဲ ​RDBMS ကို ပဲ သုံးလို့မရဘူးလား။ ဒါဆို ပြန် Recap ကြည့်ရအောင်။ RDBMS က Fixed Schema ဖြစ်တယ်။ Data Consistant ဖြစ်တယ်။ Data ပမာဏ အများကြီးကို သိမ်းတဲ့ နေရာမှာ Challenging ဖြစ်တယ်။ RDBMS က Data များလာရင် Handle နိုင်တဲ့ နည်းလမ်း က Vartical Scaling လုပ်လိုက်တာ ( လိုအပ်တဲ့ CPU / Memory တွေကို လိုက်မြှင့်တာ )။ ​  
   
   ဒါဆို NoSQL ကို ပြန်ဆက်ရအောင်။ NoSQL က Fixed Schema မဟုတ်ဘူး။ ဒါကြောင့် Scalability လုပ်ရတာ အဆင်ပြေတယ်။ Flexible Structure Type ဖြစ်တဲ့ အတွက် Type မတူတဲ့ Data တွေကို သိမ်းဆည်းနိုင်တယ်။ ဒါကြောင့် NoSQL ကို Unstructured Data, Dynamic Schema ဆိုပြီး မှတ်ထားလို့ရပါတယ်။
   
   Dynamic Schema ဖြစ်တဲ့ အတွက် RDBMS လို ကြိုတင်ပြီး Schema တွေ သတ်မှတ်ပေးထားစရာမလိုဘူး။ Performance , Speed , Scalability ကို ဦးစားပေးထားတယ်။ 
   
   NoSQL Database ကို အဓိကအားဖြင့် အမျိုးအစား (၄) မျိုးခွဲထားတယ်။ 
   
1. Document-oriented stores
      
      Document Stores ဆိုတဲ့ အတိုင်းပဲ Data ကို Document ထဲမှာ သိမ်းတာပေါ့။ ဘယ်လိုသိမ်းလဲဆိုရင် Collection နဲ့ သိမ်းတယ်။ Document တစ်ခုစီမှာ Nested Structure နဲ့ သိမ်းပါတယ်။ Schema မသတ်မှတ်ထားတဲ့အတွက် Data အစုံပါတယ်။ key-value pairs လည်းဖြစ်နိုင်တယ်။ key-array လည်းဖြစ်နိုင်တယ်။
      
      Example: MongoDB
            
```
{
   "_id": "12345",
   "name": "John Doe",
   "email": "john@example.com",
   "address": {
      "street": "123 Main St",
      "city": "New York"
   }
}
```
      
2. Key-value stores
      
      
3. Graph stores
4. Column-family Stores

   
   
   
   

