Alerting 

Settings > All Settings > Alerts and Reports > Manage Alerts 

![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/5f1b6e76-bb82-4fd8-8c93-9031627b3dc5)

Yeni alarm eklemek için **Manage Alert** diyoruz 

## 1. Properties
![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/b553b914-e0c8-4fcf-b53f-e86ff5540a2c)

```1- Name of Alert...   :``` alarm adınız zorunlu varsa envanteri yönetmek için kullandığınız bir kırılım ,network / system / application gibi örnek : "System - VM High CPU Usage Alert"

```2- Severity           :``` alarm ekranındaki renklendirmede kullanabilirsiniz ve alarmalrın kendi arasında bir severity durumu varsa yapınızda raporlama ve dashboardlarda daha sonra listelerken filtreleyebilirsiniz.

```3- alarm Cutom Pro... :``` alarm bildirimleri; gruplamak, filtrelemek, raporlama , dashboardlarda envanter özgü gruplamalarda kullanılır. yapınızda bu şekilde durumlar varsa custom properties oluşturum ekleyebilirsiniz. 

```4- Alert Limitat....  :``` alarm ekranında farklı gruplara ya da kişilere göre bir limitasyon uyguluyorsanız kullanabilirsiniz. 

![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/d8da4e91-9ff5-47b2-959e-5882f35c9020)

## 2. Trigger Condition
Burda sanallaştırmadan (Hyper-V, VMware,.. ) oto şekilde eklenen "virtual machine" makinalar için bir cpu kullanım alarmı oluşturmak istiyorum. 

```I want to alert on ``` kısmından  Virtual Machine 

```Warning Value Reached ``` burda orion içerisndeki  [default tresholdlar](https://documentation.solarwinds.com/en/success_center/vman/content/vman-gsg-vm-threshold.htm) ile birlikte alarm üretmek istiyorum burda  iki değer vardır Warning %80 ve Critical %90 ,değerler ve yüzdelik hesaplanır, ben warning değeri için oluşturuyorum farklı olarak "CPU Load eşit yada büyük 55" gibi bir değer ile %55' de alarma özel default treshold'ları değştirmeden de alarm üretebilirsiniz. 


## 3. Reset Condition
![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/3c85eeb1-2edb-4d9c-895e-ef700bf72ca7)

Alarmın resetlenmesi yani resolved duruma gelebilmesi için özel koşullar oluşturulabilir, genelde önerilen ile cpu memory yük durum durumlarında önerilende kullanılır. 

![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/9aede848-6d92-49bb-bffc-cbe5a09d276a)

## 4.Time Of Day
alarmı belirli günlerde ya da saatlerde kullanmak ya da kullanmamak için gerekli düzenlemer burdan yapabiliriz.  örnek  cpu alarmı mesaii saatleri içerisinde gelmesin sadece hafta sonları gelsin tarzında.

![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/fb1dfbbd-6f20-4b51-b11a-857fe31e8ac5)

## 5.Trigger Actions
alarm trigger durumda nasıl bir aksiyon almak istiyoruzu burdan düzenliyoruz.  yeni bir aksiyon oluşturabiliriz, daha önceden farklı alarmlar kullandığımız kayıtlı bir aksiyonu bu alarmla ekleyebiliriz. örnek  belirli bir kişiye mail göndermek ya da ITSM üzerinde ticket açtırmak gibi 
![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/031e7cd1-1198-4937-a342-dd5d1a7f4729)

En basit ben mail bildirimi almak istiyorum. 
![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/21e97be0-80db-428f-80d6-aa4c55e7ef4a)
![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/d477dce3-4868-4281-9ae7-51990443f717)

Messsage kısmıdna default mesajıda kullanabilirsiniz içerisinde  alert trigger time ile birlikte alarm linki gelecektir. 
ya da özelleştirmek için "Insert Variable" kısmından alarma özgü değişkenler ile birlkte alarma ait verileri de ekleyebilirisiniz. 
![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/f6d9a6f0-2331-47ad-bff0-ce49993081b3)

Ek olarak alarmla bir eskalasyon süresi ve birden fazla aksiyon eklenebilir, alarm 10 dakika içerisinde çözülmez ise ITSM'e bir ticket açtırılabilir.  
burda ServiceNow incident açtırmayı kullanıyorum demo arayüzünde sadece bu olduğu için, farklı ITSM'ler için  "Execute an External VB Script"le gerekli düzenlemler ile api konuşturup ya da mail ile de ticket açtırılabilir. 
![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/3c697704-321f-480d-a98c-2c1719e74e54)

## 6. Reset Actions
alarm durumu bittiğinde aksiyonlar eklenebilir. alarm clear oldu maili  ya da ıtsm e açtırdığınız ticketlar burdan aynı şekilde kontrol ettirebilir. 

![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/1567afc5-dcc9-4136-bc33-93d715ab144d)

## 7. Summary of Alert Configiration
Alarmla koşulları aksiyonları ve en son bu durumda anlık olarak kaç tane makinanın ekileneceği bilgisi verir. 

![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/5db28857-1593-4731-8b9c-0c42c37748b4)![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/d3410b2e-6d33-4073-a75f-f97d950775ad)


alarm koşulunda belirtilen süre sonra alarm trigger olur ve alarmlar ekranında görülür. 
![resim](https://github.com/3QU1N0X3/Solarwinds/assets/121360885/1f1b2429-088f-4ee3-b5e1-731b9ed51668)



