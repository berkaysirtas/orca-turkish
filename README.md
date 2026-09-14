# Orca için Türkçe dil paketi

[Orca](https://github.com/stablyai/orca) (Stably AI'nin ajan geliştirme ortamı) arayüzünü Türkçeleştiren eklenti. Uygulamaya dokunmaz, Orca'nın kendi `contributes.languagePacks` mekanizmasıyla yüklenir. Çevrilmemiş metinler otomatik olarak İngilizce görünür.

*Turkish language pack for the Orca ADE. Installs as a normal Orca plugin; untranslated strings fall back to English.*

## Kurulum

1. **Settings → Plugins**: eklenti sistemini aç.
2. **Install plugin → Git URL**: sürüm etiketiyle birlikte yapıştır (Orca etiketsiz adresi kabul etmez):

   ```
   https://github.com/berkaysirtas/orca-turkish.git#v0.2.0
   ```

3. **Settings → Appearance → Language**: **Türkçe** seç.

Yerelde geliştirmek için: **Settings → Plugins → Development → Add path** ile bu klasörü ekle; `locales/tr.json` değişince Orca yeniden okur.

## Durum

Sürüm 0.2.0, Orca `>=1.4.0`, 215 anahtar. Menü, tepsi, dil ayarları, durum çubuğu, uzak tarayıcı ayarları, worktree atlama paleti, ajan panosu, ajan sekmesi tanıtımı, CLI başlangıç hatası ve kurtarma ekranları çevrildi. Kalan katalog kademeli olarak ekleniyor; bir sonraki sürümde ayarlar ve kenar çubuğu bölümleri gelecek.

Katalog, Orca deposundaki `pnpm scaffold:language-pack` aracıyla üretiliyor ve doğrulanıyor (bkz. stablyai/orca#20513): korumalı anahtarlar, yer tutucu uyumu ve katalog sınırları her sürümde denetleniyor.

## Katkı

Çeviri önerisi ya da düzeltme için issue aç ya da `locales/tr.json` üzerinde PR gönder. Terim tutarlılığı:

| English | Türkçe | Not |
|---|---|---|
| workspace | çalışma alanı | |
| worktree | worktree | `git worktree` komut adı, çevrilmez |
| agent | ajan | |
| session | oturum | |
| pull request | PR | kısaltma korunur |
| pane | bölme | |
| status bar | durum çubuğu | |

Em dash kullanılmaz; açıklama için virgül ya da iki nokta.

## Lisans

MIT. Orca, Stably AI'nin MIT lisanslı ürünüdür; İngilizce kaynak metinler Orca projesine aittir. Bu depo bağımsız bir topluluk çevirisidir, Stably AI ile bağlantısı yoktur.
