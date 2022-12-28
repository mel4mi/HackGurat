## Forensic Nedir:
Forensic(Adli Bilişim) Dijital ortamlarda saklanan her türlü dosyaların(fotoğraflar,sesler,...) hukuki süreçlerde kullanılabilecek kanıt niteliğinde olan verileri bulabilmeyi amaçlayan uzmanlıktır.

Örneklendirmek gerekirse elimizdeki fotoğrafın meta datalarına bakarak konum, cihaz bilgisi, tarih gibi bilgilere ulaşabilir veya özel olarak fotoğrafın içine şifreli bir biçimde saklanmış fotoğraflar, metin belgeleri, ağ geçmişi(pcap) gibi dosyaları özel metodlarla çıkartıp erişebiliriz.

Bu alan özellikle CTF yarışmalarının gözdesidir ve bu alana vakıf olmak takımınıza çokça puan kazandıracaktır. O yüzden bu alanda ilerlemek için bazı kaynaklar ve işinize yarayacak toolların bir listesini bırakacağım.


### Kaynaklar(resources)
 - [ctf-wiki](https://ctf-wiki.mahaloz.re/misc/introduction/) - forensic için örnek ctf çözümü yapan site.
 - [Png And Hidden Data](https://www.hackerfactor.com/blog/index.php?/archives/894-PNG-and-Hidden-Pixels.html) - Png'nin içindeki gizli pikseller.
 - [Forensics](https://ctf101.org/forensics/overview/)
 - [Steghide](https://null-byte.wonderhowto.com/how-to/steganography-hide-secret-data-inside-image-audio-file-seconds-0180936/)
 - [Stego List](https://0xrick.github.io/lists/stego/)



### Tools(Online):
 - 📷 [AperiSolve](https://www.aperisolve.com/) - Forensic ctf'lerinde toplu analiz yapmamızı sağlar.
 - 🎧 [Audio Decoder](https://morsecode.world/international/decoder/audio-decoder-adaptive.html) - Ses dosyalarında gizlenmiş mors kodlarını çözmemizi sağlar.
 - 🖌️ [29a.ch](https://29a.ch/photo-forensics/#pca) - Fotoğraf içine gömülmüş gizli pixelleri ortaya çıkarmaya yarar.
 - 📝 [steganography](https://stylesuxx.github.io/steganography/) - Fotoğrafın içine gizlenmiş mesajları çıkarmanıza yarar.
 - 📝 [MobileFish](https://www.mobilefish.com/services/steganography/steganography.php) - Fotoğrafın içine gizlenmiş mesajları çıkarmanıza yarar.
 - 📝 [fotoforensics](https://fotoforensics.com/) - Fotoğrafın üzerine efekt atarak gizlenmiş metinleri bulmamızı sağlar.

### Tools(On Machine):
 * Binwalk
 * Steghide
   * Stegcracker
   * Stegsolve
 * Exiftool
   * Exiv2
 * Hexedit
 * Strings
 * File
 * Pngcheck
 * Zsteg
