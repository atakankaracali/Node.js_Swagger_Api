# Node.js_Swagger_Api
Node.js ile Swagger kullanarak API Dokumantasyon Example
![swagger](https://user-images.githubusercontent.com/53658645/129714110-0c868de6-6ade-4cb6-a584-bdd3ac57d8d3.PNG)
Swagger Kullanarak Node.js İle API Dökümantasyonunda İşlemler
![ng1](https://user-images.githubusercontent.com/53658645/129714178-9164cdeb-3b0a-476f-919d-60472f677332.PNG)
İşlemler Bu şekildedir
![ng2](https://user-images.githubusercontent.com/53658645/129714207-edff4370-c5a9-4fb4-9290-18c7659cbc07.PNG)
Get ve Post Görünümü
![ng3](https://user-images.githubusercontent.com/53658645/129714264-d108dd16-d76a-489f-a9fb-db3a3c98ecb7.PNG)

Update ve Delete Görünümü

200 OK
Gönderilen isteğin başarılı bir şekilde görevini yerine getirdiğini ifade eder. Body’de döndürülecek olan şeyler isteğe göre değişir. Eğer GET isteği gönderildiyse istenen resource body’de, HEAD isteği gönderildiyse istenen bilgiler header’da, POST isteği gönderildiyse yapılan işlemin sonucu gönderilir.

201 Created
Client’ın isteğiyle bir resource yaratıldıysa 201 kodu döndürülür. Burada önemli olan iki nokta vardır. Resource yaratılmadan önce 201 döndürülmez. Eğer bu işlem uzun sürecekse 202 Accepted kodu döndürülür.

202 Accepted
Client’ın gönderdiği isteğin yerine getirilmesi zaman alacaksa ve asenkron olara devam edecekse 202 döndürülür. Fakat bu kod işlem yerine getirildiğinde başarılı olacağını garanti etmez. Hata da verebilir.
Controller’lar 202 kodunu kullanabilir fakat diğer resource’ların kullanması doğru değildir.

204 No Content
Client’ın gönderdiği isteğe karşılık olarak herhangi bir body gönderilmediği durumlarda server’ın kasıtlı olarak body alanını boş bıraktığını belirtmek için kullanılır.
301 Moved Permanently

Client’ın istek gönderdiği URI’ın artık kullanılmadığını ve başka bir adreste hizmet verdiğini belirtir. Response’ta bu kodla beraber header’da Location alanında yeni URI gönderilmelidir.

304 Not Modified
Bu kod 204'e benzer. Body’siz gönderilir. Client’ın resource’un zaten en güncel haline sahip olduğunu belirtir.

400 Bad Request
Genel 4xx kodudur. Diğer kodların ihtiyacımızı karşılamadığı durumlarda 400 kullanılır.

401 Unauthorized
Korumalı bir resource’a gerekli authorization sağlanmadan erişilmeye çalışıldığını ifade eder.

403 Forbidden
Bu kod 401'le karıştırılır ama aralarındaki fark şudur: Authorization bilgileri hiç gönderilmediyse veya yanlış gönderildiyse 401, eğer authorization sağlanan kullanıcının istenen kaynağa erişim yetkisi yoksa 403 döndürülür.

404 Not Found
Client’ın istediği resource’un bulunamadığını ifade eder.

405 Method Not Allowed
İstek yapılan URI’ın ilgili metodu desteklemediğini belirtir. Örneğin yalnızca okuma izni verilmiş bir resource POST isteği gönderilirse 405 döner.

406 Not Acceptable
Server’ın, client’ın gönderdiği istekte header’da Accept alanında yazdığı medya tiplerinden herhangi bir formatta çıktı veremediğini belirtir. Örneğin isteğin Accept alanında yalnızca application/json varsa ve server JSON tipinde çıktı veremiyorsa 406 döner.

409 Conflict
Client’ın gönderdiği istekle server’daki resource’u olmaması gereken bir duruma getirmeye çalıştığını ifade eder. Örneğin client nullable olmayan bir alanı null yapmaya çalışırsa 409 döner.

415 Unsupported Media Type
Server’a, desteklemediği tipte bir resource gönderildiğinde 415 döner.

500 Internal Server Error
Aynı 400 gibi genel 5xx kodudur. Server’ın hatası yüzünden istek yerine getirilemiyorsa kullanılır.

