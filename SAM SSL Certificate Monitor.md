## SAM SSL Certificate Monitor.

<img src="https://github.com/3QU1N0X3/Solarwinds/assets/121360885/0ee524ac-a337-4c6b-aade-837c2796d9a7" width="200">

Bu component ile  basit bir şekilde ssl sertifika bilgileri çekbilebilir. ve expire date dolmadan bir alarm tanımına bağlanıp  expire date is less than x date gibi bir koşul ile alarm oluşturulabilir.

```Settings > All Settings >  Product Specific Settings altında SAM Settings >  Create Template > Add Component Monitor > SSL Certificate Expiration Date Monitor```
![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/331e1a0e-6c54-456a-980b-04af7825c4b2)
![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/fc83f350-c409-4793-a088-f7b14af93731)
![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/156001d6-2f3b-41c9-9938-33d7793e0b73)
![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/68c6ed3c-136b-4c36-83be-5a9455f4e4b1)

Windows ya da linux web sunucunuzda önceden solarwinds agent kurulu olması gerekiyor. windows ortamında agentless olarak WMI ile de monitor edilebiliyor. bunun için sunucuda administrator grubunda bir credential bilgisi isteniyor.

```SET TEST NODE  :```  Web sunucusu seçilir.

```TEST : ``` Successful olduğunda ssl bilgileri görülür.  
![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/b4a7c611-bb1c-4a47-9736-54a03f15f56b)

**Test sonuçları** 
Certificate valid days left : kalan gün sayımız , alarm tanımında static value > x gün gibi bir kural ile bildirim oluşturabilir.

![image](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/4f160ec5-a8ca-4c39-bd28-2b2a6dfaa2b4)


