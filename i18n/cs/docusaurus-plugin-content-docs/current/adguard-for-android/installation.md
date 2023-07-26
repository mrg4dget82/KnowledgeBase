---
title: Instalace
sidebar_position: 2
---

:::info

Tento článek popisuje AdGuard pro Android, multifunkční blokátor reklam, který chrání vaše zařízení na úrovni systému. Chcete-li zjistit, jak funguje, [stáhněte si aplikaci AdGuard](https://adguard.com/download.html?auto=true)

:::

## Požadavky na systém

**Verze OS:** Android 7.0 nebo vyšší

**RAM:** alespoň 2 GB

**Volné místo na disku:** 500 MB

## Instalace

Většina aplikací pro Android je distribuována prostřednictvím služby Google Play. AdGuard zde však není prezentován, protože společnost Google zakazuje distribuci blokátorů reklam na úrovni sítě prostřednictvím služby Google Play, tj. aplikace, které blokují reklamy v jiných aplikacích. Další informace o restriktivní politice Google najdete v [našem blogu](https://blog.adguard.com/en/google-removes-adguard-android-app-google-play/).

Proto můžete AdGuard pro Android nainstalovat pouze ručně. Chcete-li aplikaci používat v mobilním zařízení, musíte provést následující kroky.

1. **Stáhněte si aplikaci do zařízení**. Zde je několik způsobů, jak to můžete udělat:

    * přejděte na [náš web](https://adguard.com/adguard-android/overview.html) a klepněte na tlačítko *Stáhnout*
    * spusťte prohlížeč a zadejte následující URL: [https://adguard.com/apk](https://adguard.com/apk)
    * nebo naskenujte tento QR kód

    ![QR code *mobile_border](https://cdn.adtidy.org/content/kb/ad_blocker/android/installation/inst_qr.png)

2. **Povolte instalaci aplikací z neznámých zdrojů**. Po dokončení stahování souboru klepněte na *Otevřít* v oznámení.

![Instalace aplikací z neznámých zdrojů *mobile_border](https://cdn.adtidy.org/content/kb/ad_blocker/android/installation/inst_1.png)

Zobrazí se vyskakovací okno. Klepněte na *Nastavení*, přejděte na *Instalace neznámých aplikací*a udělte oprávnění pro prohlížeč, který jste použili ke stažení souboru.

![Instalace aplikací z neznámých zdrojů *mobile_border](https://cdn.adtidy.org/content/kb/ad_blocker/android/installation/inst_3.png)

Tato příručka je pro systém Android 8+. Pokud máte starší verzi operačního systému, přejděte před stažením souboru APK do *Nastavení* a vyberte možnost *Další nastavení* v sekci *Systém a zařízení*. Povolte *Neznámé zdroje* a klepněte na *OK* v okně se systémovým varováním.

3. **Nainstalujte aplikaci**. Jakmile prohlížeč získá potřebná oprávnění, systém se vás zeptá, zda chcete aplikaci AdGuard nainstalovat. Klepněte na *Instalovat*.

![Instalace aplikací z neznámých zdrojů *mobile_border](https://cdn.adtidy.org/content/kb/ad_blocker/android/installation/inst_4.png)

Poté budete požádáni o přečtení *licenční smlouvy AdGuard* a *Zásad ochrany osobních údajů*. Můžete se také podílet na vývoji produktů. Za tímto účelem můžete zaškrtnout políčka *Odesílat automatická hlášení o pádech* a *Odesílat technická a interakční data*. Klepněte na *Pokračovat*.

![Zásady ochrany osobních údajů *mobile_border](https://cdn.adtidy.org/content/kb/ad_blocker/android/installation/fl_3.png)

4. **Vytvořte lokální VPN**. Aby bylo možné filtrovat veškerý provoz přímo v zařízení a nesměrovat jej přes vzdálený server, musí AdGuard navázat spojení VPN.

![Vytvoření lokální VPN *mobile_border](https://cdn.adtidy.org/content/kb/ad_blocker/android/installation/fl_2.png)

5. **Povolte HTTPS filtrování**. Není to povinná volba, ale doporučujeme ji zapnout, abyste dosáhli nejlepší kvality blokování reklam.

Pokud vaše zařízení používá systém Android 7-9, budete po nastavení lokální VPN vyzváni k instalaci kořenového certifikátu a konfiguraci HTTPS filtrování.

![Povolení HTTPS filtrování v systému Android 7-9 *mobile_border](https://cdn.adtidy.org/content/kb/ad_blocker/android/installation/cert_1.jpg)

Po klepnutí na *Instalovat nyní* se zobrazí výzva k ověření instalace certifikátu pomocí hesla nebo otisku prstu.

![Povolení HTTPS filtrování v systému Android 7-9. Krok 2 *mobile_border](https://cdn.adtidy.org/content/kb/ad_blocker/android/installation/cert_2.jpg)

Pokud máte v zařízení Android 10+, zobrazí se po vytvoření lokální VPN hlavní obrazovka aplikace s lištou ve spodní části: klepněte na *Povolit* a postupujte podle pokynů na další obrazovce.

![Povolení HTTPS filtrování *mobile_border](https://cdn.adtidy.org/content/kb/ad_blocker/android/installation/fl_5.png)

## Odinstalování/přeinstalování AdGuardu

Pokud potřebujete AdGuard v mobilním zařízení znovu nainstalovat, nejprve jej odstraňte otevřením **Nastavení** a výběrem **Aplikace** (Android 7) nebo **Aplikace a oznámení** (Android 8+). Vyhledejte **AdGuard** v seznamu nainstalovaných aplikací a stiskněte **Odinstalovat**.

![Přeinstalace AdGuardu *mobile_border](https://cdn.adtidy.org/content/kb/ad_blocker/android/installation/inst_4.png)

Chcete-li aplikaci znovu nainstalovat, zopakujte úkony popsané v části Instalace.
