## File Change Monitor
Bu component ile dosya üzerinde bir değişlik yapılıp yapılmadığını tespit edebiliyoruz. bu  durumun tespiti için dosyanın 


- ```File Path  :``` Kontrol gerçekleştireceğimiz dosya yolunu buraya giriyoruz
- ```Select and Upload : ``` burda dosyayı gözat diyerek yüklüyoruz ve update checksum yapıyoruz. dosyayı orion sunucumuza update ediyor ve 1 saatlık aralıklar ile upload ettiğimiz ddosya checksum ile path'deki dosya checksum karşılaştırıyor eğer fakrlılık yoksa Componnet Status up durumda kalıyor farklılık yakalarsa down duruma geçiyor.

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/b0913842-35c8-4e1e-8541-1cfdd4685daa)

 Burda upload ettiğimiz dosya ve path'deki dosya aynı  ve component status UP 

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/12a4ebb2-d036-4525-b01b-8303a6be16db)

Şimdi dosyayı açıyorum ve içerisinde birşeyler karalayıp kaydediyorum burda üzerine yazdırmıyor fakrlı bir lokasyona kaydedip üzerine daha sonra üzerine yazdırıyorum.  
![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/765ef53a-e7f5-4f51-b3d2-ba3a4db78b20)

 Dosya kontrolünü sağlanması için 1 saat beklemeyip  Poll Now diyorum ve test gerçekleşiyor. 
![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/c8c26b84-1931-47c5-8848-1331baeb6198)

Sonrasında dosya farklıkları olduğu için component down duruma geliyor. 

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/0ed8eb84-9c5f-4ea4-b115-3a8bfb5c2579)
