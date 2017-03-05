#ARP - 150 - Soru
ARP saldırısı yapan cihazın hostname bilgisini bulun.

http://battalfaik.com/SGB/100e7a83f1b3d2da4694eeb6d028ee86.rar

#Cevap

Soru gayet açık. Bize bir .pcap dosyası verilmiş ve ARP saldırısı yapan cihazın hostname bilgisi isteniyor.

Bu soru için .pcap dosya analizinde çokça kullanılan yazılımlardan biri olan Wireshark'ı kullanacağız.

Dosyamızı Wiresharkta açıyoruz ve filtre kısmına;

> bootp.option.type == 53

yazarak DHCP trafiğini görebilirsiniz.

Flagimiz;
> Bootstrap Protocol (Inform) > Option: (12) Host Name

altındaydı.

* Flag : sgt_{malware-x}
