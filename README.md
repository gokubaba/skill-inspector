# skill-inspector

Claude'a eklenecek skill ve eklentileri kurmadan önce [NVIDIA SkillSpector](https://github.com/NVIDIA/SkillSpector) ile tarayan küçük bir GitHub Actions deposu.

## Nasıl çalışır

1. **Actions › SkillSpector taraması › Run workflow**
2. `target` alanına taranacak GitHub reposunu yaz (ör. `https://github.com/kepano/obsidian-skills`).
3. Gerekirse `subdir` ile repo içinde bir klasör seç.
4. Tarama bitince rapor `reports/` klasörüne `.md` ve `.json` olarak kaydedilir ve çalışmanın özet sayfasında görünür.

## Kurallar

- Yalnızca statik tarama (`--no-llm`); hiçbir API anahtarı kullanılmaz.
- Hedef repo sadece indirilir; içindeki hiçbir script çalıştırılmaz.
- SkillSpector sabit bir commit'e bağlıdır (`SKILLSPECTOR_REF`).
- Skor tek başına karar değildir. Son karar (`APPROVE` / `CAUTION` / `REJECT`) raporla birlikte kaynak kod incelenerek verilir.
