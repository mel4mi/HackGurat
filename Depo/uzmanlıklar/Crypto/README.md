
<!--
![](https://github.com/mel4mi/siber-guvenlik-ziggurat/blob/main/Depo/resimler/block.png)
# Tadilatta
-->

# Cryptology
Cryptology, her türlü verinin kullanıldığı bugünlerde önemi gittikçe artan bir veri bakış açısıdır. Cryptology'nin genel amacı, verilerin bütünlüğünü sağlamak, verilerin yanlış kişilerin eline geçtiğinde okunamaz hale getirmek ve client'ler(cihazlar,sistemler, vs.) arasındaki iletişimin gizliliğini ve bütünlüğünü sağlamaktır. Bu metodolojilere güncel hayatta örnek vermek gerekirse; hesaplarınızda kullandığınız parolaların saklanmasından tutun bir bankacılık işlemi sırasında yaptığınız isteklerin dışarıdan okunamaz ve değiştirilemez hale getirilmesine kadar her alanda cryptology kullanılmaktadır.


## Temel 3 Prensip
Kendi açımdan cryptology alanını tanımlamak için, üç temel prensibi kullanarak anlatmak daha doğru olacaktır.
Bunlar:
1- Encoding
2- Encrypting
3- Hashing

---
### Encoding
<!-- ![encode](/Depo/uzmanlıklar/Crypto/fotolar/encoding_cutted.png) <br> -->
Encoding kodlama olarak çevirebileceğimiz(bkz. tureng) çift taraflı bir veri dönüştürme işlemidir. bu tanımı açmak gerekirse encoding işlemi verinin erişilebilmesini zorlaştırmaktan ziyade kolaylaştırmayı amaçlamaktadır. Örneklendirmek gerekirse fotoğraflar non-ascii dediğimiz normal karakterlerden oluşmayan bir şekli vardır. Biz bir fotoğrafları taşımaya çalıştığımızda veri kayıpları yaşacanağından dolayı fotoğraflarımız bozuk gelebilir. Bu yüzden non-ascii verileri başka formatlara encode ederek bu kayıpları önlemeye çalışırız.

 #### Örnek:
  ```
  Dönüştürülmemiş veri --> [Base64 Encode Algorithm] -->  RMO2bsO8xZ90w7xyw7xsbWVtacWfIHZlcmk=
  ```

  
  Aynı Şekilde dönüştürülmüş veri ilk haline çevrilebiliriz. Bu da encoding işlemini çift taraflı olarak tanımlamamıza sebep oluyor.


  
  ```
  RMO2bsO8xZ90w7xyw7xsbWVtacWfIHZlcmk= --> [Base64 Decode Algorithm] --> Dönüştürülmemiş veri
  ```

  Encoding işlemi sadece veri taşımakla da sınırlı değildir. İlkel şifreleme dediğimiz eskiden kullanılan verilerin güvenliğini sağlamak için kullanılan 
algoritmalar vardı fakat kırılması çok kolay olduğundan dolayı günümüzde kullanılmaktadır. örnek: [sezar şifrelemesi](https://teknolojiprojeleri.com/teknik/sezar-sifreleme)
 #### Deneme yapmak için:
 [Cyberchef](https://gchq.github.io/CyberChef/),
 istediğiniz encode yöntemini seçip mesajlarınızı encode edebilirsiniz.

---
### Encrypting
Encrypt etmek, saklanmak istenen veriyi bir anahtar ile şifreleyip sadece tekrardan o anahtar ile açmayı amaçlayan yaklaşımdır. Bu yaklaşım teknoloji camiyaında yaygın olarak kullanılmaktadır. Örneklendirmek gerekirse şuan bu web sitesine bağlanırken kullandığınız ssl koruması veya kişisel dosyalarınızı bitlocker ile şifrelerken kullandığınız şifrelemeleri örnek olarak gösterebiliriz. Encypt işlemi güçlü matematik algoritmalarını kullanarak anahtarsız bir şekilde verileri geri döndürülemeyecek hale getirene kadar devam eder. Bu matematiksel fonksiyonlar, bir kişinin tek tek ihtimalleri düşünerek allgoritmada geri gidip veriyi çözmesi imkansıza çok yakındır. Fakat şifrelenen veriyi tekrar kullanmamız gereken durumlar olacaktır. Bunun içinde encrypt aşamasında şifreye çözecek bir anahtar (private key) üretilir. Bu anahtar sadece o şifreleme işlemine özeldir, kopyalanması imkansıza yakındır ve şifrelenmiş veri sadece o anahtarla açılır. Sonuç olarak bu yapılan işlemler bir demircinin kasa yapmasına benzerdir. Size ait bir kasa var ve kasanın içindekilere erişmek için size bir anahtar üretilir. Anahtara sahip olamayan kişilerde kasanızın içindekilere erişemez.



---
### Hashing
Hashing işlemini özetleme olarak türkçeye çevirebiliriz. hashleme dediğimiz şey istediğiniz herhangi boyuttaki veriyi hep aynı uzunlukta olacak şekilde değiştirmesidir. Kafa karışıklığını önlemek için örneklendirelim: <br>
![hashing](/Depo/uzmanlıklar/Crypto/fotolar/hashing.png)
Yukarıdaki fotoğrafa dikkatli bakarsak farklı 2 metin ve metinlerin boyutları gösterişmiştir. Sonrasında bu 2 metni de md5 ile hashliyoruz ve hashlerin içeriği değişsede genel uzunluğu 2 hashinde 16'dır. Kısaca anlatmak gerekirse hashlemek bu şekilde çalışır.

---
### Cryptology Uzmanı ne iş yapar ? 
Gösterdiğim bu 3 alan ve daha nice alanları bünyesinde bulunduran ve genel olarak veri güvenliğini sağlayan uzmanlara cryptology uzmanları denir. Yukarıda anlattığım algoritmalar sürekli güncellenmeye ve geliştirilmeye ihtiyaç duyar çünkü her zaman akıl akıldan üstündür. Tarihde öncesine baktığımız zaman nist standartı olarak kabul edilen DES algoritması şuan kullanılması tabiri caizse yasaklanmıştır. Çünkü sahip olduğu algoritma bugünkü şartlar altında çok kolay bir şekilde kırılmaktadır. Hakeza şuan kullandığımız ssl aslında zaafiyetlerinden dolayı 6 defa değiştirilerek şuan tls olarak kullandığımız hale gelmiştir. İşte bu yüzden Cryptology uzmanları şifreleme sistemleri üretir, şifreleme algoritmalarını güvenliğini test eder ve şifrelemeleri çözmeye çalışır. 

<br><br><br>






## Kaynaklar:
- [Bilgi Güvenliği ve Kriptografi](https://gnexlab.medium.com/bilgi-g%C3%BCvenli%C4%9Fi-ve-kriptografi-652f3c8e4225)
- [Kriptografi Nedir](https://anilcelik.medium.com/tr-kriptoloji-ve-kriptografi-nedir-f74ced3a6b7e)
- [Sezar Şifrelemesi Nedir?](https://caylakyazilimci.medium.com/sezar-%C5%9Fifrelemesi-nedir-9dc54b18e56d)
- [Xor Nedir](https://www.mehmetince.net/crypto-101-1-merhaba-exclusive-or-xor/)
- [AES Encryption Decryption](https://medium.com/@hazal333302/aes-encryption-decryption-f04e08d067db)


### Örnek Vakalar ve Çözümleri:
- [Cracking AES Without any one of its Operations](https://medium.com/@wrth/cracking-aes-without-any-one-of-its-operations-c42cdfc0452f)
- [Single-Byte XOR | CSAW CTF "babycrypto"](https://www.youtube.com/watch?v=p__QZIxjHMk&list=PL1H1sBF1VAKU05UWhDDwl38CV4CIk7RLJ)
- [Simple Cryptography Ctf](https://www.youtube.com/watch?v=j9xht4K-MBk)
- [Break Me!, DownUnder CTF 2021, Writeup](https://0awawa0.medium.com/break-me-downunder-ctf-2021-writeup-d2f4db2144b6)
- [ICMTC CTF — Cryptography Challenge Writeup "Bad Mode"](https://medium.com/@motarekk/icmtc-ctf-cryptography-challenge-writeup-bad-mode-416f49bb1b54)


### Youtube Kaynakları
- [Kriptoloji (Şifreleme)](https://www.youtube.com/playlist?list=PLh9ECzBB8tJM-T5Dlbh-Byl_9c_2d9pbk) - BilgisayarKavramlari
- [Kriptoloji](https://www.youtube.com/playlist?list=PL_OkErp2FkJQ3DdRDaltKNM7y_1jZZT_f) - Konsol Ekranı
- [30 Derste Bilgi Güvenliği](https://www.youtube.com/playlist?list=PLKnjBHu2xXNNq-icsYoo3LQOZK9DKZU7W) - Murat Yücedağ
- [Introduction To Cryptography](https://www.youtube.com/@introductiontocryptography4223/videos) - Christof Paar


### lablar:
- [Google ctf](https://capturetheflag.withgoogle.com/challenges)
- [Csaw19](https://www.csaw.io/csaw19archive)
- [Hackthebox](https://app.hackthebox.com/challenges?category=2&sort_type=asc)
- [THM - cryptographyfordummies](https://tryhackme.com/r/room/cryptographyfordummies)
- [THM - cryptographyintro](https://tryhackme.com/r/room/cryptographyintro) 
- [THM - theimpossiblechallenge](https://tryhackme.com/r/room/theimpossiblechallenge)
- [Ringzer0](http://ringzer0ctf.com/)










