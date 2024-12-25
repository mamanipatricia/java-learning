# install intellij

1. intellij idea 2024.3.1.1
- go to: https://www.jetbrains.com/idea/download/other.html and download the version you want (avoid release candidate versions = RC)
example: `2024.3.1.1 - Linux x86_64 (tar.gz)`
- uncompress in /opt/
  `sudo tar xzfv ~/Downloads/ideaIU-2024.3.1.1.tar.gz -C /opt/`
 check where and what is the name of the uncompressed folder is
mine is: idea-IU-243.22562.218 

- go to `cd /opt/idea-IU-243.22562.218/bin`
- edit the vmoptions `sudo nano idea64.vmoptions`
add these lines
```
-javaagent:/home/pat/jetbrains-cosas/jetbra(240701)/ja-netfilter.jar=jetbrains
--add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED
--add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED
  ```
NOTE: check and point to the correct folder where is placed the jetbra(240701) foder
NOTE1: jetbra(240701) folder is the last version working for 2024.3.x idea version

- In case you don't have the latest jetbra download it from here: https://3.jetbra.in/ and save it in a folder (remember the place of this folder)

- update the path of the jetbra folder in vmoptions. 
example: /home/pat/jetbrains-cosas/jetbra(240701)/

- open the `./idea` not the `./idea.sh` and paste the activation code
- generate the desktop entry press `shift + shift` > type create desktop entry > enter



