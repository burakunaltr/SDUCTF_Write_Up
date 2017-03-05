#WPA2Hack - 200 - Soru

Kablosuz ağın sahibinin 23.07.95 doğumlu olduğunu öğrendik.

http://battalfaik.com/SGB/f6b16d7c2dd79e502b19c31b33155062.rar

* Hint: Parola 8 karakterli.

#Cevap

Soruda bir .cap dosyası verilmiş ve bizden ağın parolası isteniyor. O halde tekrar aircrack-ng ye baş vuracağız. Ancak bu bir WPA/WPA2 şifrelemeyle korunan ağ ve parola bilgisi için elimizde bir wordlist olması gerekiyor.

Soruda verilen ip uçlarını kullanarak wordlist oluşturma aracı olan 'crunch' ile 8 karakterli bir wordlist oluşturduk.

> crunch 8 8 230795 -o pass.txt

Toplamda 14 MB boyutunda 1679616 adet parola oluşturdu.

oluşan wordlist ile aircrack-ng aracını çalıştırdık.

> aircrack-ng -w pass.txt wpa2hack.cap

* Flag : sgt_{23200577}

