# NETPRACTICE ALIŞTIRMALARINI ÇÖZME MANTIĞI

![netpractice](https://github.com/b-tekinli/Net-Practice/blob/main/net.png)

## Level 1

İlk olarak bilmemiz gerekenler;
IP adresleri ve subnet mask'ları, aygıtlar arasında ağları bölme işlevi görür. IP adresi, aygıtın ağdaki tanımlı konumunu, subnet mask ise aygıtın hangi alt ağa ait olduğunu belirleyen bir araçtır. Bunlar birbirine bağımlıdır ve birbirini tamamlar, ancak birbirini hesaplamak mümkün değildir. Subnet mask'ı aynı olan aygıtlar aynı alt ağa aittir ve birbirlerine direkt olarak erişebilirler. Eğer subnet mask'ları farklı ise, aygıtlar farklı alt ağlarda yer alır ve birbirlerine direkt olarak erişemezler. <br />
Burada Interface A1 ve B1'in subnet mask'leri aynı olduğu için yani aynı alt ağda bulundukları için A1'in IP adresi de B1'in IP adresinin bulunduğu alt ağ ile aynı alt ağda bir IP adresi olmalıdır. Dolayısıyla eğer size verilenler

**Interface B1          <br />
IP : 104.97.23.12       <br />
Mask : 255.255.255.0    <br /> <br />
Interface A1            <br />
IP :  ?                 <br />
Mask : 255.255.255.0**  <br />

bu şekildeyse yani A1'in IP adresi soruluyorsa B1'in mask'ı ile aynı
alt ağda bulunuyorlar mı diye kontrol etmelisiniz. Eğer ikisi de aynıysa
ki burada ikisi de 255.255.255.0 subnet maskte bulnuyor bu sefer IP adreslerinde
ikisi de 104.97.23. kısmı tamamen aynı olmak zorunda. Tam olarak sayısal
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

**Interface B1            <br />
IP : 192.168.113.222      <br />
Mask : ?                  <br /> <br />
Interface A1              <br />
IP : ?                    <br />
Mask : 255.255.255.224**  <br />

Bu level için, Interface B1 Mask'ı 255.255.255.224 olmalıdır ve Interface A1 IP adresi de 192.168.113.224 - 192.168.113.254 aralığındaki bir IP adresi olmalıdır. Bu IP adres aralığı aynı alt ağdaki diğer aygıtların IP adreslerinin aralığını belirtir ve belirlenen Mask'ın network ve host kısımlarını ayırdığı IP adres aralığını tanımlar.

Aynı şekilde, Interface A1 için bir IP adresi belirlemek için, 192.168.113.192 alt ağından bir IP adresi seçebilirsiniz. Örneğin, 192.168.113.193, 192.168.113.194, 192.168.16.195 gibi. En son sayı 192 ve 222 dahil olmadan bu aralıkta olmalıdır.

Yani, Interface B1 için Mask: 255.255.255.224 ve Interface A1 için IP: 192.168.16.193 gibi bir konfigürasyon uygun olabilir.

Dİğer pratilte client D ve client C için

**Interface D1            <br />
IP : ?                    <br />
Mask : /30                <br /> <br />
Interface C1              <br />
IP : ?                    <br />
Mask : 255.255.255.252**  <br />

olarak belirtilmiş. Burada örnek olarak IP kısımlarına 127 ile başlayan IP adresleri verilmiş fakat 127 adresi özel bir IP adresidir. Bu adres, "localhost" veya "loopback" adı verilen bir aygıtın kendisiyle iletişim kurması için kullanılan bir adrestir. 127.0.0.1 bu adresin en sık kullanılan formudur ve bu aygıtın kendisiyle iletişim kurması için kullanılır. Dolayısıyla 127 sayısı verilen IP örneğini değiştirmeliyiz. Ben C1 için **12.0.0.1** D1 içinse **12.0.0.2** yazdım. 
Subnet mask kısmında ise D1'in mask'ı "/30" olarak belirtilmiş bu "/30" açıklamalı olarak bir subnet mask'ın "CIDR (Classless Inter-Domain Routing) notation"u olarak adlandırılır. /30, bir IP adresinin 4 adet baytından sadece 2 baytının subnet için kullanılabileceğini gösterir. Bu da sadece 2 adet aygıtın bu subnet içinde bulunabileceğini gösterir. /30 subnet mask, WAN bağlantıları için kullanılan küçük subnetler olarak kullanılır.


<br />


## Level 3

Bu level için verilen tüm cihazlar 1 switch'e bağlıdır. 

Interface A1                <br />
IP :  104.198.102.125       <br />
Mask :  ?                   <br /> <br />
Interface B1                <br />
IP :  ?                     <br />
Mask :  ?                   <br /> <br />
Interface C1                <br />
IP :  ?                     <br />
Mask :  255.255.255.128     <br />

Burada öncelikle hepsi aynı alt ağda olacağı için hepsinin subnet mask'ı aynı olmalıdır dolayısıyla A1 ve B1'in mask'larını da C1 gibi 255.255.255.128 yapmalıyız. Sonrasında A1'in IP adresi 104.198.102.125 olarak belirlendiğine göre B1'in IP adresini de ona en yakın 104.198.102.126 olarak ayarlayabiliriz. Aynı şekilde C1'in IP adresini de yine birbirlerine yakın IP adresi vermek adına 104.198.102.124 olarak ayarlayabiliriz.

Switch ise burada ağ trafiğini yöneterek verilerin doğru cihaza ulaşmasını sağlar ve aynı anda birden fazla cihaz arasında veri paylaşımına olanak tanır.


<br />


## Level 4

Bu level için Interface A1 ve B1 switch'e bağlıdır.

**Interface A1            <br />
IP :  94.158.114.132      <br />
Mask :  ?                 <br /> <br />
Interface B1              <br />
IP :  ?                   <br />
Mask :  ?                 <br /> <br />
Switch ise bir router'a bağlıdır ve router üzerindeki Interface'ler ise şu şekildedir:
Interface R1              <br />
IP :  ?                   <br />
Mask :  ?                 <br /> <br />
Interface R2              <br />
IP :  94.158.114.1        <br />
Mask :  255.255.255.128   <br /> <br />
Interface R3              <br />
IP :  94.158.114.244      <br />
Mask :  255.255.255.192** <br />

Burada öncelikle bilmemiz gereken konu router'ın farklı IP adreslerine sahip cihazlar arasında veri trafiğini yönlendirir ve bunu yaparken IP adresi, mask gibi faktörleri kullanır. Aynı zamanda router ve switch birbirine bağlandığında ağ genişler ve ağın farklı alt ağlara bölünmesi sağlanır. 

Burada ilk olarak tüm bilgileri verilen router'ın Interface R2 ya da Interface R3'ün IP ve mask'ına bakarak işlem yapmaya başlamamız gerekir. Ben R2 bilgilerini baz alarak yapacağım.

Interface R1'in mask'ı R2'den aldığım için 255.255.255.128 olacaktır. Interface R1 direkt olarak switch ile iletişimde olduğundan A1'in de mask'ı için R1'e yazdığımız mask'ı yazmalıyız çünkü aynı alt ağda olacaklar. Sonra A1'in IP adresi belli olduğu için R1'in IP adresine ona yakın olarak 94.158.114.129 verebiliriz. B1 de A1 ile aynı alt ağda olacağı için onun da mask'ı R1 ve A1 ile aynı olacak. IP adresi ise A1'in IP adresine yakın olsun diye yine 94.158.114.130 verebiliriz.


<br />


## Level 5

Bu levelde **routes** ve **default** kavramı ile tanışıyoruz. Route, bir veri paketinin bir ağdaki nihai hedefine ulaşması için izleyeceği yolu ifade eder. Örneğin, "default ->" ifadesi, veri paketinin varsayılan olarak ağdaki diğer ağlara yönlendirilmesi gerektiğini gösterir. Yönlendirme tablosundaki giriş, veri paketlerinin hangi IP adresine ve alt ağa ait olduğunun belirlenmesi için kullanılır. Yönlendirme tablosundaki çıkış, veri paketinin hangi ağ cihazına gönderilmesi gerektiğini gösterir.

**Interface A1            <br />
IP :  ?                   <br />
Mask :  ?                 <br />
Interface A1 : Routes --> ? ==> ? <br /> <br />
Interface B1              <br />
IP :  ?                   <br />
Mask :  ?                 <br /> 
Interface B1 : Routes --> default ==> ? <br /> <br />
Interface A1 ve B1 bir router'a bağlıdır ve router üzerindeki Interface'ler ise şu şekildedir:
Interface R1              <br />
IP :  90.15.153.126       <br />
Mask :  255.255.255.128   <br /> <br />
Interface R2              <br />
IP :  152.249.225.254     <br />
Mask :  255.255.192.0**     <br /> <br />

Burada router Interface R1 A1'e, R2 ise B1'e bağlıdır. R1'in mask'ı A1'in mask'ına eşit olmalıdır. IP adresi ise R1'in IP adresine yakın olmalıdır mesela **90.15.153.125** olabilir. Routes kısmı ise **default => 90.15.153.126** olmalıdır. Yani R1'in IP adresi ile aynı olmalıdır. B1 de aynı şekilde mask olarak R2'nin mask'ını almalı ve IP adresi olarak da R2'nin IP adresine yakın olacak şekilde **152.249.225.253** alabilir. Routes kısmı ise R2'nin IP adresini almalıdır.



