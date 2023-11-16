## HTTP - HTTPS Monitor  

Settings > All Settings > Product Specific Settings altında  SAM Settings 

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/e08559f1-adb2-416b-a47b-14d0493f8d5d)

Application Montor Templates  altında yeni bir template oluşturuyoruz. 
![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/0e74b5e8-22d6-459f-8ae4-d06c0ff42cfb)

```Pooling Frequence``` ne kadar sürede check edileceği 

```Pooling Timeout ``` Ne kadar süre cevap dönmezse down kabul edileceği 

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/87e9bc2b-876f-4f4a-a20a-7bfb6616322a)


![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/f1fbd9df-b5db-41c1-b64a-d93841acca4b)

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/9b6578a2-cb69-4ed0-87f8-31694d7fd73b)


1. ``` Credential for Monitoring: ``` izleme yapılan node üzerinde yetkili bir credential bilgisi gerekmekte. burda daha önceden yapıda kullanılan ve node'u WMI ile polling eden credential seçili. genelde orion polling engin'ler üzerinde yapılır istisnaları mevcuttur. kiritk  seçtiğimiz Polling engine eğer web url monitor etmek istiyorsak bunun için nete çıkabiliyor olması beklenir.
   
3. ```Port number ``` HTTPS için 443  HTTP için 80 portu kullanır

4. ``` URL ```    Monitor edilmek istenen URL

5. ```Host Request ```  GET - POST  ihtiyaca göre kullanılır.

6. ```Use Proxy ```   eğer polling enginlerinizi nete çıkmıyorsa bir proxy üzerinden de  monitor edilebilir, response time süresi artıcaktır, bunun için timeout değeri üzerinde düzenleme gerektirebilir.

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/2986621a-61c5-4a74-a70a-fbc5b4c25772)

```Set Test Node ``` test etmek için yapınızda monitor edilen bir suncuu ya da polling engine üzerinden test nodu set etmek gerekir.

```TEST``` ve test sonucu varsa hataları ile birlikte yoksa Succesful olarak döner, save ettikten sonra  bir alarm tanımna bağlayıp response time üzerinden özelleştirmeler ya da orion default treshold'lar ile izlenebilir. 
![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/67f310b6-88b2-4fb6-82b6-aeab1dd8eb72)
![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/bfad16fd-de1d-4f94-a002-f34ce1f1151e)

