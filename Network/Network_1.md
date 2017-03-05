#HACK - 3000 - Soru
Flag için yazıcıdan takım adını almanız gerekmektedir. WiFi ağına sızabilmek için dosyayı kullanınız.

http://battalfaik.com/SGB/WarOfHackers-01.rar

Soruyu ilk çözen takım puanı alır. Soru çözüldüğünde Network kapanacak ve yarışmanın bitmesine yarım saat kalacaktır.
Siber savaş başlasın...

IP adresleri = 192.168.10.151, 192.168.10.152

#Cevap
Burada bizden verilen .cap dosyasını kullanarak ağa sızmamız ve ağda paylaşıma açık makinalar üzerinden yazıcıdan takım adımızı yazdırmamız bekleniyordu.

Eğer bir Wifi ağından bahsediliyorsa akıllara gelen ilk araç genellikle 'aircrack-ng'dir.
Öncelikle .cap dosyamızı aircrack e bırakıyoruz ve ağ hakkında bazı bilgiler ediniyoruz.
>aircrack-ng WarOfHackers-01.cap

* BSSID : 40:F3:08:80:A0:9B
* Encryption : WPA

Ağımız WPA ile korunduğuna göre mutlaka bir wordliste ihtiyacımız var. Bu bir CTF olduğuna göre meşhur wordlistlerden olan rockyou işimize yarayabilir.
Artık dosyayı brute force için aircrack e bırakabiliriz.

> aircrack-ng -w rockyou.txt -b 40:F3:08:80:A0:9B WarOfHackers-01.cap

Bi 10-15 dakika sonra parolayı verecektir.

* iloveyoubam

Parolayı kullanarak ağa bağlanabildik ancak bu sırada birinci olan takım senaryonun ikinci kısmını bitirdiği için soru kapandı ve devam edemedik :)

