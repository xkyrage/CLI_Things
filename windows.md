### Disguise folder
> copy /b image.extension+folder.zip image.extension

### Encrypt folder
> cipher /E

### Hide folder
> attrib +h +s +r foldername
> attrib -h -s -r foldername

### Show wlan
> netsh wlan show profile
> netsh wlan show profile wifinetwork key=clear | findstr"Key Content"
> make a batch file
```
@echo off
setlocal enabledelayedexpansion

for /F "tokens=2 delims=:" %%a in ('netsh wlan show profile') do (
set wifi_pwd=
for /F "tokens=2 delims=: usebackq" %%F IN ('netsh wlan show profile %%a key^=clear ^| find "Key Content"') do (
set wifi_pwd=%%F
)
echo %%a : !wifi_pwd!
)

```

### Check system information
> systeminfo

### Secure copy
> scp file.txt root@serverip:~/file.txt

### Open explorer at specific Directory
> explorer .

### Map any folder within the system
> subst <driveletter example input Q: it will make a Q: drive>: "c:\filelocation"
> subst /d <driveletter example input Q: it will make a Q: drive>: c:\filelocation

### Customize CMS color theme
> color 02

### Change prompt locator
> prompt {text}$G
> prompt

### Change cmd title
> title <titleyoudesired>

### Curl
unshorten shorten link
> curl --head --location "shortlink" | findstr Location

Post live url into prompt
> curl <url>

Curl post live url
```
wttr.in/bandung <checking weather>
ascii.live/rick
ascii.live/parrot
ascii.live/forrest
ascii.live/knot
ascii.live/coin
ascii.live/donut
ascii.live/time
```

Check status of a website
> curl -IsL <targetfullurl>

Check website ip address
> curl checkip.<targetfullurl>

Make QR from url
> curl qrenco.de/<fullurl>

Check latest thing using decapi.me
> curl -s https:decapi.me/<media>/latest?name=<username>or user=<username>

Check definition of a word
> curl dict.orgp/d:<word>

### Open up a web from cmd
> start <fullurl>

### Delete all temp files in windows
> del /q /f /s %temp%\*
> del /s /q C:\Windows\Temp\*

### Telnet telehack
> telnet telehack.com

### open up the previous command prompt you enter
> press f7 on command prompt

