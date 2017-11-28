---
title: "Finansinių ataskaitų duomenų srities atstatymas atkūrus duomenų bazę"
description: "Šioje temoje paaiškinama, kaip galima atstatyti finansinių ataskaitų duomenų sritį atkūrus „Microsoft Dynamics 365 for Finance and Operations“ duomenų bazę."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e3f78fb2f6528449d2a411225cd0e14ca33443e
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Finansinių ataskaitų duomenų srities atstatymas atkūrus duomenų bazę

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip galima atstatyti finansinių ataskaitų duomenų sritį atkūrus „Microsoft Dynamics 365 for Finance and Operations“ duomenų bazę.

Jei atkuriate „Finance and Operations“ duomenų bazę iš atsarginės kopijos arba duomenų bazės iš kitos aplinkos, atlikite temoje nurodytus veiksmus, kad užtikrintumėte tinkamą finansinių ataskaitų nustatymo naudojimą atkurtoje „Finance and Operations“ duomenų bazėje. 
> [!Note] 
> Šio proceso veiksmai palaikomi naudojant „Dynamics 365 for Operation“ 2016 m. gegužės mėn. leidimą (programos versija 7.0.1265.23014 ir finansinės ataskaitos versija 7.0.10000.4) ir naujesnius leidimus. Jeigu naudojate ankstesnį „Finance and Operations“ leidimą, pagalbos kreipkitės į mūsų palaikymo komandą.

## <a name="export-report-definitions"></a>Ataskaitų aprašų eksportavimas
Pirmiausia atlikite toliau nurodytus veiksmus ir eksportuokite ataskaitų dizaino įrankyje esančius ataskaitos dizainus.

1.  Įjungę atskaitos dizaino įrankį eikite į **Įmonė** &gt; **Kūrimo bloko grupės**.
2.  Norėdami eksportuoti, pasirinkite kūrimo blokų grupę ir spustelėkite **Eksportuoti**. 

    > [!Note] 
    > Naudojant „Finance and Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.
    
3.  Pasirinkite norimus eksportuoti ataskaitos aprašus:
    -   Norėdami eksportuoti visus ataskaitos aprašus ir susietus kūrimo blokus, spustelėkite **Žymėti viską**.
    -   Norėdami eksportuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, spustelėkite atitinkamą skirtuką ir tada pasirinkite norimus eksportuoti elementus. Norėdami pasirinkti keletą skirtuko elementų, paspauskite ir laikykite klavišą „Ctrl“. Pažymėjus norimas eksportuoti ataskaitas, pažymimos susietos eilutės, stulpeliai, medžiai ir dimensijų rinkiniai.

4.  Spustelėkite **Eksportuoti**.
5.  Įveskite failo pavadinimą ir pasirinkite saugią vietą, kurioje norite įrašyti eksportuotus ataskaitos aprašus.
6.  Spustelėkite **Įrašyti**.

Failą galima nukopijuoti arba įkelti į saugią vietą, kad būtų galima jį importuoti į kitą aplinką kitu laiku. Informaciją apie tai, kaip naudoti „Microsoft Azure“ saugyklos abonementą, galima rasti [Perkelti duomenis naudojant „AzCopy“ komandų eilučių programą](/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Pasirašius „Finance and Operations“ sutartį „Microsoft“ nesuteikia saugyklos paskyros. Turite įsigyti saugyklos abonementą arba naudoti saugyklos abonementą iš atskiros „Azure“ prenumeratos. 
> [!WARNING]
> Atkreipkite dėmesį į D disko elgseną „Azure“ virtualiuosiuose įrenginiuose. Nelaikykite čia savo eksportuotų kūrimo blokų grupių visam laikui. Norėdami gauti daugiau informacijos apie laikinus diskus, žr. [„Windows Azure“ virtualiųjų įrenginių laikinųjų diskų supratimas](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Tarnybų stabdymas
Norėdami prisijungti prie visų aplinkos kompiuterių naudokite nuotolinį darbalaukį, o norėdami sustabdyti toliau nurodytas „Windows“ tarnybas – services.msc.

-   Žiniatinklio tarnybos publikavimo paslauga (visuose AOS kompiuteriuose)
-   „Microsoft Dynamics 365 for Finance and Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)
-   „Management Reporter 2012“ proceso tarnyba (tik BI kompiuteriuose)

Šios tarnybos turi atvirus ryšius su „Finance and Operations“ duomenų baze.

## <a name="reset"></a>Nustatyti iš naujo
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>Raskite ir atsisiųskite naujausią MinorVersionDataUpgrade.zip paketą

Raskite naujausią MinorVersionDataUpgrade.zip paketą atsižvelgdami į nurodymus, pateiktus [Naujausių duomenų naujinimo diegimo paketų atsisiuntimas](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). Nurodymuose paaiškinama, kaip rasti ir atsisiųsti tinkamą duomenų atnaujinimo pakuotės versiją. Naujinant nėra būtina atsisiųsti MinorVersionDataUpgrade.zip paketo. Būtina atlikti veiksmus nurodytus skyriuje „Naujausių duomenų naujinimo diegimo paketų atsisiuntimas“ neatliekant jokių kitų straipsnyje nurodytų veiksmų, kad gautumėte MinorVersionDataUpgrade.zip paketo kopiją.

### <a name="execute-scripts-against-finance-and-operations-database"></a>Scenarijų vykdymas pagal „Finance and Operations“ duomenų bazę

Toliau nurodytus scenarijus vykdykite pagal „Finance and Operations“ duomenų bazę (ne pagal finansinių ataskaitų duomenų bazę).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Naudojant šiuos scenarijus užtikrinama, kad naudojami tinkami vartotojų, vaidmenų ir keitimų sekimo paametrai.

### <a name="execute-powershell-command-to-reset-database"></a>„PowerShell“ komandos vykdymas norint iš naujo nustatyti duomenų bazę

AOS kompiuteryje naudodami „PowerShell“ administratoriaus teisėmis vykdykite toliau nurodytas komandas, kad iš naujo nustatytumėte „Finance and Operations“ ir finansinių ataskaitų integravimą.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> Įvykdžius komandas jūsų bus paprašyta įvesti „Y“, kad patvirtintumėte.

Parametrų paaiškinimas:

-   Tinkamos dalies -Priežastis reikšmės yra šios: SERVICING, BADDATA, OTHER.
-   Parametras -ReasonDetail yra laisvos formos.
-   Priežastis ir „reasonDetail“ bus įrašyti atliekant telemetriją / aplinkos stebėjimą.

## <a name="start-services"></a>Tarnybų paleidimas
Naudokite services.msc norėdami iš naujo paleisti pirmiau sustabdytas tarnybas:

-   Žiniatinklio tarnybos publikavimo paslauga (visuose AOS kompiuteriuose)
-   „Microsoft Dynamics 365 for Finance and Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)
-   „Management Reporter 2012“ proceso tarnyba (tik BI kompiuteriuose)

## <a name="import-report-definitions"></a>Ataskaitų aprašų importavimas
Importuokite savo ataskaitos dizainus iš ataskaitų dizaino įrankio naudodami eksportuojant sukurtą failą.

1.  Įjungę atskaitos dizaino įrankį eikite į **Įmonė** &gt; **Kūrimo bloko grupės**.
2.  Norėdami eksportuoti, pasirinkite kūrimo blokų grupę ir spustelėkite **Eksportuoti**. 

    > [!NOTE]
    > Naudojant „Finance and Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.
    
3.  Pasirinkite kūrimo bloką **Numatytasis** ir spustelėkite **Importuoti**.
4.  Pasirinkite failą, kuriame yra eksportuoti ataskaitos aprašai, ir spustelėkite **Atidaryti**.
5.  Dialogo lange Importuoti pasirinkite norimus importuoti ataskaitos aprašus.
    -   Norėdami importuoti visus ataskaitos aprašus ir palaikomus kūrimo blokus, spustelėkite **Žymėti viską**.
    -   Norėdami importuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, pasirinkite norimas importuoti ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius.

6.  Spustelėkite **Importuoti**.





