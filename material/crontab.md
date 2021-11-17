# Scheduling in Linux

## Crontab

### Usage & Example
```bash
# Example of job definition:
# .---------------- minute (0 - 59)
# |  .------------- hour (0 - 23)
# |  |  .---------- day of month (1 - 31)
# |  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
# |  |  |  |  .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
# |  |  |  |  |
# *  *  *  *  * user-name command to be executed
# 17 *    * * *   root    cd / && run-parts --report /etc/cron.hourly
# 25 6    * * *   root    test -x /usr/sbin/anacron || ( cd / && run-parts --report /etc/cron.daily )
# 47 6    * * 7   root    test -x /usr/sbin/anacron || ( cd / && run-parts --report /etc/cron.weekly )
# 52 6    1 * *   root    test -x /usr/sbin/anacron || ( cd / && run-parts --report /etc/cron.monthly )
```

### Crontab command
```bash
# to read manual 
cat /etc/crontab

# to list crontabs
crontab -l
crontab -l -u mgmg

# to edit crontabs
crontab -e
crontab -u mgmg -e
```

### Cheatsheet 
```bash
* * * * * CMD
# run CMD every minute

*/2 * * * * CMD
# every two minute

0-20/5 * * * * CMD
# every 5 minute in first 20 minute

0 9, 15 * * * CMD
# every day, 9:00AM and 3:00PM

0 7 2-6 * * CMD
# every month, 2, 3, 4, 5, 6 days 7:00AM

@hourly CMD
@daily CMD
@monthly CMD
@yearly CMD
@reboot CMD # when the computer is reboot
# shortcuts
```