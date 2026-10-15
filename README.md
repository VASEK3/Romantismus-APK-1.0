# Romantismus – Android aplikace (GitHub Actions)

Offline kolo štěstí s 8 otázkami a kvíz s 10 otázkami. APK lze sestavit **bez počítače** přes GitHub.

## Postup jen na telefonu

1. V telefonu rozbal ZIP `Romantismus_GitHub_APK.zip`.
2. Na **github.com** se přihlas a vytvoř nový **veřejný nebo soukromý** repozitář, například `romantismus-apk` (Add README nezaškrtávej).
3. Nahraj **obsah rozbalené složky** do kořene repozitáře, nikoli ZIP jako jeden soubor. Musí tam být `app`, `.github`, `build.gradle.kts`, `settings.gradle.kts` atd. DŮLEŽITÉ: soubor `.github/workflows/build-apk.yml` musí být na GitHubu přesně v této cestě. Mobilní nahrávání složek někdy nefunguje – použij v prohlížeči „Web pro počítač“, případně nahraj jednotlivé soubory přes GitHub web editor. Skrytou složku `.github` nezapomeň.
4. Otevři repozitář → **Actions** → **Sestavit Android APK** → **Run workflow** → **Run workflow**. Workflow se také spouští automaticky při push do `main` nebo `master`.
5. Po dokončení otevři zelený běh → sekce **Artifacts** → stáhni **Romantismus-APK** (ZIP).
6. Rozbal stažený ZIP. Uvnitř najdeš `app-debug.apk`, který můžeš nainstalovat nebo přeposlat odkazem.

### Když na GitHubu nevidíš Actions

Zkontroluj, zda je workflow v `.github/workflows/build-apk.yml` a zda jsou Actions pro repozitář povolené. Na mobilu může pomoci přepnout prohlížeč na desktopové zobrazení.

### Upozornění

- Jde o **debug APK** podepsané automatickým testovacím klíčem; pro osobní školní sdílení je vhodné. Není určené pro Google Play.
- Android při instalaci APK mimo obchod může požadovat povolení instalace z daného zdroje. Instaluj jen soubory, kterým důvěřuješ.
- Instagram zprávy obvykle neumožňují přiložit APK; pošli odkaz na stažení souboru (např. z cloudového úložiště).
- GitHub Actions při prvním sestavení stahuje závislosti. APK není předem sestavené a sestavení zde nebylo ověřeno.
- `app/src/main/assets/index.html` obsahuje samotnou hru a funguje offline.
