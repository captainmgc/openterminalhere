![alt text]([http://url/to/img.png](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjn-YDFdCZxpKZCGc4HrnIs0I5Lal7LpMJKc8F3m0Q9uq2m12VcSbl6gG2s29rc1srpGNC9a1AqHfp5LzlKkhyphenhyphenFn57fv3Hq2KF6MJ4wSukvTgIDJviXsUBFGPpDg8MLVwvQ98cFs0vOh7e8i1u5ZB0GqydZhHw90cxR0a4TJuQR7okbiprtpwW4dQr_Snk/s2048/Gemini_Generated_Image_ukywh9ukywh9ukyw.jpeg))
# Burada Terminal Aç - Windows Sağ Tıklama Menüsü Eklentisi

Bu araç, Windows sağ tıklama menüsüne "Burada Terminal Aç" özelliğini ekler. Linux sistemlerindeki benzer özelliğe alternatif olarak geliştirilmiştir ve Windows 7, 8, 10 ve 11 sürümlerinde çalışmaktadır.

## İçindekiler
- [Kurulum](#kurulum)
- [Kaldırma](#kaldırma)
- [Nasıl Çalışır](#nasıl-çalışır)
- [Özelleştirme](#özelleştirme)
- [Sorun Giderme](#sorun-giderme)

## Kurulum 🛠️

1. `TerminalAc.reg` dosyasına çift tıklayın
2. Açılan güvenlik uyarısını onaylayın
3. "Registry düzenleyicisi" uyarısında "Evet" seçeneğini tıklayın
4. İşlem tamamlandığında "Registry düzenleyicisindeki bilgiler başarıyla eklendi" mesajını göreceksiniz

Kurulumdan sonra, aşağıdaki yerlerde sağ tıkladığınızda "Burada Terminal Aç" seçeneğini görebilirsiniz:
- Herhangi bir klasöre sağ tıkladığınızda 📁
- Klasör içinde boş bir alana sağ tıkladığınızda 🗂️
- Herhangi bir sürücüye sağ tıkladığınızda 💾

## Kaldırma ❌

1. `TerminalAcKaldir.reg` dosyasına çift tıklayın
2. Açılan güvenlik uyarısını onaylayın
3. "Registry düzenleyicisi" uyarısında "Evet" seçeneğini tıklayın
4. İşlem tamamlandığında "Registry düzenleyicisindeki bilgiler başarıyla eklendi" mesajını göreceksiniz

Kaldırma işleminden sonra, sağ tıklama menüsünden "Burada Terminal Aç" seçeneği tamamen kaldırılacaktır.

## Nasıl Çalışır ⚙️

Bu araç, Windows Kayıt Defteri'ne (Registry) aşağıdaki anahtarları ekler:
- `HKEY_CLASSES_ROOT\Directory\shell\OpenTerminalHere`
- `HKEY_CLASSES_ROOT\Directory\Background\shell\OpenTerminalHere`
- `HKEY_CLASSES_ROOT\Drive\shell\OpenTerminalHere`

Bu anahtarlar, sağ tıklama menüsüne "Burada Terminal Aç" seçeneğini ekler ve seçildiğinde PowerShell'i o konumda başlatır.

## Özelleştirme 🎨

Varsayılan olarak, bu araç PowerShell'i açar. Command Prompt (cmd.exe) kullanmak isterseniz, `TerminalAc.reg` dosyasındaki:

```
@="powershell.exe -NoExit -Command \"Set-Location -LiteralPath '%V'\""
```

satırını aşağıdaki ile değiştirin:

```
@="cmd.exe /k \"cd /d %V\""
```

## Sorun Giderme 🛡️

**Sorun**: Registry düzenlemelerine izin verilmiyor

**Çözüm**: Dosyayı yönetici olarak çalıştırın. Bunun için dosyaya sağ tıklayın ve "Yönetici olarak çalıştır" seçeneğini seçin.

**Sorun**: Kurulumdan sonra özellik çalışmıyor

**Çözüm**: Windows'u yeniden başlatmayı deneyin. Sorun devam ederse, kayıt defteri anahtarlarının doğru eklenip eklenmediğini kontrol edin.

---

Bu araç, açık kaynak kodludur ve kişisel kullanım için ücretsizdir. Sorunları veya önerileri bildirmekten çekinmeyin. 😊
