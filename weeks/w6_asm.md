# Group-3 Week-6 Assignment

***10 marks***

အောက်ဖော်ပြပါ steps များအားလုံးပါဝင်အောင် Shell script **တစ်ခု**ရေးပါ။

*အဆုံးထိသေချာဖတ်ပါ။ Hint ပေးထားပါသည်*

### Step-1

script ထဲမှာ ကိုယ့်ရဲ့ roll no:, email ကို echo တစ်ကြောင်းစီ ထုတ်ပါ။ (roll မှားလျှင် အမှတ်လုံးဝမရပါ)

[Roll no: မသေချာ/မမှတ်မိလျှင် ဒီကိုနှိပ်ပြီး ပြန်သွားကြည့်နိုင်ပါတယ်](https://docs.google.com/spreadsheets/d/1oojbslhBZQO4KZHZF_ZibkfDr4OHvBQsy5_F62yJfFk/edit?usp=sharing)

### Step-2

ပထမဆုံးအနေနဲ့ filename တစ်ခုကို input တောင်းရပါမယ်

ထည့်လိုက်တဲ့ filename သည် exist ဖြစ်ပြီးတော့ directory မဟုတ်ရပါဘူး။ မရှိရင် ဖြစ်ဖြစ်၊ directory ဖြစ်နေရင်ဖြစ်ဖြစ် ```No such file``` လို့ output ထုတ်ပေးပြီး ဘာမှဆက်လုပ်ရန်မလိုပါ။

ရှိတယ်၊ file လဲဖြစ်တယ်ဆိုရင်တော့ user action ကို input ဆက်တောင်းရပါမယ်

***(အားလုံးကို တစ်ခါပဲတောင်းရမှာဖြစ်ပါတယ် select loop လို loop ပတ်ပြီးထပ်ခါထပ်ခါ မတောင်းရပါ)***

Step-2 အထိ sample input, output က ဒီလိုဖြစ်ပါမယ်

##### တကယ်လို့ file ရှိရင်
```
Roll: g3u001
Email: mgmg@gmail.com
filename? file1.txt
action? roll
...(step-3 ကို ဆက်လုပ်ရန်)...
```
##### တကယ်လို့ file မရှိရင်
```
Roll: g3u001
Email: mgmg@gmail.com
filename? mydata.txt
No such file
```

### Step-3

Step-2 မှာတောင်းလိုက်တဲ့ user action က ဖြစ်နိုင်ချေ နှစ်မျိုးပဲရှိပါမယ်။ ```roll``` နဲ့ ```phone``` ပါ။

#### action က ```roll``` ဆိုရင်

ပထမဆုံးတောင်းခဲ့တဲ့ filename ကနေပြီးတော့ roll no တွေကို ဆွဲထုတ်ရပါမယ် (roll no သက်သက်ပဲဆွဲထုတ်ရပါမယ်၊ တစ်ကြောင်းလုံး ထုတ်မပေးရပါ)

file ထဲမှာ ရှိနေမယ့် roll no format က ဒီလိုမျိုးဖြစ်ပါမယ်။

```
G3U001
```
* ပထမဆုံးစာလုံးသည် G ဖြစ်ပါတယ် (case-sensitive ပါ၊ အကြီးဖြစ်ရပါမယ်)
* G နောက်မှာ ကပ်လိုက်တာကတော့ နံပါတ်တစ်ခုဖြစ်ပါတယ်။ digit တစ်လုံးမကလဲ ဖြစ်နိုင်ပါတယ်။ 
ဥပမာ - G1U001, G17U003, G109U077
* နံပါတ်နောက်မှာတော့ U အကြီးလိုက်ပါတယ်
* နောက်ဆုံးမှာတော့ digit 3 လုံးတိတိ ဖြစ်ရပါမယ်

* roll နံပါသည် line တစ်ခုရဲ့အစ (သို့မဟုတ်) word တစ်ခုရဲ့အစမှာ ရှိချင်မှရှိပါမည်။
ဥပမာ - ```MyrollisG3U001SoWhat?``` ဆိုရင် ```G3U001``` ကို ပဲ ဆွဲထုတ်ပေးရပါမယ်
* line တစ်ကြောင်းထဲမှာ roll ၂ ခု ၃ ခု ရှိနေခဲ့ရင်လည်း အားလုံးကို ထုတ်ပေးရပါမယ်။ (format နဲ့မကိုက်ရင်တော့ မထုတ်ပေးရပါ)

ဥပမာ - 
```
hello aG3U001G111U12345blah.
hi GU01G99U008soesoe g3U001.
```

အပေါ်က line နှစ်ကြောင်းမှာဆိုရင် ထွက်ရမယ့် roll no တွေက
```
G3U001
G111U123
G99U008
```
ဖြစ်ပါတယ်

ထိုအထဲမှ ```GU01```, ```g2U001``` တို့သည် rule နဲ့ ကွဲနေတဲ့အတွက် match မဖြစ်ပါဘူး

#### action က ```phone``` ဆိုရင်

ပထမဆုံးတောင်းခဲ့တဲ့ filename ကနေပြီးတော့ phone no: တွေကို ဆွဲထုတ်ရပါမယ် (phone no: သက်သက်ပဲဆွဲထုတ်ရပါမယ်၊ တစ်ကြောင်းလုံး ထုတ်မပေးရပါ)

file ထဲမှာ ဖြစ်နိုင်ချေရှိတဲ့ phone no: တွေကတော့

* +xxx-xxx-xxxxxx
* +xxx xxx xxxxxx
* +xxxxxxxxxxxx
* +xxx-xxx-xxxx
* +xxx xxx xxxx
* +xxxxxxxxxx
* xx-xxx-xxxxxx
* xx xxx xxxxxx
* xxxxxxxxxxx
* xx-xxx-xxxx
* xx xxx xxxx
* xxxxxxxxx

အနှစ်ချုပ် phone no: တွေအတွက် format ကတော့

* ```+xxx``` နဲ့ စနိုင်သလို ```xx``` နဲ့လဲစနိုင်ပါတယ် (x တွေသည် digit တစ်လုံးချင်းစီကို ကိုယ်စားပြုပါသည်)
* ပြီးရင် ကြားထဲမှာ space (``` ```) ဒါမှမဟုတ် hyphen (```-```) **(တစ်ခု)** ခု ရှိနိုင်သလို ဘာမှမရှိတာလဲဖြစ်နိုင်ပါတယ်
* ပြီးရင်တော့ digit ၃ လုံးတိတိလိုက်ပါတယ်
* ပြီးရင်ရှေ့ကလိုပဲ ကြားထဲမှာ space (``` ```) ဒါမှမဟုတ် hyphen (```-```) **(တစ်ခု)**ခု ရှိနိုင်သလို ဘာမှမရှိတာလဲဖြစ်နိုင်ပါတယ်
* နောက်ဆုံးမှာတော့ digit ၄ လုံးကနေ ၆ လုံးအထိရှိနိုင်ပါတယ်

ဒီ format or rule တွေနဲ့ကိုက်တဲ့ phone no: တွေကိုသာထုတ်ပေးရမှာဖြစ်ပါတယ်။ ***(မြန်မာနိုင်ငံမှာ အသုံးများတဲ့ phone no: ပုံစံကိုသာ ယူပြထားချင်းဖြစ်ပါသည်)***

Roll no: တွေတုန်းကလိုပဲ match ဖြစ်တဲ့ phone no: တွေကို(သာ) ထုတ်ပြပေးရမှာပါ


##### Example file: file1.txt

```
hello aG3U001G111U12345 phoneno is +959 888 814411
hi GU01G99U008s g3U001.
Here is another phone no pattern, 09888814411
Also, 09-888-814411.
is that your phone? +959-234-5678? ok ok got it.
these are not valid phones for this assignment, +9-934-91111, 09-88-881441, 09-888-123, 09-888-814-411
```

##### Example 1
```
Roll: g3u001
Email: mgmg@gmail.com
filename? mydir
No such file
```

##### Example 2
```
Roll: g3u001
Email: mgmg@gmail.com
filename? file1.txt
action? roll
G3U001
G111U123
G99U008
```

##### Example 3
```
Roll: g3u001
Email: mgmg@gmail.com
filename? file1.txt
action? phone
+959 888 814411
09888814411
09-888-814411
+959-234-5678
```

### ရှင်းလင်းချက်

> ရှင်းလင်းချက်များများစားစားမပြောတော့ပါဘူး Step-3 မှာ ပြည့်ပြည့်စုံစုံရှင်းပြပေးထားပါတယ်

> Asm တင်တဲ့အခါမှာတော့ shell file တစ်ခုတည်းသာတင်ပေးရပါမယ်။

### Hint

```sh
grep -oE '(\+[0-9]{3}|[0-9]{2})[\ \-]?...'
# phone no ကို ထုတ်တဲ့နေရာမှာ ပထမပိုင်းအနေနဲ့ +xxx (သို့မဟုတ်) xx နှစ်မျိုးထဲကတစ်ခုသာဖြစ်အောင်စစ်ဖို့
# အပေါ်က ပုံစံကိုအသုံးပြုနိုင်ပါတယ်
```

<br>
<hr>
<br>

### စည်းကမ်းချက်

1. File name ကို asm6_g3u001.sh (g3u001 နေရာမှာ ကိုယ့်ရဲ့ roll no ဖြစ်ရပါမည်) ဟုပေးရမည်
2. 2. File ကို submit လုပ်တဲ့အခါမှာ .sh ဖြင့်ဆုံးသော shell file သာဖြစ်ရပါမည်။ (Screenshot များ၊ zip file များ၊ docs file များ၊ အစရှိသော shell file မဟုတ်သည့် တခြား file များပေးပို့လျှင် အမှတ်လုံးဝ ရရှိမည်မဟုတ်ပါ)
3. 3. Sample output မှာ ပြထားတဲ့အတိုင်း output လိုထွက်ရပါမည်။ လိုအပ်တဲ့ output များကို တိတိကျကျ ထုတ်ပေးဖို့ အရေးကြီးပါတယ်။(ဥပမာ - ကိုယ့်ရဲ့ roll, email) မလိုအပ်တဲ့ output များ၊ output အပိုများ၊ ထွက်လို့ မရပါ။ ထွက်လျှင် အမှတ်ရမည်မဟုတ်ပါ
4. သတ်မှတ်ချိန်အတွင်း အမှီတင်ပေးနိုင်ရပါမည်
5. 4. Step ၃ ခုမှာပြောထားတဲ့ စည်းကမ်းချက်တွေနဲ့ကိုက်ညီပြီး မလိုအပ်တာများ echo ထုတ်မပေးရပါ
Assignment တင်ရန် Link


[https://forms.gle/cW2aupeKhPnZvgYJA](https://forms.gle/cW2aupeKhPnZvgYJA)

