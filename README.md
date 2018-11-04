# snort IDS under Windows environemnt 
a working configuration repository for snort under Windows

![img](https://i.imgur.com/v5XbmGr.png)

# quick guide
It was a pain in the ass to get snort working under windows that's due to the lack of people using it under Windows, so I decided to share my journey into getting it running under Windows 10 (same should be applicable for any other version of Windows)

1. go ahead and download snort windows from here: https://www.snort.org/downloads#snort-downloads
2. download rules (`snortrules-snapshot-XXXXXX.tar.gz`), I used bugmenot to find a login because I don't want to register: https://www.snort.org/downloads#rules
3. extract the rules into `c:\snort\` replacing all duplicates
4. replace `snort.conf` with the one I uploaded here. Credits to [Steve Gantz](https://www.youtube.com/watch?v=RwWM0srLSg0)
5. run `snort -W` to get which interface is your target to monitor
6. execute snort with `snort -i <interface #> -c c:\snort\etc\snort.conf`
7. logs will be in `c:\snort\log\`

# tags and erros that are solved by this file are listed here
* `ERROR: /etc/snort/snort.conf(326) => Invalid keyword '}' for server`
* `ERROR: Misconfigured dynamic preprocessor(s)`
* `Fatal Error, Quitting..`
* `ERROR: /etc/snort/rules/app-detect.rules(33) Unknown ClassType: web-application-attack`
