# Reverse Engineering APK

Challenge site = [CTFLearn](https://ctflearn.com/challenge/962)<br>
Tools used = <br>
- Android Emulator (I use [Genymotion](https://www.genymotion.com/))<br>
- [Apktool](https://apktool.org/) for decompiling.

## Steps
1. Decompile the apk using apktool. 
```bash
apktool d apkname.apk
```
2. cd into the directory.
3. The method i'm using is grep. Try grepping the flag using keywords like CTFlearn.
```bash
# I'm using ripgrep in here, but you can also do grep -rPn
➜  BasicAndroidRE1 rg "CTFlearn"
smali/com/example/secondapp/MainActivity.smali
80:    const-string v2, "Success! CTFlearn{"
➜  BasicAndroidRE1 
```
3. If you still cant grep it, make sure you use grep recursively, or try grepping/searching it directly in /smali/com/example/secondapp/

4. After looking a bit into the MainActivity.smali, i noticed there was a Hash string inside
```smali
const-string v1, "b74dec4f39d35b6a2e6c48e637c8aedb"
```

5. After doing a quick google search, it leads me to this MD5 reverse hash database, and got the password, which is Spring2019.

6. After getting the password, I boot the android emulator up, launch the apk file, and put the password in.


