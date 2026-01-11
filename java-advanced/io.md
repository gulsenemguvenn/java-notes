# Input/Output (IO)

## **📌 Java I/O Nedir?**

Java I/O, verilerin bir kaynaktan (dosya, ağ, bellek vb.) okunması ve bu verilere yazılmasıyla ilgili işlemleri içerir. I/O işlemleri, Java'da `InputStream` ve `OutputStream` gibi temel sınıflar üzerinden yapılır.

Java'da I/O işlemleri, verilerin bir kaynaktan alınıp başka bir kaynağa gönderilmesi şeklinde düşünülür. Örneğin:

- Dosya okuma ve yazma işlemleri  
- Kullanıcıdan veri alma (input) ve ekrana veri yazdırma (output)  

Java'da I/O işlemleri, verilerin **byte (ikili veri)** veya **character (karakter)** tabanlı olarak işlenmesine dayanır.

---

## **📌 I/O Sınıflarına Genel Bakış**

Java I/O, iki ana gruba ayrılır:

### **1. Byte Stream (Bayt Akışları)**

Byte stream sınıfları, byte verileri işlemek için kullanılır ve tüm veri türleri (metin, resimler, ses dosyaları vb.) üzerinde işlem yapabilir.  
`InputStream` ve `OutputStream` sınıflarının alt sınıflarıdır.

**Byte Stream Sınıfları**

- **FileInputStream:** Bir dosyadan byte okur.  
- **FileOutputStream:** Bir dosyaya byte yazar.  
- **BufferedInputStream:** Verileri byte olarak okur, ancak bellek üzerinde tampon kullanır.  
- **BufferedOutputStream:** Verileri byte olarak yazar, ancak bellek üzerinde tampon kullanır.  

📌 Örnek (FileInputStream ve FileOutputStream):

![alt text](image-107.png)

**Önemli Noktalar:**

- **FileInputStream** ve **FileOutputStream**, sadece byte verilerini işler, bu nedenle dosyanın içeriği metin veya ikili dosya olabilir.  
- **BufferedInputStream** ve **BufferedOutputStream**, performansı artırmak için tampon (buffer) kullanarak okuma ve yazma işlemlerini hızlandırır.  

---

### **2. Character Stream (Karakter Akışları)**

Character stream, sadece `char` türündeki veriler üzerinde işlem yapar ve genellikle metin verileriyle çalışırken kullanılır.  
`Reader` ve `Writer` sınıflarının alt sınıflarıdır.

**Character Stream Sınıfları**

- **FileReader:** Bir dosyadan karakter okur.  
- **FileWriter:** Bir dosyaya karakter yazar.  
- **BufferedReader:** Satır satır okuma yapar.  
- **BufferedWriter:** Satır satır yazma yapar.  

📌 Örnek (FileReader ve FileWriter):

![alt text](image-108.png)

**Önemli Noktalar:**

- **FileReader** ve **FileWriter**, `char` veri tipini işler ve genellikle metin dosyaları için kullanılır.  
- **BufferedReader** ve **BufferedWriter**, `FileReader` ve `FileWriter`'a göre daha verimlidir çünkü tamponlama kullanır.  

---

## **📌 I/O İle İlgili Önemli Sınıflar ve Arayüzler**

- **InputStream:** Byte tabanlı okuma işlemleri  
- **OutputStream:** Byte tabanlı yazma işlemleri  
- **Reader:** Karakter tabanlı okuma işlemleri  
- **Writer:** Karakter tabanlı yazma işlemleri  
- **BufferedReader:** Satır satır okuma  
- **BufferedWriter:** Satır satır yazma  

---

## **📌 Serialization ve Deserialization**

Java'da **Serialization (Serileştirme)**, nesnelerin bir byte akışına dönüştürülmesidir.  
**Deserialization** ise byte akışından nesnenin tekrar oluşturulmasıdır.

📌 Serialization Örneği:

![alt text](image-109.png)

📌 Deserialization Örneği:

![alt text](image-110.png)

**Önemli Noktalar:**

- **Serializable** arayüzü, bir nesnenin serileştirilmesine izin verir.  
- **ObjectInputStream** ve **ObjectOutputStream**, nesneleri byte akışına dönüştürmek ve geri almak için kullanılır.  

---

## **📌 I/O Mülakat Soruları ve Cevapları**

### 1️⃣ FileInputStream ile FileReader arasındaki fark nedir?
**Cevap:**  
- FileInputStream byte tabanlıdır, her tür dosyayı okuyabilir.  
- FileReader karakter tabanlıdır, sadece metin dosyaları için uygundur.  

### 2️⃣ BufferedReader ve FileReader arasındaki fark nedir?
**Cevap:**  
- BufferedReader tampon kullanır ve satır satır okur.  
- FileReader karakter karakter okur ve tamponlama yapmaz.  

### 3️⃣ Serialization nedir ve neden kullanılır?
**Cevap:**  
Nesnelerin byte akışına çevrilerek dosyaya yazılması veya ağ üzerinden taşınması için kullanılır.  

### 4️⃣ Byte Stream ve Character Stream farkı nedir?
**Cevap:**  
- Byte Stream: Her tür veri (resim, ses, metin)  
- Character Stream: Sadece metin verileri  

### 5️⃣ Neden BufferedReader ve BufferedWriter kullanmalıyız?
**Cevap:**  
Tamponlama sayesinde performans artar, büyük dosyalarda daha hızlı okuma-yazma yapılır.  

---

## **📌 Özet**

- Java I/O, veri okuma ve yazma işlemlerini kapsar.  
- **Byte Stream** ve **Character Stream** olmak üzere iki ana yapı vardır.  
- **Serialization & Deserialization**, nesnelerin kalıcı hale getirilmesini sağlar.  
- **BufferedReader / BufferedWriter**, performans için tercih edilir.  
