# snort IDS under Windows environemnt 
a working configuration repository for snort under Windows

![img](https://i.imgur.com/v5XbmGr.png)

# quick guide
It was a pain in the ass to get snort working under windows that's due to the lack of people using it under Windows, so I decided to share my journey into getting it running under Windows 10 (same should be applicable for any other version of Windows)

1. go ahead and download snort windows from here:
2. download rules, I used bugmenot to find a login because I don't want to register
3. extract the rules into `c:\snort\` replacing all duplicates
4. replace `snort.conf` with the one I uploaded here. Credits to [Steve Gantz](https://www.youtube.com/watch?v=RwWM0srLSg0)
5. run `snort -W` to get which interface is your target to monitor
6. execute snort with `snort -i <interface #> -c c:\snort\etc\snort.conf`
7. logs will be in `c:\snort\log\`
