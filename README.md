# PicoWU

**ALL CATEGORIES**:
- Forensics:
  - MacroHard WeakEdge
- WebEx:
- Reverse:
- Crypto:
  
## Forensics
- ### MacroHard WeakEdge:

I've hidden a flag in this file. Can you find it? Forensics is fun.pptm <br>
60 pts | no hints<br>

first download the file with
```txt
wget https://mercury.picoctf.net/static/c00c449c3b08daaccacca6f9d5c55d49/Forensics%20is%20fun.pptm
```
we get a pptm file which I [searched](https://fileinfo.com/extension/pptm) for a little is similar to pptx <br>
then we unzip the file with:
```txt
unzip {file_name} OR 7z x {file_name}
```
we got a lot of files that don't stand out a lot from each other. after looking one by one, one file caught my eye "ppt/slideMasters/hidden"

so i tried:
```txt 
cat hidden
```
which output is `Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q`. i realized it's a base64 encryption so i brought up [CyberChef](https://gchq.github.io/CyberChef/) to help me decrypt the messege.
the out put will be `flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}`
