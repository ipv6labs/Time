# Windows NTP

* cmd.exe in administrative mode


## NTP server

### Set NTP server

```
C:\Windows\system32>reg add HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W32Time\Parameters /v NtpServer /t REG_SZ /d ntp.nict.jp,0x8 /f
```

### Get NTP server

```
C:\Windows\system32>reg query HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W32Time\Parameters /v NtpServer

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W32Time\Parameters
    NtpServer    REG_SZ    ntp.nict.jp,0x8
```

## Time synchronization

### Set UpdateInterval

```
C:\Windows\system32>reg add HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W32Time\Config /v UpdateInterval /t REG_DWORD /d 100 /f
```

### Get UpdateInterval

```
C:\Windows\system32>reg query HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W32Time\Config /v UpdateInterval

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W32Time\Config
    UpdateInterval    REG_DWORD    0x64
```

