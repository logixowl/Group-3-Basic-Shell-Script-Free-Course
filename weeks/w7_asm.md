# Group-3 Week-7 Assignment

***10 marks***

အောက်ဖော်ပြပါ steps များအားလုံးပါဝင်အောင် Shell script **တစ်ခု**ရေးပါ။

### Step-1

script ထဲမှာ ကိုယ့်ရဲ့ roll no:, email ကို echo တစ်ကြောင်းစီ ထုတ်ပါ။ (roll မှားလျှင် အမှတ်လုံးဝမရပါ)

[Roll no: မသေချာ/မမှတ်မိလျှင် ဒီကိုနှိပ်ပြီး ပြန်သွားကြည့်နိုင်ပါတယ်](https://docs.google.com/spreadsheets/d/1oojbslhBZQO4KZHZF_ZibkfDr4OHvBQsy5_F62yJfFk/edit?usp=sharing)

### Step-2

Python auto-grader shell file တစ်ခုရေးပါ။ သူ့ကို run တဲ့အခါမှာ options သုံးခု ထည့်ပေးရပါမယ်။

* -p > python file
* -i > sample input file
* -o > sample output file

[ကျွန်တော့်ရဲ့ python auto-grader video part-1](https://www.facebook.com/logixowl/videos/242329804398454/) ကြည့်ထားတယ်ဆိုရင် အဲ့ဒီအတိုင်းရေးနိုင်ပါတယ်၊ ဒါကြောင့်မို့ မေးခွန်းကို အစအဆုံးရှင်းမပြတော့ပါဘူး။ (ဒီ asm မှာတော့ part-1 ကိုပဲ လုပ်သွားရမှာပါ)

Output လေးတွေကိုတော့ ဒါမျိုးထုတ်ပေးပါ

* program က success ဖြစ်ရင် ```correct```
* sample output နဲ့မတူရင် ```wrong```
* run တဲ့အခါမှာ error တက်ရင် ```error```

ဒီမှာကတော့ စစ်တဲ့နေရာမှာ နဲနဲကပြောင်းအလွဲရှိပါမယ်

* empty lines တွေ ကို ignore လုပ်ရပါမယ်
* case sensitive မဖြစ်ရပါဘူး၊ အကြီးဖြစ်ဖြစ်အသေးဖြစ်ဖြစ် တူရင် correct ပါ
* line အဆုံးမှာ ပါတတ်တဲ့ space တွေကို ignore လုပ်ပါ

***Assignment တင်တဲ့အခါမှာ shell file တစ်ခုတည်းကိုသာ တင်ပေးရမှာပါ ကျန်တဲ့ input, output files တွေက ထည့်ပေးစရာမလိုပါ***

##### Sample input, output (1)

```
$ ./asm7_g3u001.sh -p hello.py -i input1.txt -o output1.txt
Roll: G3U001
Email: mgmg@gmail.com
success
```
##### Sample input, output (2)

```
$ ./asm7_g3u001.sh -o output3.py -i input3.txt -p program3.py
Roll: G3U001
Email: mgmg@gmail.com
wrong
```
##### Sample input, output (3)

```
$ ./asm7_g3u001.sh -p program4.py -i input4.txt -o output4.txt
Roll: G3U001
Email: mgmg@gmail.com
error
```

<br>
<hr>
<br>

### စည်းကမ်းချက်

1. File name ကို asm7_g3u001.sh (g3u001 နေရာမှာ ကိုယ့်ရဲ့ roll no ဖြစ်ရပါမည်) ဟုပေးရမည်
2. 2. File ကို submit လုပ်တဲ့အခါမှာ .sh ဖြင့်ဆုံးသော shell file သာဖြစ်ရပါမည်။ (Screenshot များ၊ zip file များ၊ docs file များ၊ အစရှိသော shell file မဟုတ်သည့် တခြား file များပေးပို့လျှင် အမှတ်လုံးဝ ရရှိမည်မဟုတ်ပါ)
3. 3. Sample output မှာ ပြထားတဲ့အတိုင်း output လိုထွက်ရပါမည်။ လိုအပ်တဲ့ output များကို တိတိကျကျ ထုတ်ပေးဖို့ အရေးကြီးပါတယ်။(ဥပမာ - ကိုယ့်ရဲ့ roll, email) မလိုအပ်တဲ့ output များ၊ output အပိုများ၊ ထွက်လို့ မရပါ။ ထွက်လျှင် အမှတ်ရမည်မဟုတ်ပါ
4. သတ်မှတ်ချိန်အတွင်း အမှီတင်ပေးနိုင်ရပါမည်
5. 4. Step ၃ ခုမှာပြောထားတဲ့ စည်းကမ်းချက်တွေနဲ့ကိုက်ညီပြီး မလိုအပ်တာများ echo ထုတ်မပေးရပါ
Assignment တင်ရန် Link

[https://forms.gle/xZFgGWzuoUYbGc327](https://forms.gle/xZFgGWzuoUYbGc327)


