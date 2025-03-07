# 🖥️ Burada Terminal Aç - Windows Sağ Tıklama Menüsü Eklentisi

Bu araç, Windows sağ tıklama menüsüne "Burada Terminal Aç" özelliğini ekler. Linux sistemlerindeki benzer özelliğe alternatif olarak geliştirilmiştir ve **Windows 7, 8, 10 ve 11** sürümlerinde çalışmaktadır.

---

## 📝 İçindekiler
- 🔧 [Kurulum](#kurulum)
- 🗑️ [Kaldırma](#kaldırma)
- ⚙️ [Nasıl Çalışır](#nasıl-çalışır)
- 🎨 [Özelleştirme](#özelleştirme)
- ⚠️ [Sorun Giderme](#sorun-giderme)

---

## 🔧 Kurulum
1. `TerminalAc.reg` dosyasına çift tıklayın 📄  
2. Açılan güvenlik uyarısını onaylayın 🔒  
3. "Registry düzenleyicisi" uyarısında **Evet** seçeneğini tıklayın ✅  
4. İşlem tamamlandığında "Registry bilgileri başarıyla eklendi" mesajını göreceksiniz ✅  

**Kurulum sonrası kullanım:**  
- 📁 Herhangi bir klasöre sağ tıkladığınızda  
- 🖼️ Klasörde boş alana sağ tıkladığınızda  
- 💾 Sürücüye sağ tıkladığınızda  
"Burada Terminal Aç" seçeneği görünür 🚀  

---

## 🗑️ Kaldırma
1. `TerminalAcKaldir.reg` dosyasına çift tıklayın 📄  
2. Güvenlik uyarısını onaylayın 🔒  
3. "Registry düzenleyicisi" uyarısında **Evet** seçeneğini tıklayın ✅  
4. Başarı mesajı alındığında işlem tamamlanır ✅  

**Sonuç:** Sağ tıklama menüsünden "Burada Terminal Aç" seçeneği kalıcı olarak kaldırılır ❌  

---

## ⚙️ Nasıl Çalışır
Windows Kayıt Defteri'ne aşağıdaki anahtarlar eklenir:  
```plaintext
HKEY_CLASSES_ROOT\Directory\shell\OpenTerminalHere  
HKEY_CLASSES_ROOT\Directory\Background\shell\OpenTerminalHere  
HKEY_CLASSES_ROOT\Drive\shell\OpenTerminalHere


