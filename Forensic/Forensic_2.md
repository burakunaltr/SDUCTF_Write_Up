# RAM - 600 - Soru
Sadece bu dosyayı sızdırabildik. Hangi web sitelerinde gezdiğini merak ediyoruz.

http://battalfaik.com/SGB/8a2c200b4179777159437c5c3e917640.rar

# Cevap

Bu soruda bir RAM imajı verilmişti. Soruya bakılırsa muhtemelen tarayıcı geçmişinden yeni bir websitesi elde edecektik.

imajı incelemek için 'volatility' aracını kullandık.
Önce imaj için profil bilgisi elde ettik.

> volatility -f RAM.raw imageinfo

Sonra çalışan hizmetlere göz attık.

> volatility -f RAM.raw --profile WinXPSP2x86 pslist

Burada dikkatimizi çeken 2 şey vardı.
* lsass.exe
* IEXPLORE.EXE

lsass dosyasını dump edip mimikatz ile inceleyebilirdik ancak bir önceki soru tam da bunu gerektiriyordu. Bu yüzden Internet explorer geçmişine baktık.

> volatility -f RAM.raw --profile WinXPSP2x86 iehistory

Burada bir websitesi ile karşılaştık.
http://battalfaik.com/a12932b75e687cb765f44af75ff10b9a/

Başlığa bakılırsa önemli bir şeyler olmalıydı.

Bir resim var.

Site logosundan hariç bir resim daha.

Aradığımız şey bunda olabilir.

Önce exif bilgilerine baktık bi şey bulamayınca steganografi olabileceğini düşündük.

Bir yığın araç denedikten sonra resmi notepadde açıp flag formatı olan "sgt_" i aradık.

* Flag: sgt_{5ed0eef4f08eb76b8b8d22685644b4b7}
