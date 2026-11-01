# Insights & Recommendations

## Insight 1 — Payment Method Performance

### Finding
- Bank Transfer, 102 işlem içerisinde 11 başarısız işlemle %10,78 başarısızlık oranına sahiptir.
- Ödeme yöntemleri arasında en düşük başarısızlık oranı Digital Wallet yöntemindedir.

### Insight
Bank Transfer yönteminde diğer ödeme yöntemlerine kıyasla daha yüksek bir başarısızlık oranı görülmektedir. Bu durum, ödeme yöntemlerinin performanslarının birbirinden farklı olabileceğini göstermektedir.

### Recommendation
Bank Transfer işlemlerindeki başarısızlıkların nedenleri incelenmeli ve ilgili ödeme süreçleri kontrol edilmelidir. Digital Wallet gibi daha düşük başarısızlık oranına sahip yöntemlerin performansı da karşılaştırma amacıyla takip edilebilir.

### Limitation
Bu analiz, başarısızlık oranlarını göstermektedir ancak başarısızlıkların teknik veya operasyonel nedenlerini tek başına açıklamamaktadır.

---

## Insight 2 — Monthly Failure Rate by Payment Method

### Finding
- Bank Transfer yönteminde en yüksek başarısızlık oranı mart ayında %17,39 olarak gerçekleşmiştir.
- En düşük başarısızlık oranları ocak ayında Debit Card, şubat ayında Digital Wallet ve nisan ayında Bank Transfer yöntemlerinde %0 olarak görülmüştür.
- Bank Transfer yönteminin aylık başarısızlık oranlarında belirgin dalgalanmalar bulunmaktadır.

### Insight
Ödeme yöntemlerinin başarısızlık oranları aylara göre değişiklik göstermektedir. Özellikle Bank Transfer yöntemindeki dalgalanmalar, bu yöntemin aylık performansının daha yakından takip edilmesi gerektiğini göstermektedir.

### Recommendation
Aylık başarısızlık oranları düzenli olarak izlenmeli ve belirgin artış görülen dönemler detaylı incelenmelidir. Oranlar değerlendirilirken ilgili aylardaki toplam işlem sayıları da dikkate alınmalıdır.

### Limitation
Düşük işlem sayısına sahip aylarda başarısızlık oranları daha fazla değişkenlik gösterebilir. Bu nedenle yalnızca yüzdelere bakarak kesin sonuçlara ulaşmak doğru değildir. Ayrıca bu analiz, aylık değişimlerin nedenlerini açıklamamaktadır.

---

## Insight 3 — Distribution of Transaction Failure Reasons

### Finding
- Başarısız işlemlerin %38,71'i Insufficient Funds nedeniyle gerçekleşmiştir.
- Technical Error %14,52 ile ikinci sırada yer almaktadır.
- Bank Timeout ve Limit Exceeded nedenlerinin her biri %11,29 oranındadır.
- Diğer başarısızlık nedenleri daha düşük oranlarda görülmektedir.

### Insight
Başarısız işlemlerin önemli bir bölümü yetersiz bakiye nedeniyle oluşmaktadır. Teknik hatalar da dikkat çeken nedenler arasındadır. Bu durum, başarısızlıkların hem müşteri kaynaklı hem de teknik süreçlerle ilişkili olabileceğini düşündürmektedir.

### Recommendation
Yetersiz bakiye nedeniyle başarısız olan işlemler için müşterilere daha açıklayıcı bilgilendirmeler sunulabilir. Teknik hata ve banka zaman aşımı gibi nedenler ise ilgili teknik ekipler tarafından ayrıca incelenmelidir.

### Limitation
Analiz, sistemde kayıtlı başarısızlık nedenlerine dayanmaktadır. Bu kayıtlar tek başına her işlemin gerçek nedenini veya sorunun kaynağını kesin olarak ortaya koymamaktadır.

---

## Insight 4 — Transaction Activity by Hour

### Finding
- En yoğun işlem saati 19:00 olup bu saatte toplam 125 işlem gerçekleşmiştir.
- Bu işlemlerin 116'sı başarılı, 7'si başarısız ve 2'si iptal edilmiştir.
- En düşük işlem sayısı 03:00 saatinde görülmüştür.

### Insight
İşlem yoğunluğu günün saatlerine göre değişmektedir. Özellikle 19:00 saatinde artan işlem sayısı, bu zaman diliminde sistem performansının ve işlem süreçlerinin yakından takip edilmesini önemli hale getirmektedir.

### Recommendation
İşlem yoğunluğunun arttığı saatlerde sistem performansı, başarısız işlem sayısı ve olası gecikmeler düzenli olarak izlenmelidir. Yoğun saatlerde yaşanabilecek sorunları önlemek için sistem kaynaklarının yeterliliği değerlendirilebilir.

### Limitation
Bu analiz işlem sayılarını ve işlem durumlarının dağılımını incelemektedir. İşlem tutarları hesaplanmadığı için saatlik parasal işlem hacmi hakkında bir değerlendirme yapılamamaktadır.

---

## Insight 5 — Transaction Distribution by Merchant Category and Device Type

### Finding
- En fazla işlem gerçekleşen işyeri kategorisi Grocery olup toplam 266 işlem bulunmaktadır.
- Kategorilerin çoğunda Mobile üzerinden gerçekleştirilen işlem sayısı Web üzerinden gerçekleştirilen işlem sayısından fazladır.
- Genel işlem dağılımında Mobile %73,67, Web ise %26 oranındadır.
- Veri setinde cihaz türü bilgisi eksik olan 4 işlem bulunmaktadır.

### Insight
İşlemlerin büyük bölümünün Mobile üzerinden gerçekleştirilmesi, mobil kanalın ödeme süreçlerinde önemli bir yere sahip olduğunu göstermektedir. Ayrıca bazı kayıtlarda cihaz türü ve işyeri kategorisi bilgilerinin eksik olması veri kalitesi açısından dikkate alınmalıdır.

### Recommendation
Mobil ödeme deneyiminin ve performansının iyileştirilmesine öncelik verilebilir. Eksik cihaz türü ve işyeri kategorisi kayıtlarının azaltılması için veri giriş ve kayıt süreçleri kontrol edilmelidir.

### Limitation
Bu analiz işlem sayılarına ve cihaz türlerinin dağılımına dayanmaktadır. Mobil kanalda daha fazla işlem gerçekleşmesi, bu kanalın daha başarılı veya daha kârlı olduğu anlamına gelmemektedir.

---

## Insight 6 — Customer Segment and Payment Method Analysis

### Finding
- En düşük başarısızlık oranı %1,46 ile Premium segmentindeki Credit Card işlemlerinde görülmüştür.
- En yüksek başarısızlık oranı %13,33 ile New segmentindeki Bank Transfer işlemlerindedir.
- En yüksek iptal oranı %9,62 ile Standard segmentindeki Bank Transfer işlemlerinde görülmüştür.
- Credit Card kullanım oranı Premium segmentinde %45,21, Standard segmentinde ise %41,38'dir.

### Insight
Müşteri segmentlerine göre ödeme yöntemi tercihleri ve işlem sonuçları farklılık göstermektedir. Özellikle Bank Transfer yönteminin bazı segmentlerde daha yüksek başarısızlık ve iptal oranlarına sahip olması dikkat çekmektedir.

### Recommendation
Müşteri segmentleri ve ödeme yöntemleri birlikte değerlendirilerek segment bazlı iyileştirmeler yapılabilir. Başarısızlık oranı yüksek olan segmentlerde ödeme sürecinin daha ayrıntılı incelenmesi faydalı olacaktır.

### Limitation
Analiz, müşteri segmentleri ve ödeme yöntemleri arasındaki dağılımı göstermektedir ancak bu farklılıkların nedenlerini açıklamamaktadır. Müşteri davranışları ve işlem geçmişi gibi ek verilerle daha kapsamlı değerlendirme yapılabilir.

---

## Insight 7 — Average Transaction Amount by Transaction Status

### Finding
- İptal edilen işlemlerin ortalama tutarı 2.341,03 TL'dir.
- Başarılı işlemlerin ortalama tutarı 1.989,93 TL'dir.
- Başarısız işlemlerin ortalama tutarı 1.910,99 TL'dir.

### Insight
İptal edilen işlemlerin ortalama tutarının diğer işlem durumlarına göre daha yüksek olduğu görülmektedir. Bu durum, yüksek tutarlı işlemlerin iptal edilme durumuyla ilişkili olabileceğini düşündürmektedir.

### Recommendation
İşlem tutarları belirli aralıklara ayrılarak her aralık için iptal oranları incelenebilir. Böylece yüksek tutarlı işlemlerde iptal oranının gerçekten daha yüksek olup olmadığı değerlendirilebilir.

### Limitation
Ortalama işlem tutarları tek başına yüksek tutarlı işlemlerin iptal edilme olasılığının daha fazla olduğunu kanıtlamaz. Bu ilişkinin değerlendirilebilmesi için tutar aralıklarına göre işlem durumlarının ayrıca incelenmesi gerekir.

---

## Insight 8 — Transaction Success Rate by City

### Finding
- Şehir bilgisi eksik olan kayıtlar en yüksek başarı oranına sahiptir.
- Ankara, başarı oranı yüksek şehirler arasında yer almaktadır.
- İzmir, incelenen şehirler arasında en düşük başarı oranına sahiptir.

### Insight
Şehirlere göre işlem başarı oranlarında farklılıklar görülmektedir. Ancak şehir bilgisi eksik olan kayıtların en yüksek başarı oranına sahip olması, veri kalitesi açısından ayrıca değerlendirilmesi gereken bir durumdur.

### Recommendation
Şehir bazlı başarı oranları düzenli olarak takip edilebilir. İzmir'deki düşük başarı oranının olası nedenleri daha ayrıntılı incelenebilir. Ayrıca eksik şehir bilgilerinin azaltılması için veri kayıt süreçleri iyileştirilmelidir.

### Limitation
Şehir bilgisi eksik olan kayıtlar gerçek bir şehri temsil etmediğinden bu grubun sonuçları şehirlerle doğrudan karşılaştırılmamalıdır. Ayrıca başarı oranlarındaki farklılıkların nedenleri bu analizden tek başına belirlenememektedir.
