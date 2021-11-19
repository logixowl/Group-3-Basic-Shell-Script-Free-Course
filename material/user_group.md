# Users & Groups in Linux

## User Creatation

> user create လုပ်ဖို့အတွက် root user ဖြစ်နေမှလုပ်လို့ရပါမယ်

> ```sudo``` ကို သုံးပြီးလဲ create နိုင်ပါတယ်


#### User create with root user
```sh
su - root
# root password ထည့်
useradd owl
exit
```

#### User create with sudo command
```bash
sudo useradd owl
# current user password ထည့်
```

```-d``` option to define user's home directory

```bash
sudo useradd -d /home/logix owl
ls /home
# owl ဆိုတဲ့ dir ကို တွေ့လိမ့်မည်
```

#### Create a User with Account Expiry Date
```bash
useradd -e 2021-11-30 owl
```

#### Add a User with Specific Home Directory, Default Shell, and Custom Comment

```bash
useradd -m -d /home/logix -s /bin/bash -c "This is also me LogixOwl" -U owl
```

#### User Delete
```bash
# to delete user
sudo userdel owl

# to delete user and user's home dir
sudo userdel -r owl
```

#### Change user password
```bash
sudo passwd owl
```

Once a new user is created, its entry is automatically added to the ```/etc/passwd``` file

#### User info
```bash
cat /etc/passwd | grep owl
```
##### Output will be
```
owl:x:1000:1000:owl:/home/owl:/bin/bash
```
| Column | Description |
| --- | --- |
| Username | User login name used to login into the system. It should be between 1 to 32 characters long. |
| Password | User password (or x character) stored in /etc/shadow file in encrypted format. |
| User ID (UID) | Every user must have a User ID (UID) User Identification Number. By default, UID 0 is reserved for the root user and UID’s ranging from 1-99 are reserved for other predefined accounts. Further UID’s ranging from 100-999 are reserved for system accounts and groups. |
| Group ID (GID) | The primary Group ID (GID) Group Identification Number stored in the /etc/group file. |
| User Info | This field is optional and allows you to define extra information about the user. For example, user full name. This field is filled by the ‘finger’ command. |
| Home Directory | The absolute location of the user’s home directory. |
| Shell | The absolute location of a user’s shell i.e. /bin/bash. |

#### Group create
```bash
sudo groupadd programmers
sudo groupadd developers
sudo groupadd barnyar
```

#### Add a user to a group
```bash
sudo usermod -a -G developers owl

# for new user
sudo useradd -G developers owl

# for multiple groups
sudo usermod -aG developers,programmers,barnyar owl

# to verify
id owl
```

#### Check groups list
```bash
cat /etc/group
```

