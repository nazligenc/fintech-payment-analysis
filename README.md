# PayFlow | Fintech Ödeme Analizi

## Proje Hakkında

Bu proje, PayFlow adlı kurgusal bir fintech platformunun ödeme işlem verilerini SQL ve veri görselleştirme araçları kullanarak analiz etmektedir.

Projenin amacı; ödeme performansını değerlendirmek, başarısız ve iptal edilen işlemlerdeki örüntüleri belirlemek, müşteri ve ödeme davranışlarını incelemek ve analiz sonuçlarını anlamlı iş içgörülerine ve önerilere dönüştürmektir.

## İş Problemi

PayFlow, ödeme operasyonlarını daha iyi anlamak ve iyileştirilmesi gereken alanları belirlemek istemektedir.

Bu doğrultuda analiz aşağıdaki sorulara odaklanmaktadır:

- Hangi ödeme yöntemlerinde başarısızlık oranları daha yüksektir?
- Başarısızlık oranları zaman içerisinde nasıl değişmektedir?
- Başarısız işlemlerin en yaygın nedenleri nelerdir?
- Günün hangi saatlerinde işlem yoğunluğu daha fazladır?
- İşlem örüntüleri, üye iş yeri kategorilerine ve cihaz türlerine göre nasıl farklılaşmaktadır?
- Ödeme tercihleri ve işlem sonuçları müşteri segmentlerine göre nasıl değişmektedir?
- Ortalama işlem tutarları işlem durumlarına göre nasıl farklılaşmaktadır?
- Ödeme performansı şehirlere göre nasıl değişmektedir?

Analiz sonuçları, ödeme deneyimini iyileştirmeye ve potansiyel operasyonel sorunları belirlemeye yönelik veri odaklı kararları desteklemeyi amaçlamaktadır.

## Veri Seti

Veri seti, Ocak–Haziran 2026 döneminde kaydedilmiş 1.200 adet sentetik ödeme işleminden oluşmaktadır.

Her satır tek bir ödeme girişimini temsil etmektedir.

Veri setinde aşağıdaki bilgiler yer almaktadır:

- İşlem ID'si ve tarihi
- Müşteri segmenti
- Şehir
- Ödeme yöntemi
- Üye iş yeri kategorisi
- İşlem tutarı
- İşlem durumu
- Başarısızlık nedeni
- Cihaz türü
- İşlem saati

Veri seti eğitim ve analiz amaçlı oluşturulmuştur.

## Kullanılan Araçlar

- PostgreSQL
- SQLiteOnline
- Microsoft Excel
- Google Sheets
- Looker Studio
- GitHub

## İş Soruları

Analiz kapsamında aşağıdaki sekiz iş sorusu ele alınmıştır:

1. Ödeme yöntemlerine göre işlem sayıları ve başarısızlık oranları nedir?
2. Ödeme yöntemlerine göre aylık başarısızlık oranları nasıl değişmektedir?
3. Başarısız işlem nedenlerinin yüzdesel dağılımı nasıldır?
4. İşlem yoğunluğu ve işlem durumlarının oranları günün saatlerine göre nasıl değişmektedir?
5. Üye iş yeri kategorilerine göre işlem sayıları ve cihaz türlerinin dağılımı nasıldır?
6. Ödeme yöntemi tercihleri ve işlem sonuçları müşteri segmentlerine göre nasıl değişmektedir?
7. Ortalama işlem tutarı başarılı, başarısız ve iptal edilen işlemler arasında nasıl farklılaşmaktadır?
8. Şehirlere göre işlem sayıları ve başarılı işlem oranları nasıldır?

## Analiz Süreci

### 1. SQL ile Veri Analizi

Veri setini incelemek ve sekiz iş sorusunu yanıtlamak amacıyla SQL kullanılmıştır.

Analiz sürecinde:

- Veriler filtrelenmiş ve gruplandırılmıştır.
- İşlem sayıları ve tutarları hesaplanmıştır.
- Başarısızlık ve başarı oranları incelenmiştir.
- Ödeme yöntemlerinin aylık performansları karşılaştırılmıştır.
- Müşteri segmentleri ve ödeme tercihleri analiz edilmiştir.
- İşlemler saat, şehir, üye iş yeri kategorisi ve cihaz türüne göre incelenmiştir.

Kullanılan SQL teknikleri:

- GROUP BY ve ORDER BY
- CASE WHEN
- Common Table Expressions (CTE)
- Aggregate Functions
- Window Functions
- Date and Time Functions
- Conditional Aggregation

### 2. Veri Görselleştirme

Ödeme performansını, işlem örüntülerini ve kategoriler arasındaki farklılıkları görselleştirmek amacıyla Looker Studio kullanılarak bir dashboard oluşturulmuştur.

Dashboard, temel metriklerin genel görünümünü sunmakta ve ödeme yöntemleri, işlem durumları ve diğer boyutlar arasındaki farklılıkların incelenmesini sağlamaktadır.

### 3. İş İçgörülerinin Değerlendirilmesi

SQL analizlerinden elde edilen sonuçlar değerlendirilerek öne çıkan örüntüler, potansiyel operasyonel sorunlar ve daha ayrıntılı incelenmesi gereken alanlar belirlenmiştir.

Elde edilen bulgular iş içgörülerine ve uygulanabilir önerilere dönüştürülmüştür.

## Dashboard

**Ödeme Performansı Dashboard'u (PDF)**

[Dashboard PDF'ini Görüntüle](dashboard/Payment_Performance_Dashboard.pdf)

**Canlı Looker Studio Dashboard'u**

[İnteraktif Dashboard'u Görüntüle](https://datastudio.google.com/reporting/af6723e2-2f4a-479b-8007-2a485b2ac7b8)

## Öne Çıkan Bulgular

### 1. Ödeme Yöntemlerinin Performansı

Bank Transfer, 102 işlem girişiminden 11'inin başarısız olmasıyla %10,78 oranında başarısızlık göstermiştir. Bu oran, ödeme yöntemleri arasındaki en yüksek başarısızlık oranıdır.

Digital Wallet ise en düşük başarısızlık oranına sahip ödeme yöntemi olmuştur.

Bu sonuç, Bank Transfer işlemlerinin daha ayrıntılı incelenmesi gerektiğine işaret etmektedir.

### 2. Aylık Başarısızlık Oranları

Bank Transfer ödeme yöntemi, mart ayında %17,39 ile en yüksek aylık başarısızlık oranına ulaşmıştır.

Başarısızlık oranlarının ödeme yöntemlerine ve aylara göre değişiklik göstermesi, ödeme performansının zaman içerisinde takip edilmesinin önemini ortaya koymaktadır.

### 3. Başarısız İşlem Nedenlerinin Dağılımı

Insufficient Funds (Yetersiz Bakiye), 62 başarısız işlemin 24'ünü oluşturarak %38,71 ile en yaygın başarısızlık nedeni olmuştur.

İkinci sırada %14,52 ile Technical Error (Teknik Hata) yer almaktadır.

Bu bulgular, Ürün ve Operasyon ekipleri tarafından incelenebilecek potansiyel iyileştirme alanlarına işaret etmektedir.

### 4. Saatlik İşlem Örüntüleri

Saat 19.00, toplam 125 işlemle günün en yoğun saati olmuştur. Bu işlemlerin 116'sı başarılı, 7'si başarısız ve 2'si iptal edilmiştir.

İşlem yoğunluğunun gün içerisinde değişiklik göstermesi, özellikle yoğun saatlerde operasyonel performansın takip edilmesi gerektiğini göstermektedir.

### 5. Üye İş Yeri Kategorileri ve Cihaz Dağılımı

Mobil işlemler toplam işlemlerin %73,67'sini, Web işlemleri ise %26'sını oluşturmuştur.

Grocery kategorisi, 266 işlemle en yüksek işlem sayısına sahip üye iş yeri kategorisi olmuştur.

Bu sonuçlar, farklı üye iş yeri kategorilerinde mobil ödeme deneyiminin önemini ortaya koymaktadır.

### 6. Müşteri Segmentlerinin Analizi

En düşük başarısızlık oranı %1,46 ile Premium segmentindeki Credit Card işlemlerinde görülmüştür.

En yüksek başarısızlık oranı ise %13,33 ile New segmentindeki Bank Transfer işlemlerinde gözlemlenmiştir.

Bu farklılıklar, ödeme tercihlerinin ve işlem sonuçlarının müşteri segmentlerine göre değişebildiğini göstermektedir.

### 7. İşlem Durumuna Göre Ortalama İşlem Tutarı

İptal edilen işlemler, 2.341,03 TRY ile en yüksek ortalama işlem tutarına sahiptir.

Başarılı işlemlerin ortalama tutarı 1.989,93 TRY, başarısız işlemlerin ortalama tutarı ise 1.910,99 TRY olarak hesaplanmıştır.

Bu bulgu, yüksek tutarlı işlemlerde iptal oranlarının artıp artmadığının ayrıca incelenebileceğini düşündürmektedir.

### 8. Şehirlere Göre Ödeme Performansı

Şehir bazlı analiz, işlem başarı oranlarının şehirler arasında farklılık gösterdiğini ortaya koymuştur.

Ankara, daha yüksek başarı oranına sahip şehirler arasında yer alırken İzmir en düşük başarı oranına sahip olmuştur.

Şehir bilgisi eksik olan kayıtların da yüksek bir başarı oranına sahip olduğu görülmüştür. Ancak bu kayıtlar belirli bir şehirle ilişkilendirilemeyeceği için konum bazlı değerlendirmelerde dikkatli olunmalıdır.

## İş Önerileri

Analiz sonuçlarına dayanarak aşağıdaki alanlarda ek incelemeler yapılması önerilmektedir:

- Bank Transfer işlemlerindeki yüksek başarısızlık oranının nedenleri araştırılmalıdır.
- Ödeme yöntemleri ile başarısızlık nedenleri arasındaki ilişki incelenmelidir.
- Aylık başarısızlık oranlarındaki değişimler düzenli olarak takip edilmelidir.
- Yoğun işlem saatlerinde sistem performansı ve ödeme deneyimi izlenmelidir.
- Üye iş yeri kategorilerine göre mobil ödeme deneyimi değerlendirilmelidir.
- Müşteri segmentleri arasındaki işlem sonucu farklılıkları incelenmelidir.
- Farklı işlem tutarı aralıklarında iptal oranları analiz edilmelidir.
- Şehir bazlı iş kararları alınmadan önce eksik şehir bilgileri gözden geçirilmelidir.

## Sonuç

Bu proje, ham ödeme işlem verilerinin SQL kullanılarak anlamlı iş içgörülerine dönüştürülmesini göstermektedir.

Ödeme yöntemleri, başarısızlık nedenleri, saatlik işlem örüntüleri, üye iş yeri kategorileri, müşteri segmentleri, işlem tutarları ve şehir bazlı performans analiz edilerek ödeme operasyonlarında iyileştirme yapılabilecek potansiyel alanlar belirlenmiştir.

Proje; SQL sorgulama, veri yorumlama ve dashboard geliştirme süreçlerini bir araya getirerek fintech ödeme operasyonlarının veri odaklı bir yaklaşımla değerlendirilmesini amaçlamaktadır.

## Proje Klasör Yapısı

- `data/` — Kaynak işlem veri seti
- `sql/` — İş sorularına yönelik SQL sorguları
- `dashboard/` — Dashboard PDF'i ve ekran görüntüleri
- `insights/` — Analiz bulguları ve iş önerileri
