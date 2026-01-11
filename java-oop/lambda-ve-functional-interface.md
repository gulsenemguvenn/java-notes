# Lambda İfadeleri ve Fonksiyonel İnterface

## 📌 1. Lambda İfadeleri Nedir?

Lambda ifadeleri (Lambda Expressions), Java'da fonksiyonel programlamayı destekleyen bir yapıdır.  
- Kod tekrarını azaltır.  
- Daha okunaklı ve kısa kod yazmayı sağlar.  
- Anonim (ismi olmayan) fonksiyonlar gibi çalışır.  

Lambda ifadeleri, özellikle fonksiyonel arayüzlerle kullanılır.

---

## 📌 2. Lambda İfadelerinin Sözdizimi

Lambda ifadesinin temel formatı:

![alt text](images/image-133.png)

- Tek parametre varsa parantez kullanılmayabilir.  
- Tek satırlık işlem varsa süslü parantez ve `return` gerekmez.

📌 Örnek:

![alt text](images/image-134.png)

Tek satır dönüş:

![alt text](images/image-135.png)

---

## 📌 3. Fonksiyonel Arayüz (Functional Interface)

Fonksiyonel arayüz, **sadece tek bir abstract metodu olan interface**’tir.  
- Lambda ifadeleri ile birlikte kullanılır.  
- `@FunctionalInterface` anotasyonu ile işaretlenir.

📌 Örnek:

![alt text](images/image-136.png)

---

## 📌 4. Java’daki Hazır Fonksiyonel Arayüzler

`java.util.function` paketi altında bulunur:

![alt text](images/image-137.png)

### Predicate<T>

![alt text](images/image-138.png)

### Function<T, R>

![alt text](images/image-139.png)

### Consumer<T>

![alt text](images/image-140.png)

### Supplier<T>

![alt text](images/image-141.png)

---

## 📌 5. Lambda ile Koleksiyon İşlemleri

![alt text](images/image-142.png)

---

## Lambda ve Fonksiyonel Programlama Mantığı

Lambda ifadeleri `->` operatörü ile yazılır.  
Sol taraf parametreler, sağ taraf işlemdir.

Örnek:

![alt text](images/image-143.png)

Lambda ifadeleri tek başına anlamlı değildir, mutlaka bir fonksiyonel interface ile eşleşmelidir.

![alt text](images/image-144.png)  
![alt text](images/image-145.png)

İmza uyumu zorunludur.

---

## Birden Fazla Lambda Kullanımı

![alt text](images/image-146.png)

---

## Blok Lambda (Çok Satırlı)

![alt text](images/image-147.png)

---

## Lambda'nın Metoda Parametre Olarak Gönderilmesi

![alt text](images/image-148.png)

---

## Jenerik Lambda ve Fonksiyonel Interface

![alt text](images/image-149.png)  
![alt text](images/image-150.png)

---

## Variable Capture (Dış Değişken Kullanımı)

![alt text](images/image-151.png)  
![alt text](images/image-152.png)  
![alt text](images/image-153.png)

---

## Lambda ve Exception

![alt text](images/image-154.png)

---

## Method Reference

### Static Metot Referansı

![alt text](images/image-155.png)

### Nesne Üzerinden Metot Referansı

![alt text](images/image-156.png)

### Constructor Referansı

![alt text](images/image-157.png)

---

## Java’nın Hazır Fonksiyonel Interfaceleri

![alt text](images/image-158.png)  
![alt text](images/image-159.png)

---

## 🎯 Mülakat Soruları

### 1️⃣ Lambda nedir?
- Anonim fonksiyon yapısıdır.  
- Java 8 ile gelmiştir.  
- Fonksiyonel arayüzlerle kullanılır.

### 2️⃣ Fonksiyonel Interface nedir?
- Tek bir abstract metodu olan interface.

### 3️⃣ Hazır arayüzler

![alt text](images/image-160.png)

### 4️⃣ Çok satırlı lambda

![alt text](images/image-161.png)

---

## 📌 Özet

✅ Lambda ifadeleri kısa ve okunaklı kod sağlar.  
✅ Fonksiyonel interface ile birlikte çalışır.  
✅ Predicate, Function, Consumer, Supplier gibi hazır yapılar vardır.  
✅ Stream API ve koleksiyon işlemlerinde yoğun kullanılır.
