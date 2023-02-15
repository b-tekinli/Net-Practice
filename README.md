# NETPRACTICE

![net](https://geekflare.com/wp-content/uploads/2021/12/wifirouter.png)

Bu proje, nasıl ağ oluşturulur, bir ağ nasıl yapılandırılır, ağ üzerinde veri transferi nasıl yapılır ve ağ güvenliği nasıl sağlanırı anlatmayı amaçlayan bir projedir. Ağ yapılandırma, ağ protokolleri, cihaz yapılandırması, güvenlik yapılandırması gibi temel ağ konularını içerir.

***Küçük ölçekli ağları yapılandırmak için, TCP/IP adreslemenin nasıl çalıştığını anlamak gerekecektir.***


<br />


## LEVELS SOLVED
[levels](https://github.com/b-tekinli/Net-Practice/tree/main/netpractice-levels)


<br />


**Ağ Yapılandırması Nedir?**
- Ağ üzerindeki cihazların doğru bir şekilde yapılandırılması ve konfigüre edilmesi ile sağlanır. Bir ya da daha fazla cihazın bağlantısı ile oluşur ve bu cihazlar arasında veri paylaşmasını veya iletişimi sağlar.


<br />


**Ağ Protokolleri Nelerdir?**
- Bir ağ üzerindeki cihazlar arasında veri transferi yaparken kullanılan standart kurallar ve prosedürlerdir. Ağ üzerindeki cihazlar arasındaki iletişimi, veri transferini ve güvenli bir şekilde çalışmasını sağlar. 
    - Bazı işlevleri:
    	1. Veri Paketleme: Verilerin ağ üzerinde gönderilebilmesi için paketlenmesi veya bölünmesi.
    	2. Adresleme: Her bir ağ cihazının benzersiz bir IP adresine sahip olması ve bu adresleme ile verilerin yönlendirilmesi.
    	3. Veri Transferi: Verilerin ağ üzerinde güvenli ve verimli bir şekilde transfer edilmesi.
    	4. Hata Düzeltme: Verilerin ağ üzerinde gönderilirken oluşabilecek hataların düzeltilmesi.
    	5. Güvenlik: Ağ üzerindeki verilerin güvenliğinin sağlanması.

    - Ağ protokolleri arasında TCP/IP, HTTP, FTP, SMTP gibi protokoller bulnur. Her ağ protokolü belirli bir ağa uygulanması için tasarlanır ve farklı işlevlere sahiptir. Örnek olarak, HTTP ağ üzerindeki web sayfalarının görüntülenmesini sağlar, FTP ise dosya transferi için kullanılır.
    

<br />


**Cihaz Yapılandırması Nedir?**
- Cihazın fiziksel veya sanal olarak nasıl çalışması gerektiğini, nasıl bağlanması gerektiğini, hangi ayarların yapılması gerektiğini içerir.
	1. Cihaz Bağlantısı: Cihazın fiziksel ya da sanal olarak ağa bağlanması gerekir.
	2. Ayarların Yapılması: Cihazın IP adresi, alt ağ maskesi, varsa DNS sunucusu gibi ayarların yapılması gerekir. (DNS: internette bulunan web sitelerinin ve diğer hizmetlerin adreslerini kolayca kullanılabilir hale getirmek için kullanılan bir sistemdir. DNS, web sitelerinin IP adreslerini alfabetik olarak anılan domain (alan) adlarına çevirir ve bu adresleri kullanıcıların tarayıcılarına gösterir. Bu sayede kullanıcılar, domain adlarını hatırlamaya çalışmak yerine, web sitelerine direkt olarak adres girebilirler.)
	3. Güvenlik Ayarları: Cihazın güvenliğinin sağlanması için gerekli olan ayarların yapılması gerekir, örneğin parola ayarları.
	4. İşlevsel Ayarlar: Cihazın nasıl çalışması gerektiğine dair ayarların yapılması gerekir, örneğin firewall ayarları ve dosya paylaşım ayarları.
	5. Yapılandırmanın Kaydedilmesi: Ayarlar yapıldıktan sonra cihazın yapılandırmasının kaydedilmesi gerekir.


<br />


**Güvenlik duvarı yapılandırması nasıl olur?**
- Bir ağın giriş ve çıkışını kontrol eden ve güvenliğini sağlamaya yarayan bir yazılımdır. Güvenlik duvarı yapılandırması, belirli kurallar belirlenerek yapılır ve bu kurallar belirli trafiklerin ağa erişimini veya ağ dışına çıkmasını kontrol eder. Bu kurallar, belirli IP adreslerine veya hizmetlere (örneğin, HTTP veya FTP gibi) giriş yasağı, belirli IP adreslerinden gelen trafiğin bloklanması veya sadece belirli IP adreslerine güvenli bir şekilde erişim izni verilmesi gibi farklı durumları kapsayabilir. Güvenlik duvarı yapılandırmasını yapmak için bir yönetici tarafından ağın ve güvenliğin ihtiyaçlarının doğru bir şekilde anlaşılması ve güvenlik duvarı yazılımının kullanımı gereklidir.


<br />


**TCP/IP Nedir?**
- İnternet ve diğer ağlar arasında veri aktarımı için kullanılan bir standarttır. 
	TCP, verilerin doğru ve eksiksiz bir şekilde alıcıya ulaşmasını sağlar. Bu, verilerin ağ üzerinde parçalara ayrılması ve her parçanın alıcıya tek tek gönderilmesi, alıcı tarafından onaylanması ve eksik olan verilerin tekrar gönderilmesi gibi bir dizi adımı içerir.
	
	IP ise, verilerin ağ üzerinde nasıl yolculuk ettiğini belirler. Bu, verilerin belirli bir yere gönderilmesi ve belirli bir yerden başka bir yere aktarılması gibi işlemleri içerir.
	
	TCP/IP protokol grubu, internet ve diğer büyük ağlar arasında veri aktarımı için kullanılan en yaygın protokol grubudur ve bu ağların çalışması için vazgeçilmez bir öğedir.


<br />


**Adresleme Nedir?**
- Ağ üzerindeki cihazların birbirlerini tanıması ve verilerin doğru yerlere gönderilmesi için kullanılan bir yapıdır. Bu yapı, her ağ cihazına benzersiz bir adres atamasını içerir. Bu adres, IP (Internet Protocol) adresi olarak adlandırılır ve verilerin ağ üzerindeki yolculuğunu ve varış noktasını tanımlar.
  
  Ağ adresleme, ağlar arasında verilerin doğru şekilde yönlendirilmesini ve doğru alıcıya ulaşmasını sağlar. Bu, cihazlar arasındaki veri aktarımının hızlı, güvenli ve eksiksiz olmasını garantiler.
  
  Ağ adresleme, IPv4 ve IPv6 gibi farklı protokoller tarafından desteklenir ve her protokol benzersiz bir adresleme sistemi kullanır. Örneğin, IPv4 32 bitlik bir adresleme sistemi kullanırken, IPv6 128 bitlik bir adresleme sistemi kullanır.
 
 
<br />
  

**IPv4 ve IPv6 Arasındaki Farklar Nelerdir?**
    
IPv4, 32 bitlik bir adresleme sistemi kullanır ve 4 adet 8 bitlik oktetten oluşur. Bu, toplamda 2^32 (yaklaşık 4.3 milyar) benzersiz IP adresi sağlar. Ancak, giderek artan internet kullanımı nedeniyle IPv4 adres stokları tükenmeye başladı.
    
IPv6 ise 128 bitlik bir adresleme sistemi kullanır ve 8 adet 16 bitlik hextetten oluşur. Bu, toplamda 2^128 (yaklaşık 340 undecillion) benzersiz IP adresi sağlar. Bu sayı, IPv4 adres sayısından çok daha fazladır ve internet kullanımının uzun süreli büyümesi için yeterli bir stok sağlar.
    
IPv6 ayrıca IPv4'e göre daha güvenli, verimli ve skalabil bir adresleme sistemi sunar. IPv6, IPv4'e göre daha geniş bir adres alanı, daha hızlı veri transferi, daha az paket güncellemesi gereksinimi ve daha kolay yapılandırma gibi avantajlar sağlar.


<br />


**Router Nedir?**
- Ağlar üzerinde çalışan ağ protokollerini kullanarak cihazlar arasında veri yönlendirme işlemlerini yapar ve bu sayede verilerin doğru yerlere gönderilmesini sağlar.


<br />


**Switch Nedir?**
- Ağdaki tüm cihazlar arasında veri paylaşımını veya internet bağlantısını sağlamak için kullanılabilir. Switch, ağdaki cihazların MAC adreslerine göre verilerini yönlendirir ve bu sayede verilerin doğru cihaza gitmesini sağlar. Switch, ağdaki cihazlar arasındaki veri trafiğini yönetir ve ağın verimliliğini ve hızını artırır. Aynı zamanda switch, ağdaki cihazlar arasındaki güvenliği artırır ve ağın yapısını düzenler.


<br />


**Interface Nedir?**
- Cihazlar arasında veri aktarımını, mesajlaşmayı ve kullanıcıların cihazlar arasında veri görüntülemesini ve yönetmesini sağlar. 


<br />


**Ağ Maskeleme Nedir?**
- Ağ maskeleme, ağdaki bir cihazın gerçek IP adresinin gizlenmesi için kullanılan bir tekniktir. Ağ maskeleme, cihazın IP adresinin değiştirilmesini ve cihazın gerçek IP adresinin görünmez hale getirilmesini sağlar. Bu sayede cihaz daha güvenli bir şekilde internet üzerinde kullanılabilir ve cihazın IP adresi suistimal edilemez.

	Ağ maskeleme, bir ağ geçidi veya router aracılığıyla yapılabilir. Router, cihazların internet üzerindeki trafiğini yönetir ve cihazların IP adreslerini maskeleyebilir. Ağ geçidi, cihazların internet üzerindeki trafiğini yönetir ve cihazların IP adreslerini maskeleyebilir.

	Ağ maskeleme, ağın güvenliğini ve gizliliğini artırır. Aynı zamanda cihazların internet üzerindeki görünürlüklerini azaltır ve suistimallere karşı cihazları korur.


**Ağ Maskeleme Nasıl Yapılır?**
- Bu işlem ağ geçidi olarak adlandırılan bir cihaz (genellikle bir router) tarafından yapılır.

	IP adresi maskelenirken subnet mask adı verilen bir sayı dizisi kullanılır. Subnet mask, IP adresinin hangi bölümlerinin ağ kısmı (network ID) ve hangi bölümlerinin istemci kısmı (host ID) olduğunu belirtir.

	Örnek olarak, 192.161.1.1 IP adresi için, subnet mask 255.255.255.0 kullanılabilir. Bu subnet mask IP adresinin ilk 3 bölümünün ağ kısmını, son bölümünün istemci kısmını belirtir. Bu durumda, IP adresi maskelenmiş olur ve 192.161.1.0/24 olarak görünecektir.
	
	
	IP adreslerinin subnetting yapılması, belirli bir IP adresinin alt ağlar halinde bölünmesi amacıyla yapılan bir işlemdir. Bu işlemin matematiği, IP adreslerinin binary olarak ifade edilmesi ve binary bit düzeyinde masking yapılmasıdır.

	Subnet mask, IP adresinin hangi bitlerinin ağ ID'si (network identifier), hangi bitlerinin host ID'si (host identifier) olduğunu belirler. Ağ ID'si, tüm aynı alt ağdaki cihazlar arasında aynı olmalıdır ve host ID'si ise her cihazın benzersiz olmasını sağlar.

	IP adresi ve subnet mask, binary olarak AND işlemi yapılarak ağ ID'si bulunur. İşte bu noktada matematik devreye girer. IP adresinin binary formunda, subnet mask tarafından belirlenen ağ ID bitleri 1 olarak kalır ve host ID bitleri 0 olarak ayarlanır. Host ID'nin hangi bitlerinin 0 veya 1 olduğu, belirli bir alt ağa ait olduğunu gösterir.

	Bu matematiksel işlem, ağ yönetimi ve yapılandırması konularında önemlidir ve ciddi bir network yapısının planlanması, yapılandırılması ve yönetilmesinde gereklidir.
	

<br />

![subnet mask](https://github.com/b-tekinli/Net-Practice/blob/main/net2.png)

**Subnet Mask Nedir?**
- Subnet Mask, bir IP adresinin hangi bölümünün ana sistem (network) adresini ve hangi bölümünün host (end device) adresini belirlemede kullanılan bir adres maskelemesidir. Subnet Mask, 32-bit bir IP adresi için 8-bit ile 8-bitlik (yani genellikle 255.x.x.x gibi) bir adres maskelemesidir. Subnet Mask, ağdaki cihazlar arasındaki trafiği sınırlamak, büyük ağları daha küçük ağlara bölmek ve daha efektif IP adres yönetimi yapmak gibi amaçlarla kullanılır.
	  8 bit 2 de 8 kere çarpılır ve ortaya çıkan değer 255'e eşittir. 8 bitin maksimum değeri 255'dir ve 0 ile 255 arasında bir sayı ifade edebilir. Bu, ağ ve subnet maskleme gibi ağ konularında sık kullanılan bir kavramdır.
	  
	  
<br />

![subnet](https://github.com/b-tekinli/Net-Practice/blob/main/net3.png)

**Subnet Mask Nasıl Hesaplanır?**

Subnet mask, bir IP adresinin hangi bölümünün ağ kısmını, hangi bölümünün ise makine kısmını belirttiğini gösterir. Subnetting, ağdaki makinelere daha fazla sayıda IP adresi vermek için ağları daha küçük alt ağlara bölmeyi sağlar. Bu, daha fazla adres alanı sunmak için IP adreslerinin verimli bir şekilde kullanılmasını sağlar.


Subnet mask, aynı alt ağdaki IP adreslerinin benzer bir IP adres yapısına sahip olmasını sağlar. İki interface, aynı subnette bulunacaksa subnet maskleri eşleşmelidir.

Subnet maskler, bir IP adresinin hangi bölümünün subneti temsil ettiğini tanımlar. 255.255.255.224, bir IP adresinin son 5 bitini subnet numarası olarak kullanır ve 27 bit subnet numarası verir.


<br />


	!! UNUTMA: Subnet mask aslında bir IP adresi olarak ağ veya ana bilgisayar bölümünü içermez. Yalnızca bilgisayarlara belirli bir IPv4 adresinde bu bölümleri nerede arayacaklarını söyler. 
