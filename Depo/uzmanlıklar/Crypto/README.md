
<!--
![](https://github.com/mel4mi/siber-guvenlik-ziggurat/blob/main/Depo/resimler/block.png)
# Tadilatta
-->

# Cryptology
Cryptology, Her türlü verinin kullanıldığı bugünlerde önemi gittikçe artan bir veri bakış açısıdır. Cryptology'nin genel amacı verilerin bütünlüğünü sağlamak ve verilerin yanlış kişilerin eline geçtiğinde, verilerin okunamayacak(anlaşılmayacak) hale getirilmesidir. Örneklendirmek gerekirse, X adlı bir kullanıcının şifresi 123456 şeklinde bir veritabanında raw[yalın(gözüktüğü gibi)] saklanması, kötü niyetli bir hacker tarafından veritabanına erişildiğinde bütün kullanıcı adı ve şifrelerini rahatça okumasına yol açacaktır. Bu yüzden cryptology alanı, verileri encrypted(şifrelenmiş) biçimde saklamayı açamlar. Bir örnekle her şey daha anlaşılır olacak.

## Örnek:
![Raw tablo](/Depo/uzmanlıklar/Crypto/fotolar/ornek_veritabanı(raw).png) <br>
Yukarıdaki veritabanı örneği, kullanıcı adı ve şifre bilgilerini yalın(şifrelenmemiş) bir şekilde tutar. Bir veritabanını içindeki bilgilerin böyle yalın tutulması, veritabanını ele geçiren bir kötü niyetli kişi, verileri rahatça kullanabilir veya rahatça satılabilir. Bu da bizim gibi son kullanıcılar için bir felakete yol açabilir.

![hashed tablo](/Depo/uzmanlıklar/Crypto/fotolar/ornek_veritabanı(hashed).png) <br>
Yukarıdaki tablo ise bir önceki tabloda bulunan şifrelerin hashlenerek saklanmış halidir. Kötü niyetli bir hacker böyle bir veritabanına eriştiği zaman bu bilgileri kullanabilmesi için öncelikle hashlenmiş verileri kırması lazım. Bu işlem de baya bir vakit alacaktır. Aslında cryptology'nin temel amacı bu şekildedir. sahip olduğumuz veriler başka kişinin eline geçsede onu kullanamayacak hale getirilmesidir.
<br>
#
Cryptology sadece hashlemekle sınırlı değil. Şimdi ise daha derine inelim.






## Encoding
<!-- ![encode](/Depo/uzmanlıklar/Crypto/fotolar/encoding_cutted.png) <br> -->
Encoding kodlama olarak çevirebileceğimiz(bkz. tureng) çift taraflı bir veri dönüştürme işlemidir. bu tanımı açmak gerekirse encoding işlemi verinin erişilebilmesini zorlaştırmaktan ziyade kolaylaştırmayı amaçlamaktadır. Örneklendirmek gerekirse fotoğraflar non-ascii dediğimiz normal karakterlerden oluşmayan bir şekli vardır. Biz bir fotoğrafları taşımaya çalıştığımızda veri kayıpları yaşacanağından dolayı fotoğraflarımız bozuk gelebilir. Bu yüzden non-ascii verileri başka formatlara encode ederek bu kayıpları önlemeye çalışırız.

 ### Örnek:
  ```
  Dönüştürülmemiş veri --> [Base64 Encode Algorithm] -->  RMO2bsO8xZ90w7xyw7xsbWVtacWfIHZlcmk=
  ```

  
  Aynı Şekilde dönüştürülmüş veri ilk haline çevrilebiliriz. Bu da encoding işlemini çift taraflı olarak tanımlamamıza sebep oluyor.


  
  ```
  RMO2bsO8xZ90w7xyw7xsbWVtacWfIHZlcmk= --> [Base64 Decode Algorithm] --> Dönüştürülmemiş veri
  ```

  Encoding işlemi sadece veri taşımakla da sınırlı değildir. İlkel şifreleme dediğimiz eskiden kullanılan verilerin güvenliğini sağlamak için kullanılan 
algoritmalar vardı fakat kırılması çok kolay olduğundan dolayı günümüzde kullanılmaktadır. örnek: [sezar şifrelemesi](https://teknolojiprojeleri.com/teknik/sezar-sifreleme)
 ### Deneme yapmak için:
 [Cyberchef](https://gchq.github.io/CyberChef/),
 istediğiniz encode yöntemini seçip mesajlarınızı encode edebilirsiniz.

## Encrypting
Encrypt etmek, saklanmak istenen veriyi bir anahtar ile şifreleyip sadece tekrardan o anahtar ile açmayı amaçlayan yaklaşımdır. Bu yaklaşım teknoloji camiyaında yaygın olarak kullanılmaktadır. Örneklendirmek gerekirse şuan bu web sitesine bağlanırken kullandığınız ssl koruması veya kişisel dosyalarınızı bitlocker ile şifrelerken kullandığınız şifrelemeleri örnek olarak gösterebiliriz. Encypt işlemi güçlü matematik algoritmalarını kullanarak anahtarsız bir şekilde verileri geri döndürülemeyecek hale getirene kadar devam eder. Bu matematiksel fonksiyonlar, bir kişinin tek tek ihtimalleri düşünerek allgoritmada geri gidip veriyi çözmesi imkansıza çok yakındır. Fakat şifrelenen veriyi tekrar kullanmamız gereken durumlar olacaktır. Bunun içinde encrypt aşamasında şifreye çözecek bir anahtar (private key) üretilir. Bu anahtar sadece o şifreleme işlemine özeldir, kopyalanması imkansıza yakındır ve şifrelenmiş veri sadece o anahtarla açılır. Sonuç olarak bu yapılan işlemler bir demircinin kasa yapmasına benzerdir. Size ait bir kasa var ve kasanın içindekilere erişmek için size bir anahtar üretilir. Anahtara sahip olamayan kişilerde kasanızın içindekilere erişemez.




## Hashing
Hashing işlemini özetleme olarak türkçeye çevirebiliriz. hashleme dediğimiz şey istediğiniz herhangi boyuttaki veriyi hep aynı uzunlukta olacak şekilde değiştirmesidir. Kafa karışıklığını önlemek için örneklendirelim: <br>
![hashing](/Depo/uzmanlıklar/Crypto/fotolar/hashing.png)
Yukarıdaki fotoğrafa dikkatli bakarsak farklı 2 metin ve metinlerin boyutları gösterişmiştir. Sonrasında bu 2 metni de md5 ile hashliyoruz ve hashlerin içeriği değişsede genel uzunluğu 2 hashinde 16'dır. Kısaca anlatmak gerekirse hashlemek bu şekilde çalışır.


### Cryptology Uzmanı ne iş yapar ? 
Gösterdiğim bu 3 alan ve daha nice alanları bünyesinde bulunduran ve genel olarak veri güvenliğini sağlayan uzmanlara cryptology uzmanları denir. Yukarıda anlattığım algoritmalar sürekli güncellenmeye ve geliştirilmeye ihtiyaç duyar çünkü her zaman akıl akıldan üstündür. Tarihde öncesine baktığımız zaman nist standartı olarak kabul edilen DES algoritması şuan kullanılması tabiri caizse yasaklanmıştır. Çünkü sahip olduğu algoritma bugünkü şartlar altında çok kolay bir şekilde kırılmaktadır. Hakeza şuan kullandığımız ssl aslında zaafiyetlerinden dolayı 6 defa değiştirilerek şuan tls olarak kullandığımız hale gelmiştir. İşte bu yüzden Cryptology uzmanları şifreleme sistemleri üretir, şifreleme algoritmalarını güvenliğini test eder ve şifrelemeleri çözmeye çalışır. 

<!--
Notlar:

Kaynaklar:
https://www.mehmetince.net/crypto-101-1-merhaba-exclusive-or-xor/
https://www.youtube.com/watch?v=p__QZIxjHMk&list=PL1H1sBF1VAKU05UWhDDwl38CV4CIk7RLJ
https://www.youtube.com/watch?v=j9xht4K-MBk


lablar:
https://capturetheflag.withgoogle.com/challenges
https://www.csaw.io/csaw19archive










-->
