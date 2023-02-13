## Level 1

Burada Interface A1 ve B1'in subnet mask'leri aynı olduğu için
yani aynı alt ağda bulundukları için A1'in IP adresi de
B1'in IP adresinin bulunduğu alt ağ ile aynı alt ağda
bir IP adresi olmalıdır. Dolayısıyla eğer size verilenler

**Interface B1          <br />
IP : 104.97.23.12       <br />
Mask : 255.255.255.0    <br /> <br />
Interface A1            <br />
IP :  ?                 <br />
Mask : 255.255.255.0**  <br />

bu şekildeyse yani A1'in IP adresi soruluyorsa B1'in mask'ı ile aynı
alt ağda bulunuyorlar mı diye kontrol etmelisiniz. Eğer ikisi de aynıysa
ki burada ikisi de 255.255.255.0 adresinde bulnuyor bu sefer IP adreslerinde
ikisi de 104.97.23. kısmı tamamen aynı olmak zorunda. Tam olarak sayısal
hesaplama yapmadan direkt B1'in IP adresinin sonu 12 olduğu için ona yakın
bir sayı vermek adına 1 ya da 2 gibi sayılar verdiğinizde doğru sonuç alacaksınız. **--> 104.97.23.1**

Buna göre diğer örneği de kendiniz yapabilirsiniz.

<br />
