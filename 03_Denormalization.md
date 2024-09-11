
Content
1. What is Denormalization?
2. Conclusion
   
------------------------------------------------------------------------

1. What is Denormalization?
   
   Denormalization ဆိုတာက Normalization ရဲ့ ပြောင်းပြန်ပေါ့။ Normalization က Redundant Column တွေကို ခွဲထုတ်တယ်။ Denormalization ကတော့ ပြန်ပေါင်းထည့်တယ်။ 
   
   သူ့ကို Database Optimization Technique လို့လည်း ခေါ်ကြတယ်။ Data တွေကို Normalization လုပ်တာက အဆင်ပြေပေမယ့် ပြသာနာက Data တစ်ခုကို လိုချင်လို့ Table ပေါင်းစုံကနေ data ပတ်ယူရတာမျိုးဖြစ်တတ်တယ်။ 
   
   Denormalization မှာကျတော့ table တစ်ခုထဲမှာပဲ လိုချင်တဲ့ Data တွေ အကုန်ယူလို့ရနိုင်တယ်။ ဒါကြောင့် Query ဆွဲတဲ့ နေရာမှာလည်း ပိုပြီးမြန်ဆန်တယ်။
   
   ဥပမာလေး တစ်ချက်ကြည့်ရအောင်။
   
   ![Denormalization](images/Denormalization.png)

   Customer Orders တစ်ခုရဖို့ ကျွန်တော်တို့ table 4 ခုလောက် ပတ်ယူနေစရာမလိုတော့ပါဘူး။ ဒါကြောင့် Query Performance ကတော့ Normalization နဲ့ ယှဥ်ရင် မြန်ဆန်နေတာ တွေ့ရမှာပါ။ 

------------------------------------------------------------------------
2. Conclusion

   Normalization နဲ့ Denormalization တွေက Data Modeling Concepts တွေဖြစ်ကြတာမို့လို့ ကျွန်တော်တို့ သုံးမယ့် Project / Software နဲ့ ဘယ်လို Database သုံးမလဲ အပေါ်မူတည်ပြီး ရွေးချယ်သုံးရမှာပဲ ဖြစ်ပါတယ်။

------------------------------------------------------------------------