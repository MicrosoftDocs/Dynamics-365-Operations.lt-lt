---
title: "Finansinių ataskaitų duomenų srities atstatymas atkūrus duomenų bazę"
description: "Šioje temoje paaiškinama, kaip galima atstatyti finansinių ataskaitų duomenų sritį atkūrus „Microsoft Dynamics 365 for Operations“ duomenų bazę."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d4ce390c62cbfb1f693410b004aa296c0ed75eb2
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Finansinių ataskaitų duomenų srities atstatymas atkūrus duomenų bazę

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip galima atstatyti finansinių ataskaitų duomenų sritį atkūrus „Microsoft Dynamics 365 for Operations“ duomenų bazę. 

Yra keletas scenarijų, kuriais vadovaujantis reikėtų atkurti „Dynamics 365 for Operations“ duomenų bazę iš atsarginės kopijos arba nukopijuoti duomenų bazę iš kitos aplinkos. Jei taip įvyktų, taip pat turite atlikti atitinkamus veiksmus, kad užtikrintumėte, jog finansinių ataskaitų duomenų sritis tinkamai naudoja atkurtą „Dynamics 365 for Operations“ duomenų bazę. Jeigu turite klausimų apie tai, kaip iš naujo nustatyti finansinių ataskaitu duomenų sritį dėl kitokios priežasties negu „Dynamics 365 for Operations“ duomenų bazės atkūrimas, daugiau informacijos rasite [„Management Reporter“ duomenų srities nustatymas iš naujo](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/). Atkreipkite dėmesį, kad šio proceso veiksmai palaikomi naudojant „Dynamics 365 for Operation“ 2016 m. gegužės mėn. leidimą (programos versija 7.0.1265.23014 ir finansinės ataskaitos versija 7.0.10000.4) ir naujesnius leidimus. Jeigu naudojate ankstesnį „Dynamics 365 for Operations“ leidimą, susisiekite su mūsų palaikymo komanda.

## <a name="export-report-definitions"></a>Ataskaitų aprašų eksportavimas
Pirmiausia atlikite toliau nurodytus veiksmus ir eksportuokite ataskaitų dizaino įrankyje esančius ataskaitos dizainus.

1.  Įjungę atskaitos dizaino įrankį eikite į **Įmonė** &gt; **Kūrimo bloko grupės**.
2.  Norėdami eksportuoti, pasirinkite kūrimo blokų grupę ir spustelėkite **Eksportuoti**. **Pastaba:** Naudojant „Dynamics 365 for Operations“ palaikoma tik viena kūrimo blokų grupė **Numatytoji**.
3.  Pasirinkite norimus eksportuoti ataskaitos aprašus:
    -   Norėdami eksportuoti visus ataskaitos aprašus ir susietus kūrimo blokus, spustelėkite **Žymėti viską**.
    -   Norėdami eksportuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, spustelėkite atitinkamą skirtuką ir tada pasirinkite norimus eksportuoti elementus. Norėdami skirtuke pasirinkti keletą elementų, paspauskite ir laikykite nuspaudę CTRL klavišą. Pažymėjus norimas eksportuoti ataskaitas pažymimos susietos eilutės, stulpeliai, medžiai ir dimensijų rinkiniai.

4.  Spustelėkite **Eksportuoti**.
5.  Įveskite failo pavadinimą ir pasirinkite saugią vietą, kurioje norite įrašyti eksportuotus ataskaitos aprašus.
6.  Spustelėkite **Įrašyti**.

Failą galima nukopijuoti arba įkelti į saugią vietą, kad būtų galima jį importuoti į kitą aplinką kitu laiku. Informaciją apie tai, kaip naudoti „Microsoft Azure“ saugyklos abonementą, galima rasti [Perkelti duomenis naudojant „AzCopy“ komandų eilučių programą](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Pasirašius „Dynamics 365 for Operations“ sutartį „Microsoft“ nesuteikia saugyklos paskyros. Turite įsigyti saugyklos abonementą arba naudoti saugyklos abonementą iš atskiros „Azure“ prenumeratos. 
> [!WARNING]
> Atkreipkite dėmesį į D disko elgseną „Azure“ virtualiuosiuose įrenginiuose. Nelaikykite čia savo eksportuotų kūrimo blokų grupių visam laikui. Norėdami gauti daugiau informacijos apie laikinus diskus, žr. [„Windows Azure“ virtualiųjų įrenginių laikinųjų diskų supratimas](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Tarnybų stabdymas
Norėdami prisijungti prie visų aplinkos kompiuterių naudokite nuotolinį darbalaukį, o norėdami sustabdyti toliau nurodytas „Windows“ tarnybas – services.msc.

-   Žiniatinklio tarnybos publikavimo paslauga (visuose AOS kompiuteriuose)
-   „Microsoft Dynamics 365 for Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)
-   „Management Reporter 2012“ proceso tarnyba (tik BI kompiuteriuose)

Šios tarnybos turi atvirus ryšius su „Dynamics 365 for Operations“ duomenų baze.

## <a name="reset"></a>Nustatyti iš naujo
#### <a name="locate-the-latest-dataupgradezip-package"></a>Suraskite naujausią DataUpgrade.zip pakuotę

Naudodami [Atsisiųsti DataUpgrade.zip scenarijų](..\migration-upgrade\upgrade-data-to-latest-update.md) rastus nurodymus suraskite naujausią DataUpgrade.zip pakuotę. Nurodymuose paaiškinama, kaip surasti jūsų aplinkai tinkamą duomenų atnaujinimo pakuotės versiją.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Scenarijų vykdymas „Dynamics 365 for Operations“ duomenų bazėje

Toliau nurodytus scenarijus vykdykite „Dynamics 365 for Operations“ duomenų bazėje (ne finansinių ataskaitų duomenų bazėje).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Naudojant šiuos scenarijus užtikrinama, kad naudojami tinkami vartotojų, vaidmenų ir keitimų sekimo paametrai.

#### <a name="execute-powershell-command-to-reset-database"></a>„PowerShell“ komandos vykdymas norint iš naujo nustatyti duomenų bazę

Toliau nurodytą komandą vykdykite tiesiogiai savo AOS kompiuteryje, kad iš naujo nustatytumėte „Dynamics 365 for Operations“ ir finansinių ataskaitų integravimą:

1.  Atidarykite „Windows PowerShell“ kaip administratorius.
2.  Vykdyti: F:
3.  Vykdyti: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Vykdyti: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  Vykdyti: Nustatyti iš naujo-DatamartIntegration -Priežastis KITA -ReasonDetail „&lt;mano nustatymo iš naujo priežastis&gt;“
    -   Jūsų bus paprašyta įvesti „Y“, kad patvirtintumėte.

Parametrų paaiškinimas:

-   Tinkamos dalies -Priežastis reikšmės yra šios: SERVICING, BADDATA, OTHER.
-   Parametras -ReasonDetail yra laisvos formos.
-   Priežastis ir „reasonDetail“ bus įrašyti atliekant telemetriją / aplinkos stebėjimą.

## <a name="start-services"></a>Tarnybų paleidimas
Naudokite services.msc norėdami iš naujo paleisti pirmiau sustabdytas tarnybas:

-   Žiniatinklio tarnybos publikavimo paslauga (visuose AOS kompiuteriuose)
-   „Microsoft Dynamics 365 for Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)
-   „Management Reporter 2012“ proceso tarnyba (tik BI kompiuteriuose)

## <a name="import-report-definitions"></a>Ataskaitų aprašų importavimas
Importuokite savo ataskaitos dizainus iš ataskaitų dizaino įrankio naudodami eksportuojant sukurtą failą.

1.  Įjungę atskaitos dizaino įrankį eikite į **Įmonė** &gt; **Kūrimo bloko grupės**.
2.  Norėdami eksportuoti, pasirinkite kūrimo blokų grupę ir spustelėkite **Eksportuoti**. 
    > [!NOTE]
    > Naudojant „Dynamics 365 for Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.
3.  Pasirinkite kūrimo bloką **Numatytasis** ir spustelėkite **Importuoti**.
4.  Pasirinkite failą, kuriame yra eksportuoti ataskaitos aprašai, ir spustelėkite **Atidaryti**.
5.  Dialogo lange Importuoti pasirinkite norimus importuoti ataskaitos aprašus.
    -   Norėdami importuoti visus ataskaitos aprašus ir palaikomus kūrimo blokus, spustelėkite **Žymėti viską**.
    -   Norėdami importuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, pasirinkite norimas importuoti ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius.

6.  Spustelėkite **Importuoti**.





