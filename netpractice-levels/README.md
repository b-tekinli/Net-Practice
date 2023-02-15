# NETPRACTICE ALIŞTIRMALARINI ÇÖZME MANTIĞI

![netpractice](https://github.com/b-tekinli/Net-Practice/blob/main/net.png)

## Level 1

İlk olarak bilmemiz gerekenler;
IP adresleri ve subnet mask'ları, aygıtlar arasında ağları bölme işlevi görür. IP adresi, aygıtın ağdaki tanımlı konumunu, subnet mask ise aygıtın hangi alt ağa ait olduğunu belirleyen bir araçtır. Bunlar birbirine bağımlıdır ve birbirini tamamlar, ancak birbirini hesaplamak mümkün değildir. Subnet mask'ı aynı olan aygıtlar aynı alt ağa aittir ve birbirlerine direkt olarak erişebilirler. Eğer subnet mask'ları farklı ise, aygıtlar farklı alt ağlarda yer alır ve birbirlerine direkt olarak erişemezler. <br />
Burada Interface A1 ve B1'in subnet mask'leri aynı olduğu için yani aynı alt ağda bulundukları için A1'in IP adresi de B1'in IP adresinin bulunduğu alt ağ ile aynı alt ağda bir IP adresi olmalıdır. Dolayısıyla 

![level1](https://github.com/b-tekinli/Net-Practice/blob/main/level-assets/level1.png)

A1'in IP adresi soruluyorsa B1'in mask'ı ile aynı alt ağda bulunuyorlar mı diye kontrol etmelisiniz. Eğer ikisi de aynıysa ki burada ikisi de 255.255.255.0 subnet maskte bulnuyor bu sefer IP adreslerinde ikisi de 104.97.23. kısmı tamamen aynı olmak zorunda. Tam olarak sayısal
hesaplama yapmadan 0 ile 255 arasında bir sayı verdiğinizde doğru sonuç alacaksınız. **--> 104.97.23.1**

Fakat bu sayı 0 ile 255 arasında olmak zorunda ama 0 ve 255 dahil değil. Bu sayıları girmeyi denediğimizde **KO** sonucunu alırız yani 1 ve 254 dahil ve bu sayılar aralığında bir sayı girersek **OK** sonucunu alırız. Örn: **--> 104.97.23.254** bu sayıyı girdiğimizde de **OK** sonucunu alırız.

### Peki neden 0 ile 255 dahil değil?
0 ve 255 network ve broadcast adresleri olarak kullanılır ve makinelere atanmaz. <br />
***Network adresi,*** ağın tanımlanması için kullanılır. <br />
***Broadcast adresi*** ise ağdaki tüm makinelere aynı anda veri göndermek için kullanılır. 
Dolayısıyla bu adresler atanmazlar, çünkü makinelere atandıklarında yanıt vermeleri ve veri almaları beklenemez.

Bunlar dışında dikkat etmemiz gereken diğer bir husus ise Interface B1'in IP adresi ile aynı olursa **KO** alırız. Bu örnekte B1'in IP adresi'nin sonunda 12 sayısı olduğu için A1'in IP adresinin sonuna (sadece bu örnekte olmak üzere) 12 girdiğimizde **KO** alırız.

Eğer sayısal hesaplama yapmak istersek olaya şu şekilde bakabiliriz: aynı alt ağdaki aygıtların IP adreslerinin ilk n biti aynı olmalıdır.

#### İlk n biti aynı olmalıdır derken ne demek istiyorum?
Örneğin, bir aygıtın IP adresi: 192.168.1.100 ve subnet maskı 255.255.255.0 ise, bu aygıtın IP adresinin ilk 24 biti "192.168.1."dir. Bunun anlamı, bu aygıtla aynı alt ağda olan diğer tüm aygıtların IP adreslerinin de "192.168.1." ile başlaması gerektiğidir. Örneğin, diğer bir aygıtın IP adresi 192.168.1.101 olabilecektir.

Buna göre diğer örneği de kendiniz yapabilirsiniz.


<br />


## Level 2

İlk olarak burada bilmemiz gerekenler;
Subnet mask'ının nasıl hesaplanacağı, ağın ihtiyaçlarına göre belirlenir. Eğer ağdaki aygıtlar arasında içsel bir iletişim ihtiyacı varsa, ağı oluşturan aygıtların subnet mask'ları aynı olmalıdır. Bu durumda, ağı oluşturan aygıtların IP adreslerinin ilk n biti aynı olmalıdır.

Eğer ağdaki aygıtlar arasında dışarıya açılan bağlantılar için bir sınırlama olması gerektiği varsa, subnet mask'ları farklı olabilir. Bu durumda, ağı oluşturan aygıtların IP adreslerinin ilk n biti farklı olabilir.

Eğer subnet mask'ı belirsiz ise, IP adreslerine bakarak subnet mask'ı hesaplamak mümkün değildir. Bu durumda, ağ yöneticisi ya da sistem yöneticisi tarafından belirlenmelidir.

![level2](https://github.com/b-tekinli/Net-Practice/blob/main/level-assets/level2.png)

Bu level için, Interface B1 Mask'ı 255.255.255.224 olmalıdır ve Interface A1 IP adresi de 192.168.113.222 adresine yakın bir IP adresi olmalıdır. Bu IP adres aralığı aynı alt ağdaki diğer aygıtların IP adreslerinin aralığını belirtir ve belirlenen Mask'ın network ve host kısımlarını ayırdığı IP adres aralığını tanımlar.

Yani, Interface B1 için Mask: 255.255.255.224 ve Interface A1 için IP: 192.168.113.221 gibi bir konfigürasyon uygun olabilir.

Dİğer pratikte client D ve client C için örnek olarak IP kısımlarına 127 ile başlayan IP adresleri verilmiş fakat 127 adresi özel bir IP adresidir. Bu adres, "localhost" veya "loopback" adı verilen bir aygıtın kendisiyle iletişim kurması için kullanılan bir adrestir. 127.0.0.1 bu adresin en sık kullanılan formudur ve bu aygıtın kendisiyle iletişim kurması için kullanılır. Dolayısıyla 127 sayısı verilen IP örneğini değiştirmeliyiz. 
Subnet mask kısmında ise D1'in mask'ı "/30" olarak belirtilmiş bu "/30" açıklamalı olarak bir subnet mask'ın "CIDR (Classless Inter-Domain Routing) notation'u olarak adlandırılır. /30, bir IP adresinin 4 adet baytından sadece 2 baytının subnet için kullanılabileceğini gösterir. Bu da sadece 2 adet aygıtın bu subnet içinde bulunabileceğini gösterir. /30 subnet mask, WAN bağlantıları için kullanılan küçük subnetler olarak kullanılır.


<br />


## Level 3

Bu level için verilen tüm cihazlar 1 switch'e bağlıdır. Switch burada ağ trafiğini yöneterek verilerin doğru cihaza ulaşmasını sağlar ve aynı anda birden fazla cihaz arasında veri paylaşımına olanak tanır.

![level3](https://github.com/b-tekinli/Net-Practice/blob/main/level-assets/level3.png)

Burada öncelikle hepsi aynı alt ağda olacağı için hepsinin subnet mask'ı aynı olmalıdır dolayısıyla A1 ve B1'in mask'larını da C1 gibi 255.255.255.128 yapmalıyız. Sonrasında A1'in IP adresi 104.198.102.125 olarak belirlendiğine göre B1'in IP adresini de ona en yakın 104.198.102.126 olarak ayarlayabiliriz. Aynı şekilde C1'in IP adresini de yine birbirlerine yakın IP adresi vermek adına 104.198.102.124 olarak ayarlayabiliriz.


<br />


## Level 4

Bu level için Interface A1 ve B1 switch'e bağlıdır.

![level4](https://github.com/b-tekinli/Net-Practice/blob/main/level-assets/level4.png)

Burada öncelikle bilmemiz gereken konu router'ın farklı IP adreslerine sahip cihazlar arasında veri trafiğini yönlendirmesi ve bunu yaparken IP adresi, mask gibi faktörleri kullanır. Aynı zamanda router ve switch birbirine bağlandığında ağ genişler ve ağın farklı alt ağlara bölünmesi sağlanır. 

Burada ilk olarak tüm bilgileri verilen router'ın Interface R2 ya da Interface R3'ün IP ve mask'ına bakarak işlem yapmaya başlamamız gerekir. Ben R2 bilgilerini baz alarak yapacağım.

Interface R1'in mask'ı R2'yi baz aldığım için 255.255.255.128 olacaktır. Interface R1 direkt olarak switch ile iletişimde olduğundan A1'in de mask'ı için R1'e yazdığımız mask'ı yazmalıyız çünkü aynı alt ağda olacaklar. Sonra A1'in IP adresi belli olduğu için R1'in IP adresine ona yakın olarak 94.158.114.130 verebiliriz. B1 de A1 ile aynı alt ağda olacağı için onun da mask'ı R1 ve A1 ile aynı olacak. IP adresi ise A1'in IP adresine yakın olsun diye yine 94.158.114.131 verebiliriz.


<br />


## Level 5

Bu levelde **routes** ve **default** kavramı ile tanışıyoruz. Route, bir veri paketinin bir ağdaki nihai hedefine ulaşması için izleyeceği yolu ifade eder. Örneğin, "default ->" ifadesi, veri paketinin varsayılan olarak ağdaki diğer ağlara yönlendirilmesi gerektiğini gösterir. Yönlendirme tablosundaki giriş, veri paketlerinin hangi IP adresine ve alt ağa ait olduğunun belirlenmesi için kullanılır. Yönlendirme tablosundaki çıkış, veri paketinin hangi ağ cihazına gönderilmesi gerektiğini gösterir.

![level5](https://github.com/b-tekinli/Net-Practice/blob/main/level-assets/level5.png)

Burada router Interface R1 A1'e, R2 ise B1'e bağlıdır. R1'in mask'ı A1'in mask'ına eşit olmalıdır. IP adresi ise R1'in IP adresine yakın olmalıdır mesela **90.15.153.125** olabilir. Routes kısmı ise **default => 90.15.153.126** olmalıdır. Yani R1'in IP adresi ile aynı olmalıdır sebebi ise ona yönlendirme yapmalıdır. B1 de aynı şekilde mask olarak R2'nin mask'ını almalı ve IP adresi olarak da R2'nin IP adresine yakın olacak şekilde **152.249.225.253** alabilir. Routes kısmı ise R2'nin IP adresini almalıdır.


<br />


## Level 6

Burada internet router'ın internet bağlantısını sağlar ve router R1 internet bağlantısından gelen paketleri ağ içindeki switch'e bağlı Interface A1'e paketleri yönlendirir.

Default route, internet'e erişim için kullanılan en son yolu belirtir. "0.0.0.0/0" adresi de aynı şeyi ifade eder ve bu nedenle de "default route" olarak adlandırılır. Bir network tarafından internet'e ulaşmak için kullanılacak yolun belirlendiği yerde default route tanımlanır ve belirtilen yol default gateway olarak adlandırılır. Default gateway, verilerin internet'e ulaşması için gerekli olan diğer networklere yönlendirilmesi için kullanılır.

![level6](https://github.com/b-tekinli/Net-Practice/blob/main/level-assets/level6.png)

Bu level özelinde ilk olarak A1 mask'ı R1 mask'ı ile aynı olmak zorundadır. R1 IP adresi ise A1 IP adresine yakın olmalıdır. Client A routes default ve R1 IP adresini almalıdır. Router routes ise default almalıdır. Geriye sadece internet routes kalıyor o da --> **112.129.164.0/24** almalıdır. Alternatif olarak 112.129.164.0/24 yerine 0.0.0.0/0 gibi bir adres yazabilirsiniz. 0.0.0.0/0, tüm IP adreslerini kapsayan bir adrestir ve "default route" olarak da adlandırılır. Bu adres, sistemde tanımlı hiçbir başka rota bulunmadığında tüm paketlerin gönderilmesini gerektiren bir "catch-all" adresdir.


<br />


## Level 7

Burada 2 router birbirine bağlandığından aralarında veri akışı sağlanabilir. 

![level7](https://github.com/b-tekinli/Net-Practice/blob/main/level-assets/level7.png)

Öncelikle Client A routes kısmında default kısmı aynı kalarak IP kısmı R11'in IP adresini almalı. A1'in IP kısmı ise R11'e en yakın olan IP adresi **114.198.14.2** olabilir. Mask ise kendimiz belirleyebiliriz ben önceki levellerde gördüğüm kadarıyla **255.255.2.55.128** yapıyorum. Böylelikle R11 ve A1 mask'ları bu adresi alabilir. R1 routes kısmında ise yine default kısmı sabit kalabilir fakat IP kısmı R21'in IP adresini almalı. Onu da R12'den yola çıkarak **114.198.14.253** olarak en yakın IP'yi verebiliriz. R12 mask'ı ise farklı olmalı diğer bir router üzerinden bağlanacağı için. Yine önceki levellerden gördüğüm kadarıyla **255.255.255.252** yaptım. Buna bağlı olarak R21 mask'ı da aynı olmalı. Sonrasında R22 IP adresi R1 alt ağında olacağı için **114.198.14.150** yaptım. Mask olarak ise **255.255.255.192** belirledim. C1'in mask'ı da buna bağlı olarak aynı mask'ı almalı. C1 IP adresi ise R22 ile yakın olmak zorunda olduğundan  **114.198.14.151** olarak tanımladım. R2 routes default kısmı sabit kalıp IP ksımı R12 IP adresini almalı. Client C ise rotues kısmında default kısmı sabit kalmalı ve IP kısmı ise R22 IP adresini almalıdır.


<br />


## Level 8

Burada bir router üzerinde 2 fealt ve routes girişi bulunmaktadır. Her bir default ve routes girişi, router tarafından yönetilen aygıtlardan birine gönderilen verilerin hangi IP adresine gitmesi gerektiğini belirler.

![level8](https://github.com/b-tekinli/Net-Practice/blob/main/level-assets/level8.png)

Burada Internet ağının routes kısmında verilen IP'yi direkt olarak R1 routes kısmına yazabiliriz ve Internet ağının IP kısmmına R12 IP adresini yazmalıyız. R1'in IP kısmına ise default kısmına yakın bir IP verebiliriz. R13 ise yine R1 IP'sinin en yakını olarak **139.209.40.62** alabilir. D1'in ve R12'nin mask'ı **255.255.255.240** olduğundan diğer tüm aygıtların da maskları aynı olabilir. R2 routes default kısmı sabit kalmalı IP'si ise belli olduğundan C1 IP adresine **139.209.40.18** vermeyi tercih ettim. R22 IP adresine de C1 ile veri alışverişi yapacağı için ve aynı alt ağda olmaları gerektiğinden ona en yakın olan **139.209.40.17** adresini verdim. Client C ise default kısmı sabit kalmalı IP adresi ise R22 IP adresini almalı. R23 IP adresine de yine yakın bir IP vermek için **139.209.40.1** verdim. Bu IP adresi aynı zamanda Client D'nin default kısmı sabit kalarak IP kısmına yazılmalıdır. D1 IP adresine ise R23'e yakın olması için **139.209.40.2** verebiliriz. 


<br />


## Level 9

Bu levelde diğer levellerden farklı olarak bir internetin 3 farklı routes'ı olması karşımıza çıkıyor. Bir internetin üç tane routes'ı olması, bu internetin farklı yollarla farklı ağlara erişebileceği anlamına gelir. Router'lar, bir ağa erişmek için birden fazla yolu kullanabilirler ve her yol farklı bir route ile belirtilir. İnternet üzerindeki ağlar ve cihazlar, route tablosunu kullanarak hedef ağlara ulaşmak için hangi yolun kullanılacağını belirlerler. Bir internetin üç farklı routes'ı olması, farklı gateway'ler aracılığıyla farklı ağlara erişebileceği anlamına gelir.
Gateway ise bir ağdaki cihazların başka bir ağa erişmesini sağlayan bir ağ cihazıdır. Yani aslında router'ın diğer adı gateway diyebiliriz. 









