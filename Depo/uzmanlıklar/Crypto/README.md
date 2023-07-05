
<!--
![](https://github.com/mel4mi/siber-guvenlik-ziggurat/blob/main/Depo/resimler/block.png)
# Tadilatta
-->

# Cryptology
Cryptology, Her türlü verinin kullanıldığı bugünlerde önemi gittikçe artan bir veri bakış açısıdır. Cryptology'nin genel amacı verilerin bütünlüğünü sağlamak ve verilerin yanlış kişilerin eline geçtiğinde, verilerin okunamayacak(anlaşılmayacak) hale getirilmesinidir. Örneklendirmek gerekirse, X adlı bir kullanıcının şifresi 123456 şeklinde bir veritabanında raw[yalın(gözüktüğü gibi)] saklanması, kötü niyetli bir hacker tarafından veritabanına erişildiğinde bütün kullanıcı adı ve şifrelerini rahatça okumasına yol açacaktır. Bu yüzden cryptology alanı, verileri encrypted(şifrelenmiş) biçimde saklamayı açamlar. Bir örnekle her şey daha anlaşılır olacak.

## Örnek:
![Raw tablo](/Depo/uzmanlıklar/Crypto/fotolar/ornek_veritabanı(raw).png) <br>
Yukarıdaki veritabanı örneği, kullanıcı adı ve şifre bilgilerini yalın(şifrelenmemiş) bir şekilde tutar. Bir veritabanını içindeki bilgilerin böyle yalın tutulması, veritabanını ele geçiren bir kötü niyetli kişi, verileri rahatça kullanabilir veya rahatça satabilir. Bu da bizim gibi son kullanıcılar için bir felakete yol açabilir.

![hashed tablo](/Depo/uzmanlıklar/Crypto/fotolar/ornek_veritabanı(hashed).png) <br>
Yukarıdaki tablo ise bir önceki tablonun Encrypt(şifrelenmiş) edilmiş halidir. Kötü niyetli bir hacker böyle bir veritabanına eriştiği zaman bu bilgileri kullanabilmesi için öncelikle hashlenmiş verileri kırması lazım. Bu işlem de baya bir vakit alacaktır. Aslında cryptology'nin temel amacı bu şekildedir. sahip olduğumuz veriler başka kişinin eline geçsede onu kullanamayacak hale getirilmesidir.
<br>
#
Cryptology sadece hashlemekle sınırlı değil. Şimdi ise daha derine inelim.






## Encoding
<!-- ![encode](/Depo/uzmanlıklar/Crypto/fotolar/encoding_cutted.png) <br> -->
Encoding kodlama olarak çevirebileceğimiz(bkz. tureng) çift taraflı bir veri dönüştürme işlemidir. bu tanımı açmak gerekirse encoding işlemi verinin erişilebilmesini zorlaştırmaktan ziyade kolaylaştırmayı amaçlamaktadır. Örneklendirmek gerekirse foroğraf non-ascii dediğimiz normal karakterlerden oluşmayan bir yapıdır. Biz bir fotoğrafı taşımaya çalıştığımızda veri kayıpları yaşacanağından dolayı fotoğraflarımız bozuk gelebilir. Bu yüzden non-ascii verileri başka formatlara encode ederek bu kayıpları önlemeye çalışırız.

 ### Örnek:
  ```
  Dönüştürülmemiş veri --> [Base64 Encode Algorithm] -->  RMO2bsO8xZ90w7xyw7xsbWVtacWfIHZlcmk=
  ```

  
  Aynı Şekilde dönüştürülmüş veri ilk haline çevrilebilir. Bu da encoding işlemini çift taraflı olarak tanımlamamıza sebep oluyor.


  
  ```
  RMO2bsO8xZ90w7xyw7xsbWVtacWfIHZlcmk= --> [Base64 Decode Algorithm] --> Dönüştürülmemiş veri
  ```

  Encoding işlemi sadece veri taşımakla da sınırlı değildir. ilkel şifreleme dediğimiz eskiden kullanılan verilerin güvenliğini sağlamak için kullanılan 
algoritmalar vardı fakat kırılması çok kolay olduğundan dolayı günümüzde kullanılmaktadır. örnek: ceaser şifrelemesi
 ### Deneme yapmak için:
 [Cyberchef](https://gchq.github.io/CyberChef/),
 istediğiniz encode yöntemini seçip mesajlarınızı encode edebilirsiniz.

## Encrypting



## Hashing
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
