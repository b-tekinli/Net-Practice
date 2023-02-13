# NETPRACTICE ALIŞTIRMALARINI ÇÖZME MANTIĞI

## Level 1

İlk olarak bilmemiz gerekenler;
IP adresleri ve subnet mask'ları, aygıtlar arasında ağları bölme işlevi görür. Subnet mask'ı aynı olan aygıtlar aynı alt ağa aittir ve birbirlerine direk olarak erişebilirler. Eğer subnet mask'ları farklı ise, aygıtlar farklı alt ağlarda yer alır ve birbirlerine direk olarak erişemezler. <br />
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


