# Temel Network Eğitimleri Notlarım

Network iki veya daha fazla cihazın kaynaklarını paylaşmak maksadıyla birbirine bağlanmasıdır. Bu kaynaklar yazılımsal (bir belge, dosya yada herhangi bir yazılım olabilir) yada donanımsal (bir yazıcı olabilir) olabilir.

İki bilgisayar herhangi bir şekilde bilgi alışverişi yapabiliyorsa biz bu iki bilgisayarın birbirine bağlı olduğunu, aynı ağda olduğunu söyleyebiliriz. Bağlantı bir bakır tel üzerinde yapılması gerekmez bağlantı için fiber optik, kablolar mikrodalgalar ve iletişim uydularıda kullanılabilmektedir. 

Sistemler iletişim için tek bir protokol kullanmazlar. Bunun yerine, protokol ailesi ya da diğer bir deyişle protokol takımı kullanırlar. Popüler iletişim protokolleri örnekleri: OSI, GSM, GPRS, TCP/IP, HTTP veya ISDN olabilir.

## Network Tarihçesi

Bugün bilinen bilgisayar ağlarının temelini 1970'lerin başında geliştirilen Arpanet oluşturmuştur. Arpanet gelişerek interneti meydana getirmiştir. İnternet pek çok farklı tasarıma sahip birbirinden bağımsız ağların varlığı fikrine dayanır. Paket anahtarlamalı bir ağ olan arpanet ile başlayan süreç daha sonra paket uydu ağları, yer tabanlı paket radyo ağları ve diğer ağlar ile devam etmiştir. Bugün ki internet açık mimarili ağ adı verilen bir kavrama dayanır. Bu yaklaşıma göre herhangi bir ağ teknolojisinin seçimi, özel bir ağ mimarisi ile sınırlanamaz. Kullanıcı tarafından serbestçe seçilebilir ve diğer teknolojilerede uygun hale getirilir.

İnternet dünya çapında yüzmilyonlarca bilgisayarı birbirine bağlayan bir ağ ağıdır. İnternetin sahibi kim? *hiçkimse*

Ortak standartları kullanarak bilgi alışverişinde bulunmak için birbirine bağlı ağların tümüdür.

İlk bilgisayarın icadindan kısa bir süre sonra bilgisayar ağları hakkında çalışmalar başlamış ve internetin temelini oluşturmuştur. Uzak mesafelerdeki iki bilgisayarı birbirine bağlamanın en eski ve ilk akla gelen yolu bu bilgisayarlar arasında kiralık bir hat kurmaktır
İki bilgisayar arasında kiralık bir hat kurarken kullanılan iki teknik, <mark>Devre Anahtarlama</mark> ve <mark>Paket Anahtarlama</mark>'dır.

<div style="display: flex;justify-content: space-between; margin-right: 75px; margin-left: 75px">
<div style="width:500px">

paket anahtarlama => veri küçük boyutlarda paketlere ayrılarak ve bu paketler ara noktolarda bekletilerek yeterli kapasite boşluğu olduğu anda bir sonraki noktaya iletilmesi prensibine dayalı olarak çalışır.
![image-1](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/0cee5e68-71cc-406e-88f3-b455e2cb9879)


devre anahtarlama => kaynak ile hedef arasında belli olan yolu sadece o kaynak kullanır diğerleri kullanamaz bu da band genişliğinde verimsizliğe sebep olur. Ses ve görüntü gibi realtime uygulamalar için uygundur.
![image (1)xxxx](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/e51dbf74-2d4d-4a90-ab90-0c1f958fe213)
</div>
</div>

## Network Türleri (LAN, WAN, MAN, WLAN)

- <strong>LAN (Local Area Network)</strong>
- <strong>WAN (Wide Area Network)</strong>
    LAN ların birbirine bağlanması sonucu oluşturulan geniş ağlardır. En büyük WAN internettir.
- <strong>MAN (Metropolitan Area Network)</strong>
    Kısaca geniş alana yayılmış LAN dır.
- <strong>WLAN (Wireless Local Area Network)</strong>

Günümüzde alt yapı değişikliği yapmadan, LAN lar sanallaştırılıp birden çok virtual LAN lar oluşturulabiliyor.

Küçük ev ağları birkaç bilgisayarı birbirine ve internete bağlar.
Small Office / Home Office (SOHO) ağı bir ev ofisindeki veya uzak ofisteki bilgisayarların bir şirket ağına bağlanmasına veya merkezi paylaşan kaynaklara erişmesine olanak tanır.
Şirketler ve okullar tarafından kullanılan orta ve büyük ağlar ise yüzlerce yada binlerce birbirine bağlı ana bilgisayarlara sahip bir çok konuma sahip olabilir.

![image-3](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/9a59af3e-9471-458a-96dd-7f362a54e653)

![image-4](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/07be6e44-7d7b-4882-9a9e-065d445c3fbf)


> Network Topolojisi nedir? : Bir networkü oluşturan cihazların nasıl yerleştirileceğini bağlanacağını ve veri iletiminin nasıl olacağını belirleyen genel bir yapıdır.

>> Fiziksel topoloji : network cihazlarının kabloların veya uç cihazlarının nasıl düzenlenmesi gerektiğini belirliyor. 

>> Mantıksal topoloji : networkdeki veri akışının nasıl olacağını belirliyor.

![image-2](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/310c7e9d-0c55-473a-bc66-2e136ddcc385)



## Network İletişim çeşitleri

- <strong>unicast</strong>
    networkde bir cihazdan başka bir cihaza bire bir iletim.
- <strong>broadcast</strong>
    Bir cihaz aynı subnet içerisindeki yada tüm netwrokdeki cihazlara iletim. Veri tüm cihazlar ile ilgili olsun olmasın hepsine gönderiliyor. Router, switch gibi cihazlar tarafından broadcast bloklanabilir yada kısıtlanabilir. IPv6 broadcast iletişimi desteklemez, bunun yerice multicast kullanılır. ARP protokolünde broadcast yaparak MAC adresleri öğreniliyor. Yine DHCP protokolündede broadcast kullanıyor.
- <strong>multicast</strong>
    veri belirli bir grup cihaza gönderilir

## HTTP - HTTPS

### HTTP yani (Hyper Text Transfer Protokol)
- Network üzerinden web sayfalarının görüntülenmesini sağlıyor
- 80 portunu kullanıyor
- uygulama katmanında çalışıyor
- web tarayıcıları ile kullanılıyor
- web tarayıcıları kullanılarak client tarafından, server tarafına http protokolü kullanılarak istek gönderilir. Server tarafı bu isteğe Apache, IIS gibi web sunucu programları tarafından bu isteğe cevap verilir. Böylelikle web sitesine girmiş oluyoruz
### HTTPS yani Secure HTTP
- iletişim TLS (Transport layer security) veya SSL (secure sockets layer)ile şifreleniyor. Günümüzde artık ssl yerini tls ye bırakıyor.
- 443'üncü port kullanılıyor
- asıl amacı güvenli olmayan bir iletişim ağı üzerinden güvenli bir kanal oluşturmak
- eskiden https sadece yüksek güvenlik gerektiren uygulamalarda kullamılırken günümüzde web sitelerinin tümünde http den daha sık kullanılıyor

## FTP - TFTP

### File Transfer Protocol (FTP)

- iki bilgisayar arasında dosya transferini sağlayan bir protokol
- server - client mantığı ile çalışıyor, ftp yapabilmek için bibilgisayarda ftp client diğerinde, ftp server olmalı. Client olarak terminal veya web browser kullanılabiliyor. Ayrıca ftp server olarakda kullanılan programların istemci özelliğide kullanılabiliyor. Örneğin FileZilla programı hem server hemde istemci olarak kullanılabilir. FTP yapmak için bağlanmak istenilen cihazın ip adresi, ve .. kullanıcı adı ve şifresinin bilinmesi yeterli oluyor.
- Test için oluşturulmuş ftp servera bağlanıp oradan dosya indirelim

![d1](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/102ce262-b320-4a3d-8552-76b1f63f5b83)

![d2](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/2903085e-bc52-4f89-8050-9683fa389da9)


### Trival FTP

- Aynı şekilde dosya transeri için kullanılıyor
- UDP 69 portunu kullanıyor
- Daha hızlı, basit fakat güvensiz bir protokol
- Çoğu ftp özelliklerini barındırmıyor, ftp deki gibi dizinleri listeleme kullanıcı kimlik doğrulaması gibi özellikleri yok. Sadece okuyor ve uzak bir sunucuya yazabiliyor.
- Basit yapısından ötürü kullanımında çok az bellek kullanıyor bu nedenle daha çok yeterli belleği olmayan router gibi switch gibi cihazların ön yüklemesinden kullanılıyor.

## Network'te kullanılan Temel Cihazlar

Uç cihazlar client lar (laptop, pc, printer, telefon, tablet) ve serverlardır (web server, file server)
Google gibi büyük şirketler serverlarını server farm denilen birden fazla serverın birleştirildiği data centerlardan bu hizmetlerini sağlıyorlar
Aynı LANda bulunan cihazlar birbirleri ile haberleşebilmek için <mark>switch</mark> kullanabilirler. Switch günümüzde hem hub yerine hemde bridge yerine maliyet, performans ve güvenlik gibi nedenlerle daha çok kullanılıyor.
Kendisine gelen veriyi MAC adresine göre porta gönderir. Layer2 yada layer3 de çalışabilir. Multi layer olabilir.
Kendisine gelen broadcastleri tüm portlarına gönderir (tıpkı bridge gibi). Hub ise ne gelirse gelsin tüm portlara gönderiyor
<mark>ROUTER</mark>, Farklı LANların birbirleriyle router kullanarak haberleşebilir. Kısaca routerlar LANları WANlara bağlar
Layer 3 de çalışır
Networkler arası IP adreslerine göre yönlendirme yapar, switch cihazların MAC adreslerine göre yapıyordu
Router broadcast geçirmez (özel bir yapılandırılma yapılmadıkça)
<mark>Firewall, IDS, IPS</mark> gibi cihazlar istenmeyen trafiği önlemek için routerların önlerinde arkalarında konumlandırılabiliyorlar. Siber saldırılar için bu şekilde önlemler alınabiliyor
Firewall önceden belirlenmiş güvenlik kurallarına göre networke gelen giden trafiği izleyen ve kontrol eden donanım ve yazılım tabanlı network güvenlik sistemidir. IP filtreleme, Port filtreleme, web filtreleme, içerik filtreleme gibi birçok farklı türde filtreleme yapabiliyor
Programsal olarakda donanımsal olarakda firewallar mevcut
Genellikle güvenli bir iç network ile internet gibi güvenilir olmayan bir dış network arasında uygulanıyor.

![image-8](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/c892fcad-a2f4-416f-87c1-78868f3f36c8)


<mark>Network interface card</mark>, cihazlara ilk network bağlantısının yapıldığı kart kısaca (NIC) yada Ethernet kartı, network kartı, ağ arabirim kartı vs gibi farklı isimlendirilebiliyor.
Bilgisayarlarla ağın iletişim kurmasını sağlayan, ağa fiziksel olarak bağlanan ağ arabirim kartı (NIC)  dır
<mark>kablo ve konektörler</mark>, network cihazlarını birbirine bağlayan ara bağlantı elemanları, uzak mesafeler için yoğunluklu olarak fiber optik kablolar kullanılıyor. Kopmalar durumda, wireless olarak noktadan noktaya iletim sağlanabiliyor
kablo ile ethernet kartının bağlanmasını sağlayan aparatlar konnektörlerdir

port ve arayüz aynı anlamda kullanılabiliyor.

<mark>hub</mark>, kendisine gelen sinyallerin güçlendirilip yeniden oluşturulmasını ve zamanlanmasını sağlar. Kendisine gelen tüm sinyalleri, verinin geldiği port hariç tüm portlarına gönderir
OSI de katman 1 de çalışır.
mantıksal topolojisi bus topolojisidir, fiziksel topolojisi yıldız topolojisidir
Hub yerine günümüzde daha çok switchler kullanılıyor
switche göre daha yavaş, hub veri hızınu portlar arasında paylaşıyor
Wierless cihazlarda tıpkı hub mantıgında çalışıyor
tüm portları aynı collision domaindedir
Kısaca çok portlu bir tekrarlayıcıdır
<mark>bridge</mark>, aynı protokolü kullanan iki veya daha fazla bağımsız networkü birbirine bağlamak için kullanılan network cihazıdır
OSI modelinde ikinci katmanda çalışır (data link katmanı)
topolojiden öğrenmiş oldugu MAC adresi tablosuna göre verileri gönderir
tüm portları farklı collision domaindedir
network trafiğini azaltmak için kullanılsada, broadcast trafiğini engelleyemiyor
hubdan daha hızlı, switchten daha yavaştır. Yönlendirme işlemini switch ile aynı mantıkta yapsada bu işlemi yazılımsal olarak yapar, switch donanımsal olarak yapar. Switchte her cihaz için ayrılmış bir port vardır. Daha yavaş olmasının sebebi donanımsal değil yazılımsal yapmasıdır.

<mark>access point</mark> kablosuz erişim için kullanılır
birden çok cihazı networke bağlar
Sadece kablolu bağlantıyı kablosuza çevirmek için kullanılsada birçoğunda repeater özelliğide oldugundan kablosuz ağ sinyallerini güçlendirmek içinde kullanılıyor.
WLC ile aynı lan daki 100lerce access point tekbir noktadan yönetilibiliyor
<mark>modem</mark> MOdulasyon ve DEModulasyon işlemleri yapıyor.
Modulasyon, sayısal veriyi analog veriye dönüştürme işlemi
Demodulasyon, analog veriyi tekrar sayısal veriye dönüştürme işlemi
internet servis sağlayıcınızın altyapısından evinize interneti getirmesini yarar. Evinize en yakın kaynaktan evinizin içine kablo çekilir (Fiber ya da DSL) ve modeme takılır. Modem de bu interneti Ethernet kablosu ile bir bilgisayara ya da router cihazına dağıtır.
Evlerimizde genelde içerisinde hem modem hemde router görevini yapan cihazlar kullanılıyor. Bu sayede donanım fazlalığından kurtulmuş oluyoruz.
ADSL, VDSL ve Kablo modemleri çeşitleri vardır. ADSL modemler günümüzde en çok tercih edilen modem türüdür. VDSL modemler ise daha yüksek hızda internet erişim imkanı sunarlar. Kısacası her şekilde internete bağlanmak için bir modeme ihtiyacınız var. Bu durumun istisnası olarak internet altyapısı olmayan bölgelerde kullanılan taşınabilir internet hizmetidir. Modem tek başına sadece tek bir cihazı internete bağlayabilir. Daha fazla cihazı internete bağlamak için router’lara ihtiyaç vardır.




## IP Adresi

Network cihazlarını tanımlamak için kullanılan her bir cihaz için benzersiz bir sayısal değerdir. IPv4 42 bit, IPv6 128 bitdir
Yönetici tarafından değiştirilebilir. OSI modelinde 3. katman protokolüdür, connectionless (bağlantısız) bir protokoldür. Paketin hedefe ulaşmasını garanti etmez.
IPv4 32bitten oluşur, decimal olarak yazılır. (örn 192.168.5.18)

![image-9](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/6b25acb3-43c5-48da-8b23-de468f73efdc)

herbir 8 bitlik kısma oktet adı verilir

> <mark><strong>MAC için ip adresini görüntüleme</strong></mark>
```BASH
# Finding Local IP
ipconfig getifaddr en0
ipconfig getifaddr en1
ifconfig | grep inet

# Finding Global/External IP
curl ipecho.net/plain ; echo
curl ifconfig.me
```
> <mark><strong>Linux için ip adresini görüntüleme</strong></mark>
```BASH
# Finding Local IP

# Finding Global/External IP

```

ip adresinin formatı
IP adresi network ve host kısmı olmak üzere iki bölümden oluşur, kaç bitinin networkü kaç bitinin hostu temsil ettiğini subnet mask belirler
Router network adresine göre yönlendirme yapar
Host adresi networkdeki uç cihazı tanımlıyor

### IPv4 IP adreslerinin sınıfları

1) > Sınıf A IP adresi: ilk bayt 0 - 127 arasındadır 
<strong>devlet kurumları tarafından kullanılır</strong>
kullanılabilir kısım: 1.0.0.0 ~ 126.155.255.255
kullanılabilir kısmın daraltılmış olmasının iki sebebi;
    > 1) 127.0.0.1 ayrılmış bir adres olup, genellikle geri döngü adresi için kullanılır, (loopback) 
    > 2) Deafault gateway olarak ayrıldıgı için [0.0.0.0 - 0.255.255.255] aralığı kullanılamaz
2) > Sınıf B IP adresi: ilk bayt 128 - 192 arasındadır (128.0.0.0 ~ 191.255.255.255)
<strong>orta ölçekli işletmelere tahsis edilir</strong>
3) > Sınıf C IP adresi: ilk bayt 192 - 223 arasındadır (192.0.0.0 ~ 223.255.255.255)
<strong>serbestçe atanabilir</strong>
3) > Sınıf D IP adresi: ilk bayt 224 - 239 arasındadır (224.0.0.1 ~ 239.255.255.254)
<strong>multicast</strong>
3) > Sınıf E IP adresi: ilk bayt 240 - 255 arasındadır (240.0.0.1 ~ 255.255.255.254
<strong>bilimsel faliyetler için kullanılır</strong>

genel olarak
- A - B ve C sınıfları unicast için,
- D çok noktaya yayın (multicast) için,
- E denemeye ayrılmıştır, bilimsel faliyetler için kullanılır

Aslında burda verilen adres aralıkları CIDR ile yerdeğiştirecek,
CIDR ile herhangi bir adres alanı farklı adres bloklarına bölünebiliyor

### CIDR
<strong> Classless inter domain routing - Sınıfsız alanlar arası yönlendirme </strong>

Genel ip adresi atama yöntemlerinden birisi
- amacı genel ipv4 adreslerinin tükenmesi ile başa çıkmak
- internet routerlarında yönlendirme tablolarının büyümesini yavaşlatmak

<strong>VLSM - varible length subnet mask</strong>
vlsm yöntemiyle ip adreslerinin standart sub.masklarını alt networklere bölünerek gerekli olan büyüklükte network elde edilebiliyor, verim arttırılabiliyor.
ayrıca /24 şeklindeki gösterimede CIDR ile geçildi

CIDR dan önce ip aralıkları aşağıdaki gibi 3 sınıfa ayrılmıştı ???

<img width="766" alt="xx" src="https://github.com/mtalhaaygen/Net-Practice/assets/63591196/3635cefd-c7d0-49ec-ad4a-ca32df546c82">


### IPv4 ayrılmış adreslerin listesi

Özel ip adresleri localde kullanılabilir fakat internete yönlendirilemiyor, internet servis sağlayıcıları tarafından bu ip adresleri bloklanıyor. 

[Subnet Mask Cheat Sheet](https://www.aelius.com/njh/subnet_sheet.html)
[127.0.0.0 nedir?](https://tr.ipshu.com/ipv4/127.0.0.0)

IPv4 ayrılmış adresleri:

| adres bloğu | Adres aralığı | Adres sayısı | Kapsam | Açıklama |
|-------------|---------------|--------------|--------|----------|
| 0.0.0.0/8	| 0.0.0.0–0.255.255.255	| 16,777,216 | Yazılım | Geçerli ağ (yalnızca kaynak adres olarak geçerlidir). 
| 10.0.0.0/8 | 10.0.0.0–10.255.255.255 | 16,777,216 | Özel ağ | Özel bir ağ içindeki yerel iletişim için kullanılır.
| 100.64.0.0/10 | 100.64.0.0–100.127.255.255 | 4,194,304 | Özel ağ | Operatör düzeyinde bir NAT kullanırken bir servis sağlayıcı ve aboneleri arasındaki iletişim için paylaşılan adres alanı.
| 127.0.0.0/8 | 127.0.0.0–127.255.255.255 | 16,777,216 | Sunucu | Network cihazlarının kendilerini test etmeleri için kullanılıyor
| 169.254.0.0/16 | 169.254.0.0–169.254.255.255 | 65,536 | alt Ağ | Normalde bir DHCP sunucusundan alınacak gibi bir IP adresi belirtilmediğinde, tek bir bağlantıda iki ana bilgisayar arasındaki bağlantı yerel adresleri için kullanılır.
| 172.16.0.0/12 | 172.16.0.0–172.31.255.255 | 1,048,576 | Özel ağ | Özel bir ağ içindeki yerel iletişim için kullanılır.
| 192.0.0.0/24 | 192.0.0.0–192.0.0.255 | 256 | Özel ağ | IETF Protokol Atamaları.
| 192.0.2.0/24 | 192.0.2.0–192.0.2.255 | 256 | belgeleme | TEST-NET-1, dokümantasyon ve örnekler olarak atandı.
| 192.88.99.0/24 | 192.88.99.0–192.88.99.255 | 256 | Internet | Ayrılmış. IPv6 - IPv4 rölesi (IPv6 adres bloğu 2002 :: / 16 dahil).
| 192.168.0.0/16 | 192.168.0.0–192.168.255.255 | 65,536 | Özel ağ | Özel bir ağ içindeki yerel iletişim için kullanılır.
| 198.18.0.0/15 | 198.18.0.0–198.19.255.255 | 131,072 | Özel ağ | İki ayrı alt ağ arasındaki ağlar arası iletişimin karşılaştırmalı testi için kullanılır.
| 198.51.100.0/24 | 198.51.100.0–198.51.100.255 | 256 | belgeleme | TEST-NET-2, dokümantasyon ve örnekler olarak atandı.
| 203.0.113.0/24 | 203.0.113.0–203.0.113.255 | 256 | belgeleme | TEST-NET-3, dokümantasyon ve örnekler olarak atandı.
| 224.0.0.0/4 | 224.0.0.0–239.255.255.255 | 268,435,456 | Internet | IP çok noktaya yayın için kullanılır. (Eski D Sınıfı ağ).
| 240.0.0.0/4 | 240.0.0.0–255.255.255.254 | 268,435,455 | Internet | Gelecekte kullanılmak üzere rezerve edilmiştir. (Eski E Sınıfı ağ).
| 255.255.255.255/32 | 255.255.255.255 | 1 | alt Ağ | "Sınırlı yayın" hedef adresi için ayrılmıştır.

## IP Subnetting

IP Subnetting (Alt ağları bölme)
IPv4 adreslerini daha verimli kullanmak, broadcast trafiğini azaltmak, networkü daha kolay yönetmek ve güvenliğini sağlamak için subnetting işlemine ihtiyaç duyuyoruz.

Subnet Mask; bir ip adresinin hangi network'te olduğunun belirlenmesi için kullanılan bir adres. 32bitten oluşur ve tıpkı ipv4 bir ip adresi gibi yazılır. Bir ip adresninin hangi bölümünün network hangi bölümünün host olduğunu subnetmask sayesinde öğrenebiliyoruz

![image-10](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/af88f5c6-5c8d-4992-8731-97f6a647c91b)


subnetmaskelar IP ile birlikte gösterileceği zaman 1 sayıları yanlarına / işareti ile eklenir. Yukarıdaki görselde subnetmasklar CIDR gösterimle sırasıyla /8, /16 ve /24 şeklinde ifade edilebilir.

Bize bir ip adresi ve bu ipnin subnetmaskı verildiğinde network, broadcast adresleri, networkte kullanılabilir ilk ve son IP adreslerini bulabiliriz.
> Not: local broadcast address ve directed broadcast address olmak üzere iki çeşit broadcast adres var. Local broadcast adresi herzaman 255.255.255.255 dir aynı anda yerel network üzerindeki tüm cihazlara veri göndermek için kullanılıyor. Routerlar local broadcast geçirmiyor. Directed olan ise bizim hesaplayacağımız olan belirli bir networkte tüm cihazlara veri gönderirken kullanılacak olan address dir. Normalde directed broadcastte routerlardan geçmiyor ama gerekli yapılandırma yapılarak geçirtilebilir

### Subnet Mask kullanılarak IP bilgileri edinme

Bu başlık altında subnet mask kullanarak bir IP adresinin network, broadcast adresleri, networkte kullanılabilir ilk ve son IP adreslerini nasıl bulundugunu inceleyeceğiz Bir ip adresinin network, broadcast adreslerini bildiğimizde o networkte kullanabileceğimiz ipleride bilmiş oluyoruz.

```MARKDOWN
# yöntem 1: binary kullanarak bulmak
1- ip adresinin network ve host kısımlarını ayır
2- network adresini bulmak için ip adresinin host kısmını sıfır yap
3- broadcast adresini bulmak için ip adresinin host kısmını 255 yap
4- networkde kullanılabilen ilk ve son adresi belirle. host kısmı 1 yaparsan ilk adres, 254 yaparsan son adres
```

 192.168.1.10 /24 ip ve subnetmaska sahip bir network için
bu ipnin ilk üç okteti networkü son okteti ise hostu ifade ediyor
> <strong>network kısmı</strong> 192.168.1.
> <strong>host kısmı</strong> .10

Burada hostu 0 yaparak network adresini bulmuş oluyoruz, aynı şekilde broadcast adresini bulmak içinde host kısmını 255 yapıyoruz
> <strong>network adresi</strong> 192.168.1.0
> <strong>broadcast adresi</strong> 192.168.1.255

> <strong>networkde kullanılabilir ilk adres</strong> 192.168.1.1
> <strong>networkde kullanılabilir son adres</strong> 192.168.1.254

Daha karmaşık bir ip ve subnetmask ikilisine bakalım
IP; 165.72.83.194 /19

subnetmask ifadesine gerek duyarsak 255.255.224.0 dır 
11111111.11111111.11100000.00000000

ipnin bir tık binary gösterimi 165.72.01010011.194
> network kısmı 165.72.010
> host kısmı 10011.194
> <strong>network adresi</strong> 165.72.64.0
> <strong>broadcast adresi</strong> 165.72.95.255
> <strong>networkde kullanılabilir ilk adres</strong> 165.72.64.1
> <strong>networkde kullanılabilir son adres</strong> 165.72.95.254

Yine bir örnek
IP; 87.121.165.49 /14
network kısmı 87.\*\*\**** => 87.011110
host kısmı **.165.49 => 01.165.49

netwrok adresi 87.120.0.0
broadcast adresi 87.123.255.255
kullanılabilir olan
ilk adres 87.120.0.1
son adres 87.123.255.254

```MARKDOWN
# yöntem 2: kolay yöntem
yukarıda yapılan işlemler tablo ile yapılır
```

83 => 01010111

165.72.010   10111.194

165.72.64.0   &rarr; 165.72.64.1
165.72.95.255 &rarr; 165.72.95.254

![image-11](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/0f82e612-d42f-45e8-92cd-5b5e11a6969f)


IP; 87.121.165.49 /14

tabloya bakarak hızlıca
255.252.0.0 subnet mask olur, (neden 252 cünkü network kısmı ilk oktetin tamamı ve ikinci oktetin ilk 6 biti bu 6 bitin 1 olması durumunda değer 252 oluyor)

0 - 4 - 8 ... - 120 - 124 (neden 4er çünkü 252 nin tablodaki karşılığı)
121 sayısı 120-124 aralığında

87.120.0.0      &rarr; 87.120.0.1 
87.123.255.255 &rarr; 87.123.255.254

### Subnetting işlemi (Alt ağlara bölme)

Bu işlem ihtiyaç duyulan host sayısına yani kullanıcı sayısına göre yada ihtiyaç duyulan alt network sayısına göre yapılabilir

Bu işlem host bitlerinden alıp network bitlerine aktarma yaparak gerçekleştirilir.
İhtiyaçlar şu şekilde hesaplanır;

> <br> <strong>network ihtiyacı için</strong>
burda $n$ hosttan networke kaç tane bit aktaracağımızı ifade eder
$Formül = 2^n$
<br>
> <strong>host ihtiyacı için</strong>
burda $n$ host tarafında kalacal bit sayısını ifade eder
$Formül = 2^n - 2$
hangi ihtiyaca göre subnetting yapacaksak o formülü kullanıyoruz, -2 nin amacı network ve broadcast adreslerini çıkarmaktır
<br>

12 kişilik bir departman için 

![image-12](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/c6d23dbe-ddc8-4297-a95c-499719bc0f74)

şeklinde alt ağ oluşturulabilir. (14 kişi kapasiteli oldu)
subnetmask = 255.255.255.240 şeklinde oldu
14er kişilil alt networklerimizi alt alta yazarsak;

![image-13](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/9dbe857d-920e-4598-ab7b-f6ff1f222b24)


## TCP / IP Protokolleri

![tcpipProtokelleri](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/5c11ef7f-2be4-4a6c-a2ba-fcf2f7deade4)

## OSI

OSI Modeli sadece bir standarttır. Eskiden olduğu gibi isteyen kendi başına bir ağ iletişim modeli geliştirebilir. Ancak OSI modeli referans alınmadıysa diğer ağlarla iletişimi zor olacak değişik üreticiler bu ağ sistemi için donanım ve yazılım üretemeyecekler demektir. OSI referans modeli bilgisayar ağlarında iletişim ortamından (kablolu, kablosuz) kullanıcıya kadar olan işlemleri 7 katmana ayırmıştır.

<img width="1049" alt="osi" src="https://github.com/mtalhaaygen/Net-Practice/assets/63591196/dad39b20-7d94-4835-ac36-2830ff202817">

1) Fiziksel Katman
Fiziksel katman veri parçacıklarının (bit) kablo, fiber, hava gibi iletim ortamlarında nasıl iletileceğini tanımlar. Gönderen tarafta fiziksel katman 1 ve 0’ları bir iletim ortamının anlayacağı şekle (elektrik sinyali , radyo sinyali, ışık) gönderir, alıcı tarafta fiziksel katman iletim ortamından okuduğu bu sinyalleri tekrar 1 ve 0 haline getirir. Farklı üreticilerin ağ donanımlarının birbirleri ile sorunsuz iletişim kurmaları için, giden gelen veri bitlerinin farklı marka donanımları için aynı şeyi ifade etmesi gerekmektedir. Diğer bir ifadeyle belirli standartların oluşturulması, aynı protokollerin kullanılması lazımdır. Kullanılan standartlardan bazıları şunlardır;

* EIA/TIA-232
* EIA/TIA-449
* V.24
* RJ45
* FDDI
* V.35
* Ethernet
* NRZ
* B8ZS
* GBIC/SFP

2) Veri Bağı Katmanı
Bu katman, kaynaktan gönderilen verinin çerçeve (frame) haline getirilerek hedef adresine iletilmesini sağlar. Her bir network kartında benzersiz olarak bulunan 48 bitlik MAC adresini kullanır. Veri paketinde bulunan kaynak ve hedef MAC adresleri ile haberleşmenin doğru yapılmasını sağlar. Bu katmanda kullanılan bazı protokoller şunlardır; 

* IEEE 802.3/802.2
* HDLC
* Frame Relay
* PPP
* FDDI
* ATM
* CSMA/CD
* CSMA/CA

3) Ağ Katmanı 
Bu katman ağ adresi (IP adress) verinin kaynaktan hedefe ulaşmasını sağlar. Ağ ortamında veriyi yönlendiren yönlendiriciler (router) ve yönlendirme algoritmaları bu katmanda çalışır. Bu katmanda kullanılan protokollerden bazıları şunlardır;

* IP
* IPX
* AppleTalk DDP
* ARP
* RARP
* ICMP
* RIP
* EIGRP

4) İletim Katmanı
Bu katmanın iki önemli protokolü TCP (transmission control protocol) ve UDP (user datagram protocol) dir. Her ikisinin de farklı kullanım alanları ve amaçları vardır. TCP'nin UDP'den tek farkı veri akışının karşı tarafa ulaşıp ulaşmadığını kontrol eder. Bundan dolayı TCP UDP'ye göre daha yavaştır ancak güvenirlilik sağlar. 
Dosya aktarımları, web sayfası indirmeleri, e-posta iletişimi gibi uygulamalarda TCP kullanılır. Bu tür uygulamalar güvenilirlik ve veri bütünlüğü gerektirir. Video akışları, ses iletimi, oyunlar gibi uygulamalarda ise UDP kullanılır. Bu tür uygulamalar, hız ve anlık veri iletimi önemlidir, ancak veri kaybı toleranslıdır.
![tcp vs udp](https://www.karel.com.tr/sites/default/files/pictures/tcp-ve-udp-farklari.jpg)
Her uygulama için farklı farklı tanımlanan port adresleri bu katmanın önemli bileşenlerinden biridir. Örneğin internet için bu katmanda port 80 olarak belirlenir. 
Ports 20 and 21: File Transfer Protocol (FTP). FTP is for transferring files between a client and a server.
Port 22: Secure Shell (SSH). SSH is one of many tunneling protocols that create secure network connections.
Port 25: Historically, Simple Mail Transfer Protocol (SMTP). SMTP is used for email.
Port 53: Domain Name System (DNS). DNS is an essential process for the modern Internet; it matches human-readable domain names to machine-readable IP addresses, enabling users to load websites and applications without memorizing a long list of IP addresses.
Port 80: Hypertext Transfer Protocol (HTTP). HTTP is the protocol that makes the World Wide Web possible.
Port 123: Network Time Protocol (NTP). NTP allows computer clocks to sync with each other, a process that is essential for encryption.
Port 179: Border Gateway Protocol (BGP). BGP is essential for establishing efficient routes between the large networks that make up the Internet (these large networks are called autonomous systems). Autonomous systems use BGP to broadcast which IP addresses they control.
Port 443: HTTP Secure (HTTPS). HTTPS is the secure and encrypted version of HTTP. All HTTPS web traffic goes to port 443. Network services that use HTTPS for encryption, such as DNS over HTTPS, also connect at this port.
Port 500: Internet Security Association and Key Management Protocol (ISAKMP), which is part of the process of setting up secure IPsec connections.
Port 587: Modern, secure SMTP that uses encryption.
Port 3389: Remote Desktop Protocol (RDP). RDP enables users to remotely connect to their desktop computers from another device.
Bu katmanda kullanılan önemli protokoller şunlardır:
* TCP
* UDP
* SPX
* RTP
* SIP
* H.323



5) Oturum Katmanı: Bu katman, kaynak ve hedef arasında iletişimi başlatır yönetir ve sonlandırır. İstemcide kullanılan her bir ağ bağlantısı örneğin e-mail, web browser, ftp gibi her bir uygulama ayrı bir oturum açarak verilerin birbirlerine karışması engellenir. Bu katmanda çalışan  protokoller ve servisler aşağıda verilmiştir:

* Sockets
* RPC
* Netbios
* NFS
* SIP
* SDP
* AppleTalk ASP
* SQL

6) Sunum Katmanı: Ağ ortamında PC’ler arası paylaşılan verinin anlamlı olması bu katman sayesindedir. Paylaşılan bilginin PC’ler tarafından da okunabilmesi için verinin ortak bir formata dönüştürülmesi gerekmektedir. Paylaşımda bulunan bilgisayarların farklı yazılımlarla yönetildiğini düşündüğünüzde bu işlevin önemi anlaşılmaktadır. Böylece farklı programların birbirlerinin verisini kullanabilmesi mümkün olur. Sunum katmanının en önemli görevlerinden biri, paylaşılan verinin karşı bilgisayara şifreli olarak iletebilmesidir. Aslında Sunum katmanı ağ ile pek ilgili olmayıp, yazılımlarla alakalıdır. Günümüzde işletim sistemleri oluşturulan birçok formatı okuyamaz. Yani başka bir kullanıcıdan bize gelen bir veri formatını işletim sistemimiz desteklemiyorsa o bilgi bizim için hiçbir şey ifade etmez. Örnek olarak, günümüzdeki internet ortamında paylaşılan divx formatındaki videoları izleyebilmek için bilgisayarlarda destekleyici Codec programlarının olması şarttır. Bir bilgisayarın diğeri üzerindeki bir divx dosyasını açması sırasında sunum katmanına bir iş düşmez, burada kastedilen şey, aynı formatı çözebilen yazılımları ve programları kullanmaktır. Kullandığımız formatların bazıları şunlardır;

* GIF
* DIVX
* DOC
* ASCII
* EBCDIC
* TIFF
* JPEG
* PICT
* MPEG
* MIDI

7) Uygulama Katmanı: Bu katman, kullanıcıların ve programların ağı kullanabilmesi için araçlar sunar. Uygulama katmanı son katman olduğundan diğer katmanlara herhangi bir hizmet sunmaz. Çalıştırılan uygulamalar için ağ hizmetlerini oluşturur. Microsoft API’leri bu katmanda çalışır. Microsoft API’leri kullanarak program yapan bir yazılımcı, örneğin bir ağ sürücüsüne erişmek gerektiğinde API içindeki hazır aracı alıp kendi programında kullanır. Alt katmanlarda gerçekleşen onlarca farklı işlemin hiçbirisiyle uğraşmak zorunda kalmaz. Mesela diğer bir örnek HTTP’dir. HTTP program değil, kurallar dizesi olan bir protokoldür. Bu protokole göre işlev gören bir Internet Explorer, aynı protokolü kullanan başka Web sunuculara bağlanır. Ayrıca bu katman iletişim kuracağı bilgisayarın iletişime hazır olup olmadığını tespit eder, iletişimi senkronize eder. Kullanılan uygulama ve protokollerden bazıları şunlardır;

* Telnet
* http
* web browser
* NFS
* FaceBook
* ftp
* SNMP
* SMTP gateway

> TCP/IP 4 katman içeren osi benzeri bir model, içerisinde tcp, ip ve çok daha fazla protokolü barındırıyor
### OSI vs TCP/IP

* tcp/ip de gerek duyulmayan katmanlar kullanılmayabiliyor, oside böyle bir esneklik yok
* tcp/ip de katmanlar arasına yeni bir protokol kolay yerleştirilebiliyor fakat oside katmanların görevleri katı şekilde belirlenmiş
* oside veriye her bir katmanda encapsulation ve decapsulation işlemleriyle yeni bilgiler eklenir yada çıkartılır
  <img width="1205" alt="capsulation" src="https://github.com/mtalhaaygen/Net-Practice/assets/63591196/11ac634f-e7c7-4385-8647-477e3c78ec80">
* osi 7 katmandan, tcp/ip 4 katmandan oluşuyor
* osi deki fiziksel katman ve datalink katmanı tcp/ip de birleştirilmiş ve link katmanı olarak adlandırılmış
* aynı şekilde sunum, oturum ve uygulama katmanları tcp/ip modelinde uygulama katmanına karşılık geliyor
* bu iki modelin mix hali TCP/IP yeni versiyonu olarak 5 katman olarak belirlenmiş ve günümüzde en çok bu 5 katmnalı model kullanılıyor

<br>
<br>
<br>

## statik routing

![image](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/682953a9-ff58-46b8-98bb-7a36c416d55c)




## Birtakım Sorular

### Default Gateway (Ağ geçidi) Nedir?
Eğer x bir ip adresine sahip cihaza veri göndermek istenirse subnetmaska göre x ip adresinin kendi ağında olup olmadığına bakılıyor eğer değilse default gateway adresi ile router a yönlendiriliyor

### TCP nerelerde kullanılır
Gelişmiş bilgisayar ağlarında paket anahtarlamalı bilgisayar iletişiminde kayıpsız veri gönderimi sağlayabilmek için TCP protokolü yazılmıştır. HTTP, HTTPS, POP3, SSH, SMTP, Telnet ve FTP gibi internetin kullanıcı açısından en popüler protokollerinin veri iletimi TCP vasıtasıyla yapılır. 

### Intranet nedir?
İntranet, bir kuruluşun veya şirketin içinde kullanılan özel bir ağdır. Bu ağ, genellikle şirket içi iletişimi, bilgi paylaşımını, işbirliğini ve iç kaynaklara erişimi kolaylaştırmak için tasarlanmıştır. İnternet gibi genel erişime açık değildir ve sadece belirli bir kuruluşun çalışanları veya üyeleri tarafından kullanılabilir.

### Extranet nedir? 
Şirket çalışanlarının dışarı dışarısı ile iş birliği ve iletişimini sağlayan özel iş ağı Intranetlere benzer
![x20-24-07](https://github.com/mtalhaaygen/Net-Practice/assets/63591196/3941995e-ab27-4696-a3de-2ebb44420ec5)

### Man-in-the-middle saldırısı nedir?
Man-in-the-middle saldırısı kısaca MITM; saldırganın birbiri ile doğrudan iletişim kuran iki taraf arasındaki iletişimi gizlice ilettiği veya değiştirdiği saldırı türüdür. İletişim ağı üzerinde veri paketleri serbestçe dolaşır. Özellikle broadcast olarak salınan paketler, aynı ağa bağlı tüm cihazlar tarafından görülebilir. İlkesel olarak hedefinde kendi IP'si olmayan bir paketi alan makinelerin, bu paketlerle ilgili herhangi bir işlem yapmamaları gerekir. Ancak istenirse bu paketlere müdahale edebilir ya da içeriğini öğrenebilirler. Aradaki adam saldırısı ağ üzerindeki paketleri yakalayarak manipüle etmek olarak özetlenebilir.

### Switch - Hub nedir?
Hub, bilgisayarları birbirine bağlayan merkezi birleştirme cihazıdır. Verileri Hub kendine bağlı tüm bilgisayarlara gönderir. Veriyi alması gereken tek bilgisayar olması halinde diğer kendine bağlı bilgisayarlara da veri yolladığı için onları da meşgul eder. Bu yüzden Hublar Switch lere göre performans olarak daha zayıftır.

Switch ise, her bir veriyi iletim kanalına ayrı bir yol bulan cihazlardır. Sadece istenilen bilgisayarlara veri gönderir. MAC adreslerini bilen Switch’ler verileri portlar aracılığı ile aktarmak istediğiniz bilgisayara kolayca aktarmanızı sağlar. Portlarına hangi cihaz bağlı ise hepsine ayrı bir yol hazırlar. Görev olarak hub le aynıdır, fakat performans ve hız olarak hub dan daha hızlıdır. Switch kendine gelen verinin hangi adrese gideceğine bakar o veriyi gönderen ve alacak olan arasında bir bağlantı kurup diğer bilgisayarların haberi olmadan ve onları meşgul etmeden iletir.

### NAT nedir?
NAT (Network Address Translation), Türkçe’deki anlamıyla Ağ Adresi Dönüştürme, TCP/IP ağındaki bir bilgisayarın yönlendirme cihazı ile başka bir ağa çıkarken adres uzayındaki bir IP ile yeniden haritalandırma yaparak IP paket başlığındaki ağ adres bilgisini değiştirme sürecidir.

NAT, aynı ağ içerisinde bulunan birden fazla cihazın aynı public IP’yi kullanarak internete erişebilmesini sağlayan bir yöntemdir. Bu sayede birden fazla cihaz aynı internete bağlanır ve bu sayede farklı IP adreslerine gerek kalmaz.

NAT, IP’den IP’ye dönüşüm yapmaktadır dolayısıyla public IP sayısı yeterli olsa bile NAT, servislerin sunulduğu sunucuları dış dünyadan soyutlamak amacı ile de kullanılabilir. Örneğin web sunucu olarak internete açmak istediğimiz bir sunucuyu elimizdeki public IP’lerden biri üzerinden açmak yerine ona bir yerel ağ IP adresi vererek NAT üzerinden public IP’yi yerel IP’ye yönlendirebiliriz. Böylece yerel ağdaki değişikliklerden NAT dönüşümü yapıldığı sürece dış dünyanın haberdar olması gerekmez.

### Proxy server nedir?
Proxy sunucusu, Türkçe’deki anlamıyla vekil sunucu, internet üzerinde bir web sitesini görüntülemek istediğimizde doğrudan değil, bir ara sunucu aracılığıyla ulaşılmak istenilen bilginin bir kopyasını size farklı bir pencere üzerinden yeniden gösterilmesi gibi düşünülebilir.

Tarayıcı üzerinden proxy sunucusu kullanarak bir internet sitesine bağlanmamız, bizim doğrudan değil de, bir köprü aracılığıyla siteye eriştiğimiz anlamına gelmektedir. Araya bir ek bağlantı daha sağlanıp biz bir proxy sunucusuna istek gönderiyoruz. Proxy ise erişmek istediğimiz yerde ki bilgiyi alıyor ve ardından bize gösteriyor.

Proxy sunucular güvenliğiniz için sanal ortamda bir güvenlik katmanı oluşturur. Bir web sitesine Proxy sunucusu ile ziyaret ederseniz o web sayfasına sizin adınıza girer ve web içeriklerini size aktarır.

Proxy kullanarak engellenmiş sitelere girebilir, internette daha hızlı ve güvenli dolaşabilirsiniz. Bazı Proxy’lerin amacı internette kimliği gizlemekten ziyade filtreleme/zararlı sitelere girişi engelleme ya da bant genişliğinden tasarruf ederek veri akışını hızlandırmaktır.

