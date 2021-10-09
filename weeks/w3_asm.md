# Group-3 Week-3 Assignment

***10 marks***

အောက်ဖော်ပြပါ steps များအားလုံးပါဝင်အောင် Shell script **တစ်ခု**ရေးပါ။

#### Step-1

script ထဲမှာ ကိုယ့်ရဲ့ roll no:, email ကို echo တစ်ကြောင်းစီ ထုတ်ပါ။ (roll မှားလျှင် အမှတ်လုံးဝမရပါ)

[Roll no: မသေချာ/မမှတ်မိလျှင် ဒီကိုနှိပ်ပြီး ပြန်သွားကြည့်နိုင်ပါတယ်](https://docs.google.com/spreadsheets/d/1oojbslhBZQO4KZHZF_ZibkfDr4OHvBQsy5_F62yJfFk/edit?usp=sharing)

#### Step-2

user ဆီကနေ filename input တောင်းပါ (input တောင်းတဲ့အခါ 'enter ...' စတဲ့ echo များ ထုတ်ပြရန်မလိုပါ။)

#### Step-3

Step-2 မှာ တောင်းခဲ့တဲ့ filename ကို while loop သုံးပြီး ဖတ်ပါ။

file ထဲမှာ ဒါမျိုး data ရှိပါလိမ့်မယ်

```
lower:HeLLo LogixOwl
upper:mingaLar PaR
origin:My name is Owl
lower:I DON'T LIKE ZEE THEE

```
***နမူနာပြထားခြင်းသာဖြစ်ပါသည်***
 
file ထဲမှာက line အရေအတွက်က ရှိချင်သလောက် ရှိပါမည်

line တစ်ကြောင်းစီမှာ ```:``` ခြားထားတဲ့ string data နှစ်မျိုးရှိပါတယ်။

ဘယ်ဘက်အခြမ်းက string က လုပ်ရမယ့် ခေါင်းစဥ်ဖြစ်ပါတယ်

ညာဘက်အခြမ်းက string က data ဖြစ်ပါတယ်

### လုပ်ရမယ့်ခေါင်းစဥ်

> ဘယ်ဘက် အခြမ်းမှာ lower လို့တွေ့ရင် ညာဘက်အခြမ်းက string data ကို lower case (စာလုံးအသေး) ပြောင်းပြီး ထုတ်ပါ

> ဘယ်ဘက် အခြမ်းမှာ upper လို့တွေ့ရင် ညာဘက်အခြမ်းက string data ကို upper case (စာလုံးအကြီး) ပြောင်းပြီး ထုတ်ပါ

> ဘယ်ဘက် အခြမ်းမှာ origin လို့တွေ့ရင် ညာဘက်အခြမ်းက string data ကို ဒီတိုင်းပြန်ထုတ်ပါ

> အောက်မှာ ဥပမာပြပေးထားပါတယ်

<br>
<hr>
<br>

### Sample file data တွေနဲ့ ထုတ်ပေးရမယ့် sample outputs တွေကတော့

#### ဥပမာ (၁)
##### Sample file (filename = myfile1)
```
lower:HeLLo LogixOwl
upper:mingaLar PaR
origin:My name is Owl
lower:I DON'T LIKE ZEE THEE

```
##### Sample output:
```
Roll: g3u001
Email: mgmg@gmail.com
myfile1
hello logixowl
MINGALAR PAR
My name is Owl
i don't like zee thee
```

<hr>

#### ဥပမာ (၂)
##### Sample file (filename = myfile3)
```
origin:This is a TesTinG
lower:this SHOULD be In Lower String

```
##### Sample output:
```
Roll: g3u001
Email: mgmg@gmail.com
myfile3
This is a TesTinG
this should be in lower string
```

<hr>

#### ဥပမာ (၃)
##### Sample file (filename = myfile2)
```
upper:A quiz brown fox Jumps over the lazY doG
upper:Bite Sar tl
upper:london bridge is fallINg down

```
##### Sample output:
```
Roll: g3u001
Email: mgmg@gmail.com
myfile2
A QUIZ BROWN FOX JUMPS OVER THE LAZZY DOG
BITE SAR TL
LONDON BRIDGE IS FALLING DOWN
```

<hr>
<br>

### ရှင်းလင်းချက်

> input တောင်းလိုက်တဲ့ filename သည် ကျွန်တော်ထည့်ချင်တဲ့ file ကို ထည့်မှာဖြစ်ပါတယ်။ (ကိုယ်စမ်းကြည့်ဖို့ဆိုရင်လည်း နှစ်သက်ရာ file တစ်ခု တည်ဆောက်ပြီး input ထည့် စမ်းကြည့်နိုင်ပါတယ်)

> ထည့်လိုက်တဲ့ filename အပေါ်မူတည်ပြီး output တွေက တူညီမှာမဟုတ်ပါဘူး (အပေါ်မှာ ဥပမာ ၃ ခုပြထားပါတယ်)

> ကိုယ့်ရဲ့ စက်မှာ စမ်းကြည့်ဖို့ဆိုရင် file ရဲ့ နောက်ဆုံးမှာ new line တစ်ကြောင်းပိုဆင်းပေးထားဖို့လိုပါတယ်။ (ဥပမာပြထားတဲ့ sample file တွေကို ကြည့်ပါ)

> Asm တင်တဲ့အခါမှာတော့ shell file တစ်ခုတည်းသာတင်ပေးရပါမယ်။

> Sample output သည် နမူနာထုတ်ပြထားခြင်းဖြစ်ပါသည်။ [Roll: မိမိ၏ roll no:] စသည်ဖြင့် ကိုယ့်ရဲ့ roll, email တွေကို အစားထိုးထည့်သွားရမှာဖြစ်ပါတယ်။

<br>
<hr>
<br>

### စည်းကမ်းချက်

1. File name ကို asm3_g3u001.sh (g3u001 နေရာမှာ ကိုယ့်ရဲ့ roll no ဖြစ်ရပါမည်) ဟုပေးရမည်
2. File ကို submit လုပ်တဲ့အခါမှာ .sh ဖြင့်ဆုံးသော shell file သာဖြစ်ရပါမည်။ (Screenshot များ၊ zip file များ၊ docs file များ၊ အစရှိသော shell file မဟုတ်သည့် တခြား file များပေးပို့လျှင် အမှတ်လုံးဝ ရရှိမည်မဟုတ်ပါ)
3. Sample output မှာ ပြထားတဲ့အတိုင်း output လိုထွက်ရပါမည်။ လိုအပ်တဲ့ output များကို တိတိကျကျ ထုတ်ပေးဖို့ အရေးကြီးပါတယ်။(ဥပမာ - ကိုယ့်ရဲ့ roll, email) မလိုအပ်တဲ့ output များ၊ output အပိုများ၊ ထွက်လို့ မရပါ။ ထွက်လျှင် အမှတ်ရမည်မဟုတ်ပါ
သတ်မှတ်ချိန်အတွင်း အမှီတင်ပေးနိုင်ရပါမည်
4. Step ၃ ခုမှာပြောထားတဲ့ စည်းကမ်းချက်တွေနဲ့ကိုက်ညီပြီး မလိုအပ်တာများ echo ထုတ်မပေးရပါ

Assignment တင်ရန် Link

[https://forms.gle/JHEpprZJj5Uoonv98](https://forms.gle/JHEpprZJj5Uoonv98)

