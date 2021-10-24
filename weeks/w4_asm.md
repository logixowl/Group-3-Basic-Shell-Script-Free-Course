# Group-3 Week-4 Assignment

***20 marks***

အောက်ဖော်ပြပါ steps များအားလုံးပါဝင်အောင် Shell script **တစ်ခု**ရေးပါ။

### Step-1

script ထဲမှာ ကိုယ့်ရဲ့ roll no:, email ကို echo တစ်ကြောင်းစီ ထုတ်ပါ။ (roll မှားလျှင် အမှတ်လုံးဝမရပါ)

[Roll no: မသေချာ/မမှတ်မိလျှင် ဒီကိုနှိပ်ပြီး ပြန်သွားကြည့်နိုင်ပါတယ်](https://docs.google.com/spreadsheets/d/1oojbslhBZQO4KZHZF_ZibkfDr4OHvBQsy5_F62yJfFk/edit?usp=sharing)

### Step-2

select loop ကို သုံးပြီးတော့ menu တစ်ခု ဖန်တီးပါ။ ပါဝင်ရမယ့် menu တွေကတော့

1) Create file or dir
2) Delete file or dir
3) List all files and dirs
4) List all executable files
5) Change permissions
6) Exit

user ရွေးလိုက်တဲ့ နံပါတ်ကိုမူတည်ပြီးတော့ လုပ်ဆောင်ရမယ့် တာဝန်တွေ ကွဲပြားသွားပါမယ်။ တစ်ခုချင်းစီရဲ့ အသေးစိတ်ကို Step-3 မှာ ဖော်ပြပေးသွားပါမယ်

### Step-3

Step-2 မှာရှိတဲ့ menu တစ်ခုချင်းစီရဲ့ အဓိကလုပ်ဆောင်ရမှာတွေကတော့

#### 1. Create file or dir

user က 1 ကိုရွေးခြယ်လိုက်ပြီဆိုတာနဲ့ user ဆီကနေ input နှစ်ခု တောင်းပါမယ် ပထမတစ်ခုကတော့ file or dir ရဲ့ name ပါ။ ဒုတိယတစ်ခုကတော့ file လား dir လားဆိုတာကို မေးမှာပါ။ ပြီးတာနဲ့ သူရွေးလိုက်တဲ့ အပေါ်မူတည်ပြီး f ဆိုရင် file create လုပ်၊ d ဆိုရင်တော့ directory create လုပ်ရပါမယ်။


##### Example output 1

```
1) Create file or dir
2) Delete file or dir
3) List all files and dirs
4) List all executable files
5) Change permissions
6) Exit
#? 1
name? test1
file or dir? f
Created file test1
#? 
```
ဒီမှာဆိုရင်  file or dir ရဲ့ name တောင်းပြီးရင် file or dir ရွေးရတဲ့နေရာမှာ user အနေနဲ့ f ဒါမှမဟုတ် d ရွေးပေးရပါမယ်

f ဆိုတာ file ကိုကိုယ်စားပြုပြီး d ကတော့ dir ကို ကိုယ်စားပြုပါတယ် (တခြား outputs အပိုများ လုံးဝ မထုတ်ပေးရပါ)

> Tip: Shell script ထဲမှာ linux command တွေကို ဒီတိုင်းသုံးလို့ရပါတယ်။ ဥပမာ၊

```sh
#!/bin/bash

filename="hello.txt"
mkdir movies
touch "$filename"
rm -rf "$filename"
```
(ဥပမာ ပြထားခြင်းသာဖြစ်ပါသည်)


#### 2 Delete file or dir

ဒီမှာဆိုရင် user က ဖျက်ချင်တဲ့ file or dir name ကို input တောင်းပြီး ဖျက်ပေးရမှာပါ။ ဒီမှာကတော့ file လား dir လား မတောင်းရပါ။ သူထည့်လိုက်တဲ့ name ကို file ဖြစ်ဖြစ် dir ဖြစ်ဖြစ် ဖျက်ပေးရမှာပါ။

ဒီမှာ သတိထားစရာ တစ်ခုက user က ဖျက်ဖို့ထည့်ပေးလိုက်တဲ့ name ကို ရှိမရှိအရင်စစ်ပေးရပါမယ်၊ မရှိဘူးဆိုရင် example မှာ ပြထားတဲ့အတိုင်း ```No file or dir``` ဟုထုတ်ပေးရပါမယ်။ ရှိတယ်ဆိုရင် file or dir ကို ဖျက်ပေးရပါမယ်။

ဖျက်ပြီးတဲ့အခါမှာ file ဆိုရင် ```Deleted file (name)``` ဟုလည်းကောင်း၊ dir ဆိုရင် ```Deleted directory (name)``` ဟုလည်းကောင်း၊ output ပြန်ထုတ်ပေးရပါမယ်။ Example ကိုကြည့်ပါ

##### Example output 2
```
1) Create file or dir
2) Delete file or dir
3) List all files and dirs
4) List all executable files
5) Change permissions
6) Exit
#? 2
name? test1
Deleted file test1
#? 2
name? programs
Deleted directory programs
#? 2
name? blahblah
No file or dir
#? 
```
(တခြား output အပိုများ မထုတ်ရပါ)


#### 3 List all files and dirs

ဒါကတော့ ရှင်းပါတယ် လက်ရှိ dir အောက်မှာ ရှိနေတဲ့ file တွေ dir တွေ အကုန်လုံးထုတ်ပြပေးရပါမယ်။ ထူးခြားချက်အနေနဲ့ ထုတ်ပြတဲ့အခါ name တွေရဲ့ရှေ့မှာ နံပါတ်စဉ်တပ်ပြီး file ဆိုရင် ```f```, dir ဆိုရင် ```d``` ဆိုပြီး ထုတ်ပြပေးရပါမယ်။ Example ကိုကြည့်ပါ

##### Example output 3
```
1) Create file or dir
2) Delete file or dir
3) List all files and dirs
4) List all executable files
5) Change permissions
6) Exit
#? 3
1. f test1
2. f hello.txt
3. d programs
#? 
```
(file တွေ dir တွေက ဥပမာပြထားတဲ့ အစဉ်လိုက်မဟုတ်လဲရပါတယ်)

### 4 List all executable files

ဒါကတော့ if condition ကိုသုံးပြီး executable ရှိတဲ့ file တွေပဲ ထုတ်ပေးရမှာပါ (dir မပါ)

##### Example output 4
```
1) Create file or dir
2) Delete file or dir
3) List all files and dirs
4) List all executable files
5) Change permissions
6) Exit
#? 4
myprogram
run.sh
#? 2
name? myprogram
Deleted file myprogram
#? 2
name? run.sh
Deleted file run.sh
#? 4
#? 
```

(List ထုတ်ပြတဲ့ 3 ရော 4 မှာပါ file တွေ dir တွေမရှိရင် ဘာမှ ထုတ်မပေးရပါ)

ဒီ example မှာဆိုရင် ပထမကြည့်တုန်းက myprogram နဲ့ run.sh ဆိုတဲ့ executable ရှိတဲ့ file 2 ခုပြပေးပါတယ်။ ပြီးတော့ အဲ့နှစ်ခုကို ဖျက်လိုက်တဲ့အခါ ပြန်ထုတ်ကြည့်တော့ ဘာမှ မပြတော့ပါဘူး။


#### 5 Change permissions

ပထမဆုံး file or dir name တောင်းမယ် ပြီးရင် permission ပြောင်းဖို့လိုတဲ့ ရွေးစရာလေးတွေပြပေးပါမယ်။ ရွေးလိုက်တဲ့အတိုင်း file or dir ကို permission ပြောင်းပေးရပါမယ်။

မှတ်ချက်။ file or dir က မရှိရင် ```No file or dir``` ဟု ထုတ်ပြပြီး permission ပြောင်းပေးရန်မလိုပါ။

(Permission ပြောင်းတဲ့အခါ users တိုင်းကိုပြောင်းပေးရပါမယ်၊ ဥပမာ read only ပြောင်းပါဆိုရင် ```chmod 111 myfile``` or ```chmod a=r myfile``` ဆိုပြီးပြောင်းနိုင်ပါတယ်)

##### Example output 5
```
1) Create file or dir
2) Delete file or dir
3) List all files and dirs
4) List all executable files
5) Change permissions
6) Exit
#? 5
name? blahblah
No file or dir
#? 5
name? hello.sh
1) Read only
2) Read & Write
3) Full
4) No permission
permission? 3
Changed
#? 4
hello.sh
#? 
```

ဒီမှာဆိုရင် Permission က ရွေးစရာ ၄ မျိုးရှိပါမယ်။ (Full ဆိုတာ read, write, execute) အားလုံးကို ဆိုလိုပါတယ်။ (No permission ဆိုတာ read, write, execute တစ်ခုမှမရှိတာကိုဆိုလိုပါတယ်)

Example ကို သေချာလေးကြည့်ပေးပါ

> permission ရွေးဖို့တောင်းတဲ့နေရာမှာ ထပ်ခါထပ်ခါမတောင်းရပါဘူးနော်။ တစ်ခါပဲတောင်းပြီးတော့ အလုပ်လုပ်ပြီးတာနဲ့ မူရင်း menu ကို ပြန်သွားပါတယ်

#### 6 Exit

ဒါကတော့ ရှင်းပါတယ် 6 ကိုရွေးလိုက်တာနဲ့ program က ထွက်သွားပါပြီ။ 6 မရွေးမချင်း ဆက်တိုက် အလုပ်လုပ်နေမှာပါ။

<br>
<hr>
<br>

### ရှင်းလင်းချက်

> ရှင်းလင်းချက်များများစားစားမပြောတော့ပါဘူး Step-3 မှာ ပြည့်ပြည့်စုံစုံရှင်းပြပေးထားပါတယ်

> Asm တင်တဲ့အခါမှာတော့ shell file တစ်ခုတည်းသာတင်ပေးရပါမယ်။

> Example တိုင်းမှာ ကျွန်တော် roll နဲ့ email ထုတ်မပြထားပါဘူး၊ (ရှုပ်နေမှာစိုးလို့)။ ဒါကြောင့် ရေးတဲ့အခါမှာတော့ အရင် Asm တွေတုန်းကလို roll email သည် ထိပ်ဆုံးမှာ ရှိနေရပါမယ်

<br>
<hr>
<br>

### စည်းကမ်းချက်

1. File name ကို asm4_g3u001.sh (g3u001 နေရာမှာ ကိုယ့်ရဲ့ roll no ဖြစ်ရပါမည်) ဟုပေးရမည်
2. 2. File ကို submit လုပ်တဲ့အခါမှာ .sh ဖြင့်ဆုံးသော shell file သာဖြစ်ရပါမည်။ (Screenshot များ၊ zip file များ၊ docs file များ၊ အစရှိသော shell file မဟုတ်သည့် တခြား file များပေးပို့လျှင် အမှတ်လုံးဝ ရရှိမည်မဟုတ်ပါ)
3. 3. Sample output မှာ ပြထားတဲ့အတိုင်း output လိုထွက်ရပါမည်။ လိုအပ်တဲ့ output များကို တိတိကျကျ ထုတ်ပေးဖို့ အရေးကြီးပါတယ်။(ဥပမာ - ကိုယ့်ရဲ့ roll, email) မလိုအပ်တဲ့ output များ၊ output အပိုများ၊ ထွက်လို့ မရပါ။ ထွက်လျှင် အမှတ်ရမည်မဟုတ်ပါ
4. သတ်မှတ်ချိန်အတွင်း အမှီတင်ပေးနိုင်ရပါမည်
5. 4. Step ၃ ခုမှာပြောထားတဲ့ စည်းကမ်းချက်တွေနဲ့ကိုက်ညီပြီး မလိုအပ်တာများ echo ထုတ်မပေးရပါ
Assignment တင်ရန် Link


[https://forms.gle/3rgUBhhYMGjdPxBT8](https://forms.gle/3rgUBhhYMGjdPxBT8)
