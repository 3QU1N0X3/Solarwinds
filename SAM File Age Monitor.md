## SAM File Age Monitor

Bu component ile herhangi bir dosyanın son değiştirilme tarihi izlenebilmekte, örnek bir bir log dosyasına belirli periyotlarla yazılan veriler aksaklığa uğraması durumu tespit edilebilmekte. 
output value değeri saatlik olarak gelmekte, ve kurgulayacağınız alarmı buna göre x saatten büyükse gibi yapıalbilir. 

```Settings > All Settings > Product Specific Settings altında SAM Settings > Application Montor Templates >  Create a New Template > Add Component > File Age Monitor ```

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/e8588550-0012-40c8-accd-f68a3848650e)

Örnek bir kurguda saatlik log tutulan bir yapımız olsun ve  FileAge.txt dosyasına yazsın **burda önemli nokta ayrı bir dosya oluşturulmuyor bütün işlem tek bir dosya üzerinden yapılıyor sürekli bu dosya güncelleniyor.** 
eğer herhangi bir saat aralığında dosya yazma işlemi gerçekleşmezse kurgu bunu yakalayacak ve  alarm üretecek. 


![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/a08d1ddf-47b1-468f-b81a-33bea86d51c5)

Kaydederken zaten bu şekilde bildirimde vermekte. 

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/7722aaa9-e4c7-4674-a1b7-278e39a1c15d)

ve alarm ekranında aşağıdaki gibi alarm üretilmekte. 

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/b3a87af8-b514-4cab-a392-1bae36be5a03)
