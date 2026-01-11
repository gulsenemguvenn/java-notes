# SOLID Prensibi

## SOLID Prensibi Nedir?

SOLID, yazılım tasarımında daha iyi, sürdürülebilir ve esnek kod yazmayı amaçlayan 5 temel prensibin baş harflerinden oluşan bir kısaltmadır. Bu prensipler, nesne yönelimli programlama (OOP) kullanılarak yazılımın kalitesini artırmaya yardımcı olur.

---

## S - Single Responsibility Principle (SRP)  
### Tek Sorumluluk Prensibi

Her sınıf yalnızca **bir sorumluluğa** sahip olmalıdır.  
Yani bir sınıfın yaptığı iş sadece tek bir amaca hizmet etmeli ve sadece o işten sorumlu olmalıdır.

📌 Bir sınıfın değişmesi için yalnızca **tek bir nedeni** olmalıdır.

---

## O - Open / Closed Principle (OCP)  
### Açık / Kapalı Prensibi

Yazılım bileşenleri:

- **Genişlemeye açık**
- **Değiştirmeye kapalı**

olmalıdır.

Yeni bir özellik eklerken mevcut kodu değiştirmek yerine, yeni sınıflar veya metotlar ekleyerek sistemi genişletebilmeliyiz.

---

## L - Liskov Substitution Principle (LSP)  
### Liskov Yerine Geçme Prensibi

Alt sınıflar, üst sınıfların yerine sorunsuzca kullanılabilmelidir.

Yani:

- Bir nesne, üst sınıf türünde bekleniyorsa
- Alt sınıf nesnesi de aynı davranışı bozmadan kullanılabilmelidir.

Alt sınıf, üst sınıfın sözleşmesini ihlal etmemelidir.

---

## I - Interface Segregation Principle (ISP)  
### Arayüz Ayrım Prensibi

Kullanıcılar, kullanmadıkları metotları içeren arayüzleri implement etmeye zorlanmamalıdır.

Büyük ve şişkin arayüzler yerine:

- Daha küçük
- Daha amaca özel

arayüzler tercih edilmelidir.

---

## D - Dependency Inversion Principle (DIP)  
### Bağımlılıkların Tersine Çevrilmesi Prensibi

Yüksek seviyeli modüller, düşük seviyeli modüllere doğrudan bağlı olmamalıdır.  
Her ikisi de **soyutlamalara (interface / abstract class)** bağlı olmalıdır.

Somut sınıflar, soyutlamalara bağımlı olmalı; soyutlamalar somut sınıflara değil.

---

## 📌 Genel Özet

SOLID prensipleri sayesinde:

✅ Kod daha okunabilir olur  
✅ Bakımı kolaylaşır  
✅ Genişletilebilirlik artar  
✅ Bağımlılıklar azalır  
✅ Test edilebilirlik yükselir  

Kısaca:

> SOLID, sürdürülebilir, esnek ve temiz mimari tasarlamanın temel taşıdır.
