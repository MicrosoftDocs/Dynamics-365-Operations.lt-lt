---
title: "Iš naujo nustatyti finansinės atskaitomybės duomenų mart po duomenų bazės atkūrimas"
description: "Šioje temoje aprašoma, kaip iš naujo nustatyti finansinės atskaitomybės duomenų mart atkūrus Microsoft Dynamics 365 operacijos duomenų bazės."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Iš naujo nustatyti finansinės atskaitomybės duomenų mart po duomenų bazės atkūrimas

Šioje temoje aprašoma, kaip iš naujo nustatyti finansinės atskaitomybės duomenų mart atkūrus Microsoft Dynamics 365 operacijos duomenų bazės. 

Yra keli scenarijai, kur jums gali tekti savo dinamika 365 operacijos duomenų bazės atkurti iš atsarginės kopijos arba duomenų bazei kopijuoti iš kitos aplinkos. Kai taip atsitinka, jums taip pat reikia laikytis reikiamų priemonių siekdama užtikrinti, kad finansinės atskaitomybės duomenų saugyklą teisingai naudoja atnaujintame Dynamics 365 operacijos duomenų bazės. Jei turite klausimų apie naujo finansinės atskaitomybės duomenų mart priežasties ne atkurti Dynamics 365 operacijos duomenų bazės, perduoti į [iš naujo nustatyti valdymo reporteris duomenų mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) daugiau informacijos. Atkreipkite dėmesį, kad šio proceso etapus palaikomi Dynamics 365 darbui Gegužė 2016 išleidimo (App statyti 7.0.1265.23014 ir finansinės atskaitomybės statyti 7.0.10000.4) ir naujesnių versijų. Jei turite su ankstesne jos versija, Dynamics 365 operacijoms, susisiekite su mūsų klientų aptarnavimo komanda paramos.

## <a name="export-report-definitions"></a>Eksporto ataskaitos apibrėžimai
Pirma eksportuokite ataskaitą dizaino įsikūrusi ataskaitų konstruktorius, atlikite šiuos veiksmus:

1.  Ataskaitų konstruktorius, eikite į **įmonė**&gt;**statybinis blokas grupių**.
2.  Pasirinkite eksportuoti, ir spustelėkite kūrimo bloko grupę **eksportuoti**. **Pastaba:** Dynamics 365 operacijoms, palaikomas tik vieno pastato bloko grupė, **pagal nutylėjimą**.
3.  Pasirinkite eksportuoti ataskaitos apibrėžimai:
    -   Norėdami eksportuoti visus ataskaitos aprašus ir susietus kūrimo blokus, spustelėkite **Žymėti viską**.
    -   Norėdami eksportuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, spustelėkite atitinkamą skirtuką ir tada pasirinkite norimus eksportuoti elementus. Norėdami skirtuke pasirinkti keletą elementų, paspauskite ir laikykite nuspaudę CTRL klavišą. Kai pasirenkate eksportuoti ataskaitas, atrenkami susietas eilutes, stulpelius, medžiai ir židinius.

4.  Spustelėkite **eksportuoti**.
5.  Įveskite failo vardą ir pasirinkite saugioje vietoje, kur norite įrašyti eksportuojamas ataskaitos apibrėžimai.
6.  Click **Save**.

Failas gali būti nukopijuotas arba įkeltos į saugią vietą, ji galėtų būti importuojami į kitoje aplinkoje, kitą kartą. Galima rasti informacijos, kaip naudoti Microsoft Azure saugojimo sąskaitos [perduoti duomenis naudojant AzCopy komandų eilutės priemonę](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Pastaba:** "Microsoft" neteikia saugyklos abonementą kaip dalį savo dinamika 365 operacijų susitarimui. Turite įsigyti saugyklos abonementą arba naudoti saugojimo sąskaitos iš atskiros Azure prenumeratos. **Svarbu:** reikia žinoti apie elgesį D diske apie Azure virtualiųjų mašinų. Negalima laikyti eksportuojamos statybinis blokas grupių čia visam laikui. Daugiau informacijos apie laikinųjų diskus, rasite [suprasti laikinai automobiliu ant Windows Azure virtualiosios mašinos](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Sustabdyti paslaugas
Naudokite nuotolinį darbalaukį Norėdami jungtis prie visų kompiuterių aplinkoje ir sustabdyti šiuos "Windows" paslaugų naudodami services.msc:

-   Žiniatinklio leidybos paslaugos (visuose kompiuteriuose AOS)
-   Microsoft Dynamics 365 operacijų partijos valdymo paslaugos (valstybiniuose AOS kompiuteriai tik)
-   Valdymo reporteris 2012 procesas paslauga (kompiuteriuose, BI tik)

Šios paslaugos turi atvirą ryšį su Dynamics 365 operacijos duomenų bazės.

## <a name="reset"></a>Nustatyti iš naujo
#### <a name="locate-the-latest-dataupgradezip-package"></a>Raskite naujausią DataUpgrade.zip paketą

Raskite naujausią DataUpgrade.zip paketą naudodami rasti kryptimis [DataUpgrade.zip scenarijaus atsisiuntimas](..\migration-upgrade\upgrade-data-to-latest-update.md). Kryptimis paaiškinti, kaip rasti versija duomenų atnaujinimo paketą jūsų aplinkai.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Vykdyti scenarijus prieš Dynamics 365 operacijos duomenų bazės

Šiuos scenarijus paleisti Dynamics 365 operacijos duomenų bazės (ne prieš finansinės atskaitomybės duomenų bazę).

-   DataUpgrade.zip\\AosService\\scenarijai\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\scenarijai\\GrantAzViewChangeTracking.sql

Šie scenarijai užtikrinti, kad vartotojai, vaidmenis ir keitimų sekimo parametrai yra teisingi.

#### <a name="execute-powershell-command-to-reset-database"></a>"PowerShell" komandą nustatyti iš naujo duomenų bazės

Vykdyti šią komandą, tiesiai ant AOS kompiuterio, Norėdami iš naujo nustatyti integracijos dinamika 365 operacijoms ir finansinė atskaitomybė:

1.  Atidarykite "Windows PowerShell" kaip administratorius.
2.  Vykdyti: f
3.  Vykdyti: f cd\\MRApplicationService\\MRInstallDirectory
4.  Vykdyti: Importo modulis. \\Server\\MRDeploy\\MRDeploy.psd1
5.  Vykdyti: Reset-DatamartIntegration-priežastis kita - ReasonDetail "&lt;mano priežastis iš naujo&gt;"
    -   Jūsų bus paprašyta įvesti "Y", kad patvirtintumėte.

Parametrų paaiškinimas:

-   Leistinos reikšmės-priežastis yra: aptarnavimo, BADDATA, kitų.
-   -ReasonDetail parametras yra laisvos formos.
-   Priežastis ir reasonDetail bus registruojami telemetrija ir (arba) aplinkai stebėti.

## <a name="start-services"></a>Pradžia paslaugos
Naudokite services.msc iš naujo paleisti paslaugas, kurios nustojote anksčiau:

-   Žiniatinklio leidybos paslaugos (visuose kompiuteriuose AOS)
-   Microsoft Dynamics 365 operacijų partijos valdymo paslaugos (valstybiniuose AOS kompiuteriai tik)
-   Valdymo reporteris 2012 procesas paslauga (kompiuteriuose, BI tik)

## <a name="import-report-definitions"></a>Importo ataskaitos apibrėžimai
Importuoti savo ataskaitos dizainą iš ataskaitų konstruktorius, naudojant sukurtas eksportavimo failas:

1.  Ataskaitų konstruktorius, eikite į **įmonė**&gt;**statybinis blokas grupių**.
2.  Pasirinkite eksportuoti, ir spustelėkite kūrimo bloko grupę **eksportuoti**. **Pastaba:** Dynamics 365 operacijoms, palaikomas tik vieno pastato bloko grupė, **pagal nutylėjimą**.
3.  Pasirinkite, **pagal nutylėjimą** pastato blokas ir spustelėkite **importo**.
4.  Pasirinkite failą, kuriame yra eksportuojami ataskaitos apibrėžimai ir spustelėkite **atviras**.
5.  Dialogo lange Importuoti pasirinkite norimus importuoti ataskaitos aprašus.
    -   Norėdami importuoti visus ataskaitos aprašus ir palaikomus kūrimo blokus, spustelėkite **Žymėti viską**.
    -   Norėdami importuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, pasirinkite norimas importuoti ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius.

6.  Click **Import**.



