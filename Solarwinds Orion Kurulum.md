# Solarwinds Orion Kurulum
---
- **Kurulum öncesi**nde mutlaka yapınızdaki cihaz sayısına ve test edeceğiniz modüle uygun sistem gereksinimlerini <a href ="https://documentation.solarwinds.com/en/success_center/orionplatform/content/core-orion-requirements-sw1916.htm">buradan </a> kontrol ederek alt yapınızı hazır ediniz.
Şimdi sözü fazla uzatmadan kurulum aşamalarına geçelim. Öncelikle ihtiyacımız olan Solarwinds ürününü indirerek işlemlere başlıyorum.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW01.jpg" height="400" width="auto">

- System Management ana sekmesi altında bulunan SAM(Server & Application Monitor) modülünü ilgili bilgileri girerek test ortamıma indiriyorum.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW02.jpg">

- Test ortamımızda Windows Server 2019 Standart ve SQL 2019 Evolution sürümleri mevcut. Solarwinds ürünleri Windows Server ürün ailesi ve MSSQL database yapıları üzerinde koşan sistemler.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW03.jpg">

- **Kurulum öncesi** en önemli hususlardan biriside sucunun System Dil ayarlarının İngilizce olması gerekmektedir. Eğer bunu Türkçe seçersek kurulum sırasında ya da sonrasında mutlaka hatalar ile karşılaşma durumumuz olacaktır.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW05.jpg">

SQL Ortamını kontrol edelim 

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW06.jpg">

- **SAM kurulunu** başlatalım.
 <img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW07.jpg">

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW08.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW10.jpg">

NET kurulumunu tamamlaması için yeniden başlatma yapacağını bildiriyor.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW11.jpg">

yeniden başlatmadan sonra kurulum devam edecektir. 

- **Setup Wizard** karşımızda, burada test ortamımızda Standart Installation ile ilerliyor olacağız.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW13.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW14.jpg">

-Burada ihtiyacımız olan modül ve ürün seçimi ekranı geliyor. Bizim yapımızda Sanallaştırma, **Sunucular** ve **Network** cihazları olması sebebi ile SAM ürününün yanında **Select Additional Products** diyerek diğer ürünlerden de seçerek Orion platformuma onları da ekliyorum.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW15.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW16.jpg">

Seçimler
- SAM (Server & Application Monitoring)
- NCM (Network Configuration Manager)
- NPM (Network Performance Monitor)
- SRM (Storage Configuration Manager)
- VM (Virtualization Manager)

OLV (Orion Log Viewer) seçimi karşımıza geliyor. Bu ürün ile Orion ortamımızdaki log izleme ve görüntüleme işlemlerini yapıyor olacağız o yüzden More Info diyerek seçimimi yapıyorum.
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW17.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW18.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW19.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW20.jpg">

İndirme işlemlerinin devamında IIS ile ilgili kurulumların yapılması için Yes diyerek bu Component’lerin kurulumlarını yapmasını sağlıyorum.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW21.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW22.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW23.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW24.jpg">

SQL Server seçim ekranı geldi. Burada yapınız büyük ise SQL sunucunuzuz ile Orion ortamınızı ayrı ayrı konumladırmak daha iyi bir seçim olacaktır. Bizim şuan ki test ortamımız olması nedeni ile SQL Server ve Orion platformumuz aynı makine üzerinde olduğu için SQL Server makinamı seçerek devam ediyorum.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW25.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW26.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW27.jpg">

SQL Server üzerinde SolarWindsOrion database için Create a new account diyerek SolarWindsOrionDatabaseUser adında yetkili bir kullanıcı oluşturuyor ve bunun parolasını vererek devam ediyorum.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW28.jpg">

Orion platformumuza hem IP adresi hem de DNS üzerinden erişebilmemiz için (All Unassigned) seçeneğini seçerek Next diyorum ve devam ediyorum.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW29.jpg">

C:\ dizini altında Solarwinds adında bir klasör olmadığını ve oluşturacağını bildiriyor. Yes diyerek kabul ediyorum.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW30.jpg">

IIS tarafında TCP binding yapacağı için Yes diyorum ve devam ediyorum.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW31.jpg">

Kurulacak olan servislerin listesini gördükten sonra Next diyerek ilerliyorum.


<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW32.jpg">

Orion Log database ile Orion kendi database aynı SQL ortamında olacak, bizim test ortamımız olduğu için bunu ayırmadan devam ediyorum. Ayrılması performans açısından önerilen bir yöntemdir.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW33.jpg">

SolarWindsOrionLog adında bir database daha oluşturuyor.


<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW34.jpg">

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW35.jpg">


<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW36.jpg">

Finish diyerek kurulumu tamamlıyorum ve Orion platformumun Login ekranının açılmasını bekliyorum.

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW37.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW38.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW39.jpg">
<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW40.jpg">

Notification ziline tıklıyorum ve 1 tane eklenmiş Node olduğunu görüntülüyorum. Bu bizim Orion kurulu olan ana sunucumuz. Kurulumdan sonra kendisini Agent kurarak izlemeye başladı bile 

<img src ="https://github.com/3QU1N0X3/Solarwinds/blob/main/assets/SW41.jpg">

