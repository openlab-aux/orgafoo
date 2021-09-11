# How to add new users 

## Add a new key to lock

connect to ctl computer:


Present the new card.
You will see the ID of the new card:

``` 
root@sphincterctl:/# tail -f screenlog.0
Found 1631357111 060080A02XXX OK
Key 060080A02XXX not in list file!
```

add the new user to the list:

```
root@sphincterctl:~# nano /opt/rfid/rfidlist/list.txt
```

```
0600553B1QQQ    Mr. Unknown
0600553B1XXX    Bender
060080A02XXX    NewUser
```

Reboot, test, done 👍
