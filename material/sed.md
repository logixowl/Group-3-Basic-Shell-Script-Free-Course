# Linux SED Command

> SED stands for stream editor

SED is useful for
* searching
* replacing
* insertion
* deletion

### SED Examples

#### Sample text file - data4.txt

```
do you like apple? apple is a fruit and i have a lot of apples. i do like apple.
logixowl, knowledge sharing
happy shell script course
hello apples!
this is also apple.
a quick brown fox jumps over the lazy dog.
orange, apple, avocado, mango
```

[You can download](../data/data4.txt)

#### Example - 1

```sh
sed 's/apple/banana/' data4.txt
```

##### Output:

```
do you like banana? apple is a fruit and i have a lot of apples. i do like apple.
logixowl, knowledge sharing
happy shell script course
hello bananas!
this is also banana.
a quick brown fox jumps over the lazy dog.
orange, banana, avocado, mango
```

##### Explanation

* **s => substitution**
* data4.txt ထဲက apple ဆိုတဲ့ စာလုံးကို orange ပြောင်း
* ပထမဆုံးတွေ့တဲ့ apple (first occurrence) ကို ပဲ ဒီမှာ (default) replace လုပ် (ပထမဆုံး line ကိုကြည့်ပါ)

#### Example - 2 (nth occurrence)

```sh
sed 's/apple/banana/3' data4.txt
```

##### Output:
```
do you like apple? apple is a fruit and i have a lot of bananas. i do like apple.
logixowl, knowledge sharing
happy shell script course
hello apples!
this is also apple.
a quick brown fox jumps over the lazy dog.
orange, apple, avocado, mango
```
##### Explanation

* တတိယမြောက် occurrence ကို replace လုပ်


#### Example - 3 (for all occurrence)

```sh
sed 's/apple/banana/g' data4.txt
```

##### Output:
```
do you like banana? banana is a fruit and i have a lot of bananas. i do like banana.
logixowl, knowledge sharing
happy shell script course
hello bananas!
this is also banana.
a quick brown fox jumps over the lazy dog.
orange, banana, avocado, mango
```
##### Explanation

* apple စာလုံးအားလုံးကို replace လုပ်


#### Example - 4 (nth occurrence to all)

```sh
sed 's/apple/banana/2g' data4.txt
# စက်တိုင်းနဲ့ အဆင်မပြေနိုင်ပါ
```

##### Output:
```
do you like apple? banana is a fruit and i have a lot of bananas. i do like banana.
logixowl, knowledge sharing
happy shell script course
hello apples!
this is also apple.
a quick brown fox jumps over the lazy dog.
orange, apple, avocado, mango
```
##### Explanation

* ဒုတိယ occurrence ကနေ အဆုံးထိ replace လုပ်

#### Example - 5 (print the line that match)

```sh
sed -n 's/apple/banana/gp' data4.txt
```

##### Output:
```
do you like banana? banana is a fruit and i have a lot of bananas. i do like banana.
hello bananas!
this is also banana.
orange, banana, avocado, mang
```

##### Explanation

* apple စာလုံးအားလုံးကို replace လုပ်
* နောက်ဆုံးမှာ ```gp``` လို့ထုတ်ထားတာတွေ့ရပါမယ်။
* ```g``` ကတော့ ထုံးစံအတိုင်း အားလုံးကို replace လုပ်တဲ့ flag ပါ
* ```p``` ကတော့ match ဖြစ်တဲ့ line ကို ပြန်ထုတ်ပေးတဲ့ flag ပါ
* ```-n``` ဆိုတဲ့ option နဲ့ ```p``` ဆိုတဲ့ flag လေးကို နှစ်ခုတွဲသုံးခြင်းအားဖြင့် replace လုပ်လိုက်တဲ့ line တွေကိုပဲ ပြန်ထုတ်ပေးပါတယ်

[တခြားအသုံးအပြုနိုင်တဲ့ flag များ](#usableflags)

#### Example - 6 (delimiter)

```sh
sed 's/apple/banana/g' data4.txt
sed 's:apple:banana:g' data4.txt
sed 's|apple|banana|g' data4.txt
sed 's-apple-banana-g' data4.txt
sed 's#apple#banana#g' data4.txt
sed 's apple banana g' data4.txt
sed 's!apple!banana!g' data4.txt
sed 's@apple@banana@g' data4.txt
sed 'sa\appleab\an\an\aag' data4.txt
```

##### Explanation

* ပုံမှန်သုံးနေကျ ```/``` နေရာမှာ တခြားသော character တွေကို delimiter အဖြစ်ပြောင်းသုံးပြထားတာပါ
* နောက်ဆုံး command မှာဆိုရင် ```a``` ကို delimiter အဖြစ် အသုံးပြုထားတာဖြစ်ပါတယ်၊ ဒါကြောင့် ကိုယ်ရှာချင်တဲ့ စာလုံးနဲ့ replace လုပ်မယ့် စာလုံးနေရာမှာရှိတဲ့ ```a``` တွေကိုတော့ ```\a``` ဆိုပြီး သုံးပေးရပါတယ်
* အဲဒီလိုပဲ တခြားသော character တွေကိုလည်း (```(\) backslash``` နဲ့ ```new line``` ကလွဲပြီး) အစားထိုးအသုံးပြုနိုင်ပါတယ်
* အလုပ်လုပ်ပုံကတော့တူတူပါပဲ
* apple စာလုံးအားလုံးကို replace လုပ်


#### Example - 7 (ဘယ်နေရာမှာ delimiter ပြောင်းပြီး သုံးရမလဲ?)

```sh
# cat /etc/passwd | sed 's//root//myroot:g' => not work
cat /etc/passwd | sed -n 's:/root:/myroot:gp'
```

##### Output:
```
root:*:0:0:System Administrator:/var/myroot:/bin/sh
daemon:*:1:1:System Services:/var/myroot:/usr/bin/false
```

##### Explanation

* ```/etc/passwd``` ဆိုတဲ့ file ထဲမှာ ```/root``` ဆိုတဲ့ စာလုံးတွေကို ```/myroot``` လို့ပြောင်းချင်တဲ့အခါ
* ပုံမှန်သုံးနေကျ ```/``` နေရာမှာ ```:``` ကို delimiter အဖြစ်ပြောင်းသုံးပေးရပါတယ်
* စက်အပေါ်မူတည်ပြီး output မတူနိုင်ပါ


#### Example - 8 (change only nth line)

```sh
sed -n '4s/apple/banana/gp' data4.txt
```

##### Output:
```
hello bananas!
```

##### Explanation

* ```4``` ကြောင်းမြောက်ကိုပဲ replace လုပ်မယ်


#### Example - 9 (delete nth line)

```sh
sed '1d' data4.txt
```

##### Output:
```
logixowl, knowledge sharing
happy shell script course
hello apples!
this is also apple.
a quick brown fox jumps over the lazy dog.
orange, apple, avocado, mango
```

##### Explanation

* line ```1``` ကို delete လုပ်
* replace လုပ်တုန်းကနဲ့တူတူပါပဲ၊ ဒါကြောင့်မလို့ မြင်သာအောင် delete နဲ့ပဲ စမ်းပြပါမယ်

[တခြားအသုံးအပြုနိုင်တဲ့ action များ](#usableactions)

#### Example - 10 (delete lines in range)

```sh
sed '2,5d' data4.txt
# sed '5,2d' data4.txt ဆိုရင် line 5 ကိုပဲ delete လုပ်ပါမယ်
```

##### Output:
```
do you like apple? apple is a fruit and i have a lot of apples. i do like apple.
a quick brown fox jumps over the lazy dog.
orange, apple, avocado, mango
```

##### Explanation

* line ```2``` ကနေ line ```5``` ထိ delete လုပ်


#### Example - 11 (delete nth line and more m lines)

```sh
sed '3,+3d' data4.txt
```

##### Output:
```
do you like apple? apple is a fruit and i have a lot of apples. i do like apple.
logixowl, knowledge sharing
orange, apple, avocado, mango
```

##### Explanation

* line ```3``` ကနေ စပြီး နောက်ထပ် line ```3``` ကြောင်းကို delete



#### Example - 12 (delete except)

```sh
sed '2,4!d' data4.txt
```

##### Output:
```
logixowl, knowledge sharing
happy shell script course
hello apples!
```

##### Explanation

* line ```2``` ကနေ line ```4``` ထိ ကလွဲလို့ ကျန်တာအကုန် delete လုပ်

#### Example - 13 (skip and delete)

```sh
sed '1~2d' data4.txt
# စက်တိုင်းနဲ့ အဆင်မပြေနိုင်ပါ
```

##### Output:
```
logixowl, knowledge sharing
happy shell script course
this is also apple.
a quick brown fox jumps over the lazy dog.
```

##### Explanation

* line ```1``` ကိုဖျက်ပြီးရင် နောက်လာမယ့် ```2``` ကြောင်းကို မဖျက်ပဲကျော်ပါမယ် ပြီးရင် လာမယ့် line ကိုဖျက်ပါမယ် ပြီးရင် ```2``` ကြောင်းကိုမဖျက်ပဲကျော် နောက်လာမယ့် line ကိုဖျက် (အဲ့လိုမျိုး line အဆုံးထိလုပ်သွားပါတယ်)

#### Example - 14 (delete nth line to end)

```sh
sed '4,$d' data4.txt
```

##### Output:
```
do you like apple? apple is a fruit and i have a lot of apples. i do like apple.
logixowl, knowledge sharing
happy shell script course
```

##### Explanation

* line ```4``` ကနေ line အဆုံးထိ delete လုပ်


### <a name="usableactions"></a>အသုံးပြုနိုင်တဲ့ action များ

```
format => /pattern/action
p ==> prints
d ==> deletes
s/p1/p2 ==> substitutes
```

### <a name="usableflags"></a>အသုံးပြုနိုင်တဲ့ flag များ

```
g => all
number => nth
p => prints that matches
w filename => writes results to filename
i/I => case-insensitive
```

***SED မှာ regex တွေလဲသုံးလို့ရပါတယ်***

[Regular Expressions](./regex.md)



















