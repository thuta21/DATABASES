
Content

1. What is Database?
2. What is Query?
3. What is Schema?

------------------------------------------------------------------------

1. What is Database?
   
   Database အကြောင်းမစခင် Data ဆိုတာကို အရင်ပြောမှဖြစ်မှာပေါ့။ အချက်အလက်ကောက်ယူလို့ရသမျှ ကို Data လို့ခေါ်တယ်။ ဥပမာ နာမည် ၊ အသက် ၊ ဓါတ်ပုံ ၊ Company နာမည်၊ ရာသီဥတု စသည်ဖြင့်ပေါ့။
   
   ဒါဆို Database ကိုဆက်လို့ရပြီ။ Database ဆိုတာ အပေါ်က ပြောထားတဲ့ Data တွေကို စုထားတဲ့ Collection တစ်ခုပါ။ "**Digital File Cabinet**" တစ်ခုလို့ ဆိုနိုင်ပါတယ်။ 
   
   ဥပမာ Library Database တစ်ခုရှိတယ်ဆိုပါစို့။ ဒါဆို Database ထဲမှာ စာအုပ်နာမည်တွေရှိမယ်။ စာအုပ်အမျိုးအစားတွေ ကို Category အလိုက်ခွဲပြီးရှိမယ်။ စာအုပ်တွေကိုရေးတဲ့ စာရေးဆရာ နဲ့ ပတ်သတ်တဲ့ အချက်အလက်တွေရှိမယ်။ ထုတ်ဝေခဲ့တဲ့ နှစ် ရှိမယ်။ ဘယ်သူတွေငှားသွားလဲ ဆိုတဲ့ User ( အသုံးပြုသူ ) စာရင်းရှိမယ်။ ဘယ်စာအုပ်တွေ ကတော့ Available ဖြစ်အုံးမလဲဆိုတဲ့ စာရင်းတွေရှိမယ်။ ဒါဆို Database ဆိုတာတော့ အကြမ်းဖျင်းနားလည်မယ်ထင်တယ်။ 
   
   ဒါ့အပြင် ကျွန်တော်တို့ Excel တို့ စာအုပ်မှာ ဘောပင်နဲ့ မှတ်တဲ့ အကြွေးစာရင်းတို့ ဝင်ငွေ / ထွက်ငွေတို့ ဆိုတာကလည်း Database လို့ မြင်ကြည့်လို့ရပါသေးတယ်။
   
   ဆိုတော့ ကျွန်တော်တို့ သိမ်းတယ်ဆိုမှတော့ လိုအပ်ရင် ပြန်ကြည့်မယ် ၊ ပြန်သုံးမယ် ၊​ မှားရင် ပြန်ပြင်မယ်။ မလိုတော့ရင် ဖျက်ပစ်လိုက်ပြီး လိုအပ်ရင် အသစ်ထပ်ထည့်မယ်။ ဒါက Database ကိုသုံးရခြင်းရဲ့ ရည်ရွယ်ချက်ပါ။
   
   ဒီလို Data manipulation လုပ်ဖို့ဆို DBMS ကို သုံးရတော့မယ်။​ DBMS ရဲ့ အရှည်ကောက်က Database Management System ဖြစ်ပြီး Data တွေကို စီမံဖို့ Tools ( Software ) တစ်ခုပါ။ 
   
   DBMS types တွေအနေနဲ့ အများကြီး ရှိပြီး အများကြီးကျယ်ပြန့်တယ်။ Message Brokers တို့ Multi model databases တို့လိုပေါ့။​ ကျွန်တော်ကတော့ လေ့လည်း လေ့လာရင်းဆိုတော့ လူသုံးများတဲ့ သိထားသင့်တဲ့ 
   
   (1) Relational Databases ( RDMS )
   (2) NoSQL တို့တွေကို တစ်ဆင့်ပြီး တစ်ဆင့် အနေနဲ့ အတူလေ့လာကြည့်ပါမယ်။ 

------------------------------------------------------------------------

2. What is Query?
   
   တခြားဟာတွေ မစခင်မှာ Common Terms တွေက တစ်ဆင့် စပါမယ်။ Query ဆိုတာက အပေါ်က Database ကို ဒါလုပ် ဒါလုပ်ဆိုပြီး သုံးလို့ရတဲ့ Command တစ်ခုပါ။​ ဆိုလိုတာက Query ကိုသုံးပြီး Data တွေ အသစ်ထည့်မယ် (Create)။ ဘာ Data လည်းဆိုပြီး ဖတ်ကြည့်လို့ရမယ် (Read)။ ပြင်ချင်လည်း ပြင်လို့ရမယ် (Update)။ ဒါမှမဟုတ်ဖျက်ချင်လည်း ဖျက်ချပစ်လို့ရမယ် (Delete)။ ဒီလိုမျိုး ( Create / Read / Update / Delete) လုပ်တာကို အတိုခေါက် ( CRUD ) ဆိုပြီး Term တစ်ခု ဖြစ်လာတယ်။ 
   
   ဒါ့အပြင် Data တွေကို အရှေ့အနောက် Sorting စီတာတို့၊ Data တွေကို စုပေါင်းပေးတာတို့ စသည်ဖြင့်လည်း သုံးလို့ရပါသေးတယ်။
   
------------------------------------------------------------------------

3. What is Schema?
   
   ဒါဆို Schema ကကော ဘာလဲ။ Schema ဆိုတာက Database ထဲမှာသိမ်းထားတဲ့ Data တွေရဲ့ Design တစ်ခု / Structure တစ််ခုလို့ မြင်ကြည့်လို့ရပါတယ်။ ဆိုလိုတာက အပေါ်မှာ ပြောခဲ့သလိုပဲ Database ကို Excel လို့သတ်မှတ်ရင် Schema ဆိုတာက Columns တွေလို့ မှတ်လို့ရပါတယ်။ ဥပမာ Json format တစ်ခုရှိတယ် ထားပါတော့။    
   
   ```
    {
		"name": "Thuta Min Thway",
		"age": "23",
		"gender": "MALE",
		"isSingle": false // 😜
	}
    ```
   
   ဒီ format မှာ " name, age, gender, isSingle " ဆိုတာတွေက Schema တွေပါ။ တစ်ခုရှိတာက တစ်ချို့ DBMS types တွေမှာ Schema မတူတာမျိုး ရှိတတ်ပါတယ်။
   
------------------------------------------------------------------------