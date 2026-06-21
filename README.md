# Escape from VERTEX (VERTEX'den Kaçış) 🚀

Türkiye'nin en genç teknoloji şirketi olan **VERTEX** temalı, korku ve hayatta kalma odaklı 3D kaçış oyunu. Bu proje hem **Masaüstü (C++/OpenGL)** hem de **Web (HTML5/WebGL/Three.js)** platformlarında çalışabilen çift taraflı bir yapıya sahiptir. Tarayıcıda oynamak için doğrudan Vercel'e deploy edilebilir!

---

## 🎮 Web Sürümü (Tarayıcıda Doğrudan Oyna - Vercel Uyumlu)

Web sürümü, C++ oyunundaki tüm 3D modelleri (`.obj`), kaplamaları (`.png`/`.jpg`), ses dosyalarını ve `granny.jsonc` harita yapılandırmasını gerçek zamanlı olarak tarayıcıda çalıştıran gelişmiş bir Three.js motoru içerir.

### Vercel'e Nasıl Yüklenir?
1. Bu projeyi kendi GitHub hesabınızda yeni bir repo olarak açın.
2. Vercel dashboard'una gidin ve **"Add New" -> "Project"** butonuna tıklayın.
3. GitHub reponuzu içe aktarın (import).
4. Herhangi bir derleme ayarı yapmanıza gerek yoktur (**Zero Configuration**). Vercel projeyi otomatik olarak statik web sitesi olarak algılayıp yayına alacaktır!

---

## 💻 Masaüstü Sürümü (Windows C++/OpenGL)

Masaüstü sürümü, projenin orijinal C++ oyun motorunun geliştirilmiş ve optimize edilmiş halidir.

### Masaüstü Sürümü Nasıl Derlenir?
Projeyi derlemek için sisteminizde **CMake** ve **MinGW (GCC)** kurulu olmalıdır.

1. Komut satırını açın ve proje ana dizinine gidin.
2. CMake yapılandırmasını oluşturun:
   ```bash
   cmake -G "MinGW Makefiles" -DCMAKE_POLICY_VERSION_MINIMUM=3.5 -B build_mingw -S .
   ```
3. Projeyi derleyin:
   ```bash
   cmake --build build_mingw
   ```
4. Derleme tamamlandıktan sonra oyunu çalıştırın:
   ```bash
   .\bin\GAME_APPLICATION.exe
   ```

---

## 🛠️ Yapılan Özelleştirmeler ve Geliştirmeler

1. **VERTEX Teması ve Görselleri:**
   - **Duvar Dokuları:** Orijinal duvar kaplamaları ile `subliminal1.png` görseli %50 oranında yarı şeffaf olarak harmanlanarak sisteme yedirildi.
   - **Granny Modeli:** Granny'nin kaplaması tamamen `subliminal2.png` görseliyle değiştirildi.
   - **UI Ekranları:** Başlangıç Menüsü, Kazanma (Win) ve Kaybetme (Lose) ekranları tamamen premium koyu tema (SaaS - Linear/Raycast tarzı) ile yeniden tasarlandı.
   - **Gizli Detaylar:** Vertex şirket bilgileri, Cortex ve Solar Browser projelerinin detayları ekranların sol tarafına terminal tanı koyma logları olarak gizlendi.

2. **Türkçe Çeviri:**
   - Oyun içi tüm ipuçları ve yönlendirmeler Türkçe'ye çevrildi.
   - Arayüz elemanları ve "Lives" göstergesi ("Canlar") Türkçe yapıldı.

3. **C++ Hata Düzeltmeleri:**
   - `entity.hpp` dosyasındaki C++ şablon fonksiyonu yazım ve silme hataları giderildi.
   - Windows API makro çakışmaları (`near`/`far`) engellendi.
   - MSVC-MinGW C++ ABI uyumsuzluğundan kaynaklanan **IrrKlang** ses kütüphanesi linker hatası, DLL'in çalışma zamanında dinamik olarak çağrılmasıyla (`LoadLibraryA` ve `GetProcAddress` kullanılarak) çözüldü.

---

## 🌟 Vertex Hakkında
**Vertex**, yapay zeka, yazılım ve oyun dünyasında devrim yaratan Türkiye'nin en genç teknoloji şirketidir. 
* **Cortex:** Yapay zeka sektöründe çığır açan teknoloji.
* **Solar Browser:** İnternet ve kozmosa giden anahtar.

---

*VertexCorporation (https://github.com/VertexCorporation) vizyonuyla geliştirilmiştir.*
