## Veterinary App

![Ekran Görüntüsü (98)](https://github.com/GamzeSakarya/capstone-backend/assets/126356427/48194571-e46c-45b6-a896-6b4d1e748192)

## Customer (Müşteri) Tablosu
| Endpoint                             | Açıklama                                         |
|--------------------------------------|--------------------------------------------------|
| POST /v1/customer: | Yeni bir müşteri ekler.
| GET /v1/customer/{name}: | Belirtilen isme sahip müşteriyi ve sahip olduğu hayvanları getirir.
| DELETE /v1/customer/{id}: | Belirtilen ID'ye sahip müşteriyi siler.
| PUT /v1/customer: | Belirtilen müşteriyi günceller.
| GET /v1/customer/{name}/{animalName}: |  Belirtilen müşteri ismi ve hayvan ismiyle eşleşen hayvanları getirir.
| GET /v1/customer/all: |  Bütün müşterileri getirir.
## Animal (Hayvan) Tablosu
| Endpoint                             | Açıklama                                         |
|--------------------------------------|--------------------------------------------------|
| POST /v1/animal: | Yeni bir hayvan ekler.
| GET /v1/animal/{name}: | Belirtilen isme sahip hayvanı getirir.
| DELETE /v1/animal/{id}: | Belirtilen ID'ye sahip hayvanı siler.
| PUT /v1/animal: | Belirtilen hayvanları günceller.
| GET /v1/animal/customer/{name}: | Belirtilen müşteri adına göre bütün hayvanları getirir.
| GET /v1/animal/all: | Bütün hayvanları getirir.
## Vaccine (Aşı) Tablosu
| Endpoint                             | Açıklama                                         |
|--------------------------------------|--------------------------------------------------|
POST /v1/vaccine: Yeni bir aşı ekler.
DELETE /v1/vaccine/{id}: Belirtilen ID'ye sahip aşıyı siler.
GET /v1/vaccine/{vaccineName}/{animalName}: Belirtilen aşı ve hayvan ismine göre filtreleme yapar.
GET /v1/vaccine/filter/{animalName}: Belirtilen hayvan adına göre bütün aşıları getirir.
GET /v1/vaccine/date: Belirtilen koruyuculuk tarihine göre aşıları filtreler.
GET /v1/vaccine/{name}: Belirtilen aşı ismine göre filtreleme yapar.
PUT /v1/vaccine: Belirtilen aşıyı günceller.
GET /v1/vaccine/all: Bütün aşıları getirir.
## Doctor (Doktor) Tablosu
| Endpoint                             | Açıklama                                         |
|--------------------------------------|--------------------------------------------------|
| POST /v1/doctor: | Yeni bir doktor ekler.
| GET /v1/doctor/{name}: | Belirtilen isme sahip doktoru ve müsait günlerini getirir.
| DELETE /v1/doctor/{id}: |  Belirtilen ID'ye sahip doktoru siler.
| PUT /v1/doctor: | Belirtilen doktoru günceller.
| GET /v1/doctor/all: | Bütün doktorları getirir.
## AvailableDate (Müsait Gün) Tablosu
| Endpoint                             | Açıklama                                         |
|--------------------------------------|--------------------------------------------------|
| POST /v1/available-date: |  Yeni bir müsait tarih ekler.
| GET /v1/available-date/{id}: |  Belirtilen ID'ye sahip müsait tarihi getirir.
| DELETE /v1/available-date/{id}: |  Belirtilen ID'ye sahip müsait tarihi siler.
| PUT /v1/available-date: |  Belirtilen müsait tarihi günceller.
| GET /v1/available-date/all: |  Bütün müsait tarihleri getirir.
## Appointment (Randevu) Tablosu
| Endpoint                             | Açıklama                                         |
|--------------------------------------|--------------------------------------------------|
| POST /v1/appointment: |  Yeni bir randevu ekler.
| GET /v1/appointment/{id}: |  Belirtilen ID'ye sahip randevuyu getirir.
| DELETE /v1/appointment/{id}: |  Belirtilen ID'ye sahip randevuyu siler.
| GET /v1/appointment/filter: |  Belirtilen hayvan adı ve tarih aralığına göre randevuları getirir.
| GET /v1/appointment/filtered: |  Belirtilen doktor adı ve tarih aralığına göre randevuları getirir.
| PUT /v1/appointment: | Belirtilen randevuyu günceller.
| GET /v1/appointment/all: | Bütün randevuları getirir.
## Report (Rapor) Tablosu
| Endpoint                             | Açıklama                                         |
|--------------------------------------|--------------------------------------------------|
| POST /v1/report: | Yeni bir rapor ekler.
| GET /v1/report/{id}: | Belirtilen ID'ye sahip raporu getirir.
| DELETE /v1/report/{id}: | Belirtilen ID'ye sahip raporu siler.
| PUT /v1/report: | Belirtilen raporu günceller.
| GET /v1/report/all: | Bütün raporları getirir.
## Veteriner Uygulaması
Bu uygulama, bir veteriner kliniği veya muayenehanesi için temel işlemleri yönetmek için tasarlanmış bir yazılımdır. Aşağıda kullanıcıların yapabileceği işlemler ve bu işlemleri gerçekleştirmek için gerekli adımlar açıklanmıştır.

## Kullanıcı İşlemleri
##Müşteri Kaydetme  
Yeni müşterilerin sisteme kaydedilmesi için gerekli adımlar şunlardır:  

Ad, soyad, iletişim bilgileri gibi müşteri bilgilerinin girilmesi.  
Müşteriye ait bir kimlik numarasının oluşturulması veya alınması  

## Müşteriye Ait Hayvan Kaydetme
Müşterinin sahip olduğu hayvanların sisteme kaydedilmesi için gerekli adımlar şunlardır:  

Hayvanın adı, türü, cinsi gibi bilgilerin girilmesi.  
Hayvana ait müşteri bilgilerinin doğrulanması veya seçilmesi.  

## Veteriner Doktor Kaydetme  
Veteriner doktorların sisteme kaydedilmesi için gerekli adımlar şunlardır:    

Ad, soyad, uzmanlık alanı gibi doktor bilgilerinin girilmesi.  
Doktora ait bir kimlik numarasının oluşturulması veya alınması.  

## Veteriner Doktora Ait Müsait Gün Kaydetme   
Veteriner doktorların çalışma günlerinin ve saatlerinin belirlenmesi için gerekli adımlar şunlardır:    

Doktorun haftalık çalışma günleri ve saatlerinin belirlenmesi.  
Randevuların bu çalışma saatlerine göre planlanması için müsait günlerin belirlenmesi.  

## Hayvan ve Doktor İçin Randevu Oluşturma  
Müşterilerin hayvanları için randevu oluşturulması için gerekli adımlar şunlardır:  

Müşteri bilgilerinin seçilmesi veya doğrulanması.
Randevu alınacak hayvanın seçilmesi.
Veteriner doktorun seçilmesi.
Randevu tarihinin ve saatinin belirlenmesi.

## Randevuya Ait Rapor Oluşturma
Yapılan muayene veya tedavilerin raporlanması için gerekli adımlar şunlardır:

Yapılan işlemlerin ve verilen tedavilerin detaylı bir şekilde belirtilmesi.
Gerektiğinde ilaç veya diğer tıbbi müdahalelerin belirtilmesi.

## Rapor ve Hayvana Ait Aşı Kaydetme
Hayvanların aldığı aşıların kaydedilmesi için gerekli adımlar şunlardır:

Hayvanın aşı tarihlerinin ve türlerinin belirtilmesi.
Aşıyı yapan doktorun belirtilmesi.


## Kullanılan Teknolojiler
* Java
* Spring Boot
* Maven
* MySQL
* REST API
* Swagger
* Postman
