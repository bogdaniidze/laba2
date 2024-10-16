# laba2

На основе изученного материала лабораторной работы, лекций (2 и 3), дополнительных источников написал скрипт, который на вход принимает IPv4-адрес в десятичном формате, а на выходе обеспечивает данный IP-адрес в двоичном формате.
```
#!/bin/bash

IP=$1

IFS='.' 
read -r i1 i2 i3 i4 <<< "$IP"
printf "%08d.%08d.%08d.%08d\n" \
    "$(bc <<< "obase=2;$i1")" \
    "$(bc <<< "obase=2;$i2")" \
    "$(bc <<< "obase=2;$i3")" \
    "$(bc <<< "obase=2;$i4")"
```

![image](https://github.com/user-attachments/assets/7c0169f5-d8cf-4c76-ab27-1738bbbc5d3a)
