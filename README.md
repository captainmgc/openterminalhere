![alt text](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiDai-xYKhZTuIuyLpZ-hSiEy2sXob_h8TngA1mXA0TvJ2LfIAT9ynbs36yH6vyhwQo1IHL4Cq83e-nZgQF8lSJniZNSFfzP0kGH5Y_ia16MOTy7lgRdEUsssK7xD-mSZWSxVsoirONhVqkStmfTPfUEqU7jyUMWwc8UseS3H_tSRxQp5lUDziy3UC2JIY/s320/Gemini_Generated_Image_ukywh9ukywh9ukyw.jpeg)
![alt text]([https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiDai-xYKhZTuIuyLpZ-hSiEy2sXob_h8TngA1mXA0TvJ2LfIAT9ynbs36yH6vyhwQo1IHL4Cq83e-nZgQF8lSJniZNSFfzP0kGH5Y_ia16MOTy7lgRdEUsssK7xD-mSZWSxVsoirONhVqkStmfTPfUEqU7jyUMWwc8UseS3H_tSRxQp5lUDziy3UC2JIY/s320/Gemini_Generated_Image_ukywh9ukywh9ukyw.jpeg](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgkTMps89_YyrJ2Hka-6MLaHlN-WLBDlwY8Er8f984KTSrvEt08-yWEQvp0mEydcS9IcuaLrCvNbqTCXRXR2S9GexSSU7-1zZfglmH2_UZFyEgZC1vyyf0joo9ovNiFdYca8x-vG-BKcwW6VAjp7G2CkrB3vXzG1BVVhrLmvC1SG1u4GFk6E_hIHk8nn80/s16000/Ekran%20g%C3%B6r%C3%BCnt%C3%BCs%C3%BC%202025-03-08%20010859.png))


# Burada Terminal Aç - Windows Sağ Tıklama Menüsü Eklentisi

Bu araç, Windows sağ tıklama menüsüne "Burada Terminal Aç" özelliğini ekler. Linux sistemlerindeki benzer özelliğe alternatif olarak geliştirilmiştir ve Windows 7, 8, 10 ve 11 sürümlerinde çalışmaktadır.

## İçindekiler
- [Kurulum](#kurulum)
- [Kaldırma](#kaldırma)
- [Nasıl Çalışır](#nasıl-çalışır)
- [Özelleştirme](#özelleştirme)
- [Sorun Giderme](#sorun-giderme)

## Kurulum

1. `TerminalAc.reg` dosyasına çift tıklayın
2. Açılan güvenlik uyarısını onaylayın
3. "Registry düzenleyicisi" uyarısında "Evet" seçeneğini tıklayın
4. İşlem tamamlandığında "Registry düzenleyicisindeki bilgiler başarıyla eklendi" mesajını göreceksiniz

Kurulumdan sonra, aşağıdaki yerlerde sağ tıkladığınızda "Burada Terminal Aç" seçeneğini görebilirsiniz:
- Herhangi bir klasöre sağ tıkladığınızda 📁
- Klasör içinde boş bir alana sağ tıkladığınızda 🗂️
- Herhangi bir sürücüye sağ tıkladığınızda 💾

## Kaldırma

1. `TerminalAcKaldir.reg` dosyasına çift tıklayın
2. Açılan güvenlik uyarısını onaylayın
3. "Registry düzenleyicisi" uyarısında "Evet" seçeneğini tıklayın
4. İşlem tamamlandığında "Registry düzenleyicisindeki bilgiler başarıyla eklendi" mesajını göreceksiniz

Kaldırma işleminden sonra, sağ tıklama menüsünden "Burada Terminal Aç" seçeneği tamamen kaldırılacaktır.

## Nasıl Çalışır

Bu araç, Windows Kayıt Defteri'ne (Registry) aşağıdaki anahtarları ekler:
- `HKEY_CLASSES_ROOT\Directory\shell\OpenTerminalHere`
- `HKEY_CLASSES_ROOT\Directory\Background\shell\OpenTerminalHere`
- `HKEY_CLASSES_ROOT\Drive\shell\OpenTerminalHere`

Bu anahtarlar, sağ tıklama menüsüne "Burada Terminal Aç" seçeneğini ekler ve seçildiğinde PowerShell'i o konumda başlatır.

## Özelleştirme

Varsayılan olarak, bu araç PowerShell'i açar. Command Prompt (cmd.exe) kullanmak isterseniz, `TerminalAc.reg` dosyasındaki:

```
@="powershell.exe -NoExit -Command \"Set-Location -LiteralPath '%V'\""
```

satırını aşağıdaki ile değiştirin:

```
@="cmd.exe /k \"cd /d %V\""
```

## Sorun Giderme

**Sorun**: Registry düzenlemelerine izin verilmiyor

**Çözüm**: Dosyayı yönetici olarak çalıştırın. Bunun için dosyaya sağ tıklayın ve "Yönetici olarak çalıştır" seçeneğini seçin.

**Sorun**: Kurulumdan sonra özellik çalışmıyor

**Çözüm**: Windows'u yeniden başlatmayı deneyin. Sorun devam ederse, kayıt defteri anahtarlarının doğru eklenip eklenmediğini kontrol edin.

---

Bu araç, açık kaynak kodludur ve kişisel kullanım için ücretsizdir. Sorunları veya önerileri bildirmekten çekinmeyin. 😊
