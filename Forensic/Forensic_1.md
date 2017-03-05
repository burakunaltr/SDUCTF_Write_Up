# lsass.dump - 300 - Soru
Parola bilgisini arıyoruz.

http://battalfaik.com/SGB/6f4d4abb5f2fd6a6cd57ea4d1208ace8.rar

# Cevap
Bu soruda bizden istenen dump edilmiş bir lsass dosyasını incelememizdi. lsass dosyası Windows sistemlerde oturum bilgilerini tutan kritik bir dosyadır.
Windows üzerinde "mimikatz" aracı ile bu dosyayı analiz edebilirdik.

mimikatz üzerinde şu kodları çalıştırmamız yeterliydi.

>privilege::debug

>sekurlsa::minidump lsass.dmp

>sekurlsa::logonPasswords

* Flag: sgt_{ramizkaraeski}
