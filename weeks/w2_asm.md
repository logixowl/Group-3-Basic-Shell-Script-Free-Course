# Group-3 Week-2 Assignment

***10 marks***

အောက်ဖော်ပြပါ steps များအားလုံးပါဝင်အောင် Shell script **တစ်ခု**ရေးပါ။

#### Step-1

script ထဲမှာ ကိုယ့်ရဲ့ roll no:, email ကို echo တစ်ကြောင်းစီ ထုတ်ပါ။ (roll မှားလျှင် အမှတ်လုံးဝမရပါ)

[Roll no: မသေချာ/မမှတ်မိလျှင် ဒီကိုနှိပ်ပြီး ပြန်သွားကြည့်နိုင်ပါတယ်](https://docs.google.com/spreadsheets/d/1oojbslhBZQO4KZHZF_ZibkfDr4OHvBQsy5_F62yJfFk/edit?usp=sharing)

#### Step-2

လက်ရှိ dir ရဲ့ အောက်မှာ ```week2asm``` ဆိုတဲ့ file or dir တစ်ခု ရှိမရှိကို if condition သုံးပြီး စစ်ပါ။ ရှိလျှင် directory ဟုတ်မဟုတ်ဆက်ပြီး စစ်ဆေးပါ။ directory အနေနဲ့ရှိတယ်ဆိုရင် ```dir exist``` ဟုထုတ်ပါ၊ directory မဟုတ်ဘူးဆိုရင် ```file exist``` ဟုထုတ်ပါ။ (မရှိလျှင်ဘာမှမထုတ်ရပါ)

#### Step-3

(Step-2 မှာစစ်ခဲ့တဲ့ ```week2asm``` ဆိုတဲ့ file or dir ရှိမှ step-3 ကို အလုပ်လုပ်ရပါမယ်။ မရှိရင် ဘာမှ ဆက်လုပ်စရာမလိုပါ)

```week2asm``` ရဲ့ file permission က read နဲ့ write နှစ်ခုစလုံးရှိပြီး execute permission မရှိနေဘူးဆိုရင် ```ok``` ဟု echo ထုတ်ပါ။ (မဟုတ်လျှင်ဘာမှမထုတ်ရပါ)

> Step ၃ ခုစလုံးကို script file တစ်ခုတည်းတွင်ရေးရပါမည်။

<br>
<hr>
<br>

### ဖြစ်နိုင်ချေရှိတဲ့ sample outputs တွေကတော့

##### Sample output:
ဖြစ်နိုင်ချေ(၁): ```week2asm``` ရှိ၊ file အမျိုးအစားဖြစ်၊ permission က ```rw-```
```
Roll: g3u001
Email: mgmg@gmail.com
file exist
ok
```

##### Sample output:
ဖြစ်နိုင်ချေ(၂): ```week2asm``` ရှိ၊ dir အမျိုးအစားဖြစ်၊ permission က ```rwx```
```
Roll: g3u001
Email: mgmg@gmail.com
dir exist
```

##### Sample output:
ဖြစ်နိုင်ချေ(၃): ```week2asm``` မရှိ
```
Roll: g3u001
Email: mgmg@gmail.com
```

##### Sample output:
ဖြစ်နိုင်ချေ(၄): ```week2asm``` ရှိ၊ dir အမျိုးအစားဖြစ်၊ permission က ```rw-```
```
Roll: g3u001
Email: mgmg@gmail.com
dir exist
ok
```

##### Sample output:
ဖြစ်နိုင်ချေ(၅): ```week2asm``` ရှိ၊ file အမျိုးအစားဖြစ်၊ permission က ```r--```
```
Roll: g3u001
Email: mgmg@gmail.com
file exist
```

### ရှင်းလင်းချက်

> ```week2asm``` ဆိုတာ assignment ကိုစစ်ဆေးဖို့အတွက် ကျွန်တော်ကြိုတင်ဖန်တီးထားမည့် file or dir တစ်ခုဖြစ်ပါတယ်။ (ဖန်တီးမထားတာလဲ ဖြစ်နိုင်သလို permission တွေကို လဲ ပေးချင်သလို ပေးထားမှာပါ)

> ```week2asm``` ဆိုတဲ့ file or dir ရဲ့ ဖြစ်နိုင်ချေရှိတဲ့ အခြေနေတွေပေါ်မူတည်ပြီး sample output ၅ မျိုးထုတ်ပြပေးထားတာဖြစ်လို့ ၅ ခုစလုံး ထုတ်ပေးရန်မလိုပါ။ ```week2asm``` ရဲ့ အခြေနေပေါ်မူတည်ပြီး သက်ဆိုင်တဲ့ output ကိုသာထုတ်ပေးရမှာဖြစ်ပါတယ်

> ကိုယ့်ရဲ့ စက်မှာ စမ်းကြည့်ဖို့ဆိုရင် ```week2asm``` ဆိုတဲ့ dir (သို့မဟုတ်) file ကို ဖန်တီးပြီး permission တွေ ပေးကြည့်ကာ စမ်းသက်နိုင်ပါသည်

> Asm တင်တဲ့အခါမှာတော့ shell file တစ်ခုတည်းသာတင်ပေးရပါမယ်။ (```week2asm``` ကို တင်ပေးရန် လုံးဝမလိုပါ)

> Sample output သည် နမူနာထုတ်ပြထားခြင်းဖြစ်ပါသည်။ [Roll: မိမိ၏ roll no:] စသည်ဖြင့် ကိုယ့်ရဲ့ roll, email တွေကို အစားထိုးထည့်သွားရမှာဖြစ်ပါတယ်။

<br>
<hr>
<br>

### စည်းကမ်းချက်

1. File name ကို asm2_g3u001.sh (g3u001 နေရာမှာ ကိုယ့်ရဲ့ roll no ဖြစ်ရပါမည်) ဟုပေးရမည်
2. File ကို submit လုပ်တဲ့အခါမှာ .sh ဖြင့်ဆုံးသော shell file သာဖြစ်ရပါမည်။ (Screenshot များ၊ zip file များ၊ docs file များ၊ အစရှိသော shell file မဟုတ်သည့် တခြား file များပေးပို့လျှင် အမှတ်လုံးဝ ရရှိမည်မဟုတ်ပါ)
3. Sample output မှာ ပြထားတဲ့အတိုင်း output လိုထွက်ရပါမည်။ လိုအပ်တဲ့ output များကို တိတိကျကျ ထုတ်ပေးဖို့ အရေးကြီးပါတယ်။(ဥပမာ - ကိုယ့်ရဲ့ roll, email) မလိုအပ်တဲ့ output များ၊ output အပိုများ၊ ထွက်လို့ မရပါ။ ထွက်လျှင် အမှတ်ရမည်မဟုတ်ပါ
သတ်မှတ်ချိန်အတွင်း အမှီတင်ပေးနိုင်ရပါမည်
4. Step ၃ ခုမှာပြောထားတဲ့ စည်းကမ်းချက်တွေနဲ့ကိုက်ညီပြီး မလိုအပ်တာများ echo ထုတ်မပေးရပါ

Assignment တင်ရန် Link
[https://forms.gle/T1QtJCUkfahp4FTo6](https://forms.gle/T1QtJCUkfahp4FTo6)

