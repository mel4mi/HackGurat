
# Web Güvenliği:

Web application security günümüzün ve geleceğin en çok talep gören güvenlik alanlarından bir tanesidir. Çünkü artık kullandığımız bir çok uygulama, Arkasında(backend) illaki bir web sunucusu, api ortamı veya cloud ortamı bulunduruyor. Bu nedenden dolayı olası bir web zaafiyeti bir internet sitesini hacklemekten çok daha fazlası olmaya başladı. Örneklendirmek gerekirse sitedeki eksik girdi filtrelemesi olduğu zaman bir Veritabanı açığı([SQL İnjection](https://www.niobehosting.com/blog/sql-injection/)) veya kullanıcının erişimi kısıtlanmamışsa yetkisiz dosyalara ve işlemlere erişebilme imkanı([IDOR](https://www.infinitumit.com.tr/idor-insecure-direct-object-references-zafiyeti-nedir-ve-nasil-onlenir/)) gibi zaafiyetler doğurabilir.
Bu durumun farkında olan şirket ve kurumlar artık bünyelerinde siber güvenlik ekipleri oluşturmaya başladılar ve sürekli kendi sistemlerini testlere tâbi tutmaya başladılar. Fakat bu işte bilgi ne kadar önemli ise bakış açısı da o kadar önemlidir. Şirketlerin çalışanlarına ayırabilecekleri miktarlar belirli olduğu için hem işe hem eleman alımı yapmadan hemde siber güvenlik testlerini daha kalabalık bir topluluğa yaptırmak için BugBounty adında programlar yapılmaya başlandı.


## BugBounty Nedir:
Bug bounty yani ödül avcılığı, freelancer olarak herhangi bir kişinin kurumların izin verdiği servislerde(siteler, sunucular, sanal ortamlar,..) olası zaafiyetleri aramaktır ve bulduğunuz zaafiyet'in risk seviyesine göre ödül(ücret) aldığınız bir sistemdir. bu programlarda şirketin belirlediği şartlar dışına çıkalamaz ve sadece onların belirlediği yerlere güvenlik testi yapılabilir. aksi takdirde bu bir bilişim suçudur ve şirketler sizden şikayetçi olabilir(özellikle ülkemizde aktif tarama ve sonrasında yapılacak bütün işlemler bilişim suçu kabul edilmektedir.). Böyle durumların önüne geçmek için BugBounty servisi sağlayan kurumlar vardır. Bu sitelerde bir sürü şirket, bugbounty için ayırdığı bütçeler ve uymanız gereken kuralları bize gösterir ve bu siteler aracılığıyla çalışmak yasaldır.

Peki bu web security uzmanlığında ilerlemek istediniz ve ne yapmanız gerektiğinizi bilmiyorsunuz

## Nasıl Web Güvenliği Uzmanı olunur:
Web güvenliğinde bence en önemli kural okumaktır. Çünkü web teknolojisi çok karışık ve baya kapsamlı bir alandır. Bunun için web'in çalışma mantığını iyi anlamanız lazım. web mantığını anladıktan sonra web zaafiyletlerini araştırmalasınız bunun için en önemli kaynak [OWASP](https://owasp.org/www-project-top-ten/)'tır. Bu site size dünyada en çok bulunan web zaafiyetlerini gösterecektir. Bu zaafiyetleri iyi anlamanız bugbounty de baya fayda sağlayacaktır. Zaafiyetlere çalışırken pratik yapmak çok önemlidir. Bunun için benim  bildiğim 2 yol var. Bunlardan birincisi Tryhackme gibi eğitim sitelerde lablarr çözerek. İkincisi kendiniz zaafiyetli bir web sitesi oluşturup kendiniz hacklemenizdir üzerine hackledikten sonra o zaafiyeti kapatmaya çalışmak sizi çok çok öne geçirecektir.

Ben aşağıya bildiğim kaynakları ve kullanmanız gerek tooları bırakacağım umarım yararlı olur.

## En iyi türkçe kaynak:
 - [Mehmet Dursun İnce](https://www.youtube.com/watch?v=WtHnT73NaaQ&list=PLwP4ObPL5GY940XhCtAykxLxLEOKCu0nT) - Web güvenliğinde bana çok yardımı olanmuştur. Zaafiyetlerin temelini nereden geldiğini çok iyi anlatan bir hocadır. Benim için ilk başta anlaması zordu :no_mouth: sizede aynısı olursa umudunuzu kaybetmeyin alışınca her şey çok daha kolay oluyor. 

## Kaynaklar:

 - [PortSwigger](http://portswigger.net/web-security) :star: - Portswigger web güvenliği için zirveleri oynayan bir sitedir. Bu sitede web zaafiyetlerini öğrenebilir ve uygulamalı bir şekilde çalışabilirsiniz.
 - [Tryhackme](https://tryhackme.com/) - içinde farklı farklı alanlardan dersler olasa da web güvenliği için faydalı odaları vardır. Yeni başlayanlar için tavsiye edilir.
 - [HackTheBox](https://www.hackthebox.com/) - Tryhackme'den daha zordur kendi akademi kısmı olsa da daha çok pratik için kullanılabilecek sitedir.
 
 
## Toollar:
 - [Burp suite](https://portswigger.net/burp) :star: -  Web güvenliği için one man army görevi gören tooldur. Temel mantığı internette attığınız bütün paketleri yakalayarak gönlünüzde değiştirme imkanı verir
 - [Gobuster](https://www.kali.org/tools/gobuster/) - Bu tool ile web sitesinde göremediğiniz gizli dizinleri keşfetmenizi sağlar. Ayrıca subdomain taraması da yapabilirsiniz.
 - [Nmap](https://nmap.org/) - Nmap'in burda ne işi var diyebilirsiniz ama bazen başka portta çalışan web servislerinden tutun ftp gibi bazı web sitesi ile entegre servisler olabilir ve servislerin olası zaafiyetleri sizin test sürecinize fazlasıyla katkıda bulunabilir
 - [Sqlmap](https://sqlmap.org/) - Sql injection saldırısının otomatik tooludur. kullanımı kolay baya da iş görür.
 - [Wpscan](https://wpscan.com/wordpress-security-scanner) - Wordpress sitelerinde bilgi toplamaya ve zaafiyet tespiti yapmamıza yarayan tooldur.
 - [Nikto](https://github.com/sullo/nikto) - Otomatik Web zaafiyeti için test yapan tooldur.
 - [w3af](https://w3af.org/) -Otomatik Web zaafiyeti için test yapan tooldur.
 - [wafw00f](https://github.com/EnableSecurity/wafw00f) - web sitesini koruyan veya bizi engelleyen firewall'ların tespiti ve zaafiyeti için bize yardımcı olan tooldur.
