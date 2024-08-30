# HTB Perfection

```bash
nmap -sV -sT -Pn 10.10.11.253 > nmap.txt
```

nmap

![Untitled](Perfection%2061be048794494634a64af5963e07058d/Untitled.png)

## Try fuzzing diretories

manual fuzzing and got 404 not found

![Untitled](Perfection%2061be048794494634a64af5963e07058d/Untitled%201.png)

![Untitled](Perfection%2061be048794494634a64af5963e07058d/Untitled%202.png)

ใช้ dirb กับ ffuf แล้วก็ไม่เจออะไร

![Untitled](Perfection%2061be048794494634a64af5963e07058d/Untitled%203.png)

# check request

weigted

```
POST /weighted-grade-calc HTTP/1.1
Host: 10.10.11.253
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:102.0) Gecko/20100101 Firefox/102.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 168
Origin: http://10.10.11.253
Connection: close
Referer: http://10.10.11.253/weighted-grade
Upgrade-Insecure-Requests: 1

category1=a&grade1=4&weight1=20&category2=b&grade2=4&weight2=20&category3=c&grade3=4&weight3=20&category4=dasdase&grade4=4&weight4=20&category5=sdas&grade5=4&weight5=20
```

###