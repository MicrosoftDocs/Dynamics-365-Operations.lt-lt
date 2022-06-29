---
title: Pradėkite darbą su Visuotine atsargų apskaita
description: Šiame straipsnyje aprašoma, kaip pradėti nuo visuotinės atsargų apskaitos.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cbe6bff6fab96900b8bd4e112a8858363fff86d1
ms.sourcegitcommit: 9870b773a2ea8f5675651199fdbc63ca7a1b4453
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013561"
---
# <a name="get-started-with-global-inventory-accounting"></a>Pradėkite darbą su Visuotine atsargų apskaita

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Visuotinė atsargų apskaita leidžia jums atlikti kelias atsargų apskaitas Visuotinės atsargų apskaitos didžiosiose knygose, kurias nustatėte. Turite susieti kiekvieną Visuotinės atsargų apskaitos didžiąją knygą su *konvencija*. Konvencija yra toliau pateiktų apskaitos strategijų tipų rinkinys.

- Savikainos objektas
- Įeigos matavimo vieneto pagrindas
- Savikainos srauto numanymas
- Savikainos elementas

> [!NOTE]
> Netgi įjungę Visuotinę atsargų apskaitą, galite atlikti atsargų apskaitą „Microsoft Dynamics 365 Supply Chain Management” įprastu būdu.

Visuotinė atsargų apskaita yra papildinys. Turite ją įdiegti iš „Microsoft Dynamics Lifecycle Services” (LCS), kad jos funkcijos būtų prieinamos. Prieš įjungdami paslaugą gamybos aplinkose galite pasirinkti, kad ji būtų įvertinta testavimo aplinkoje.

Visuotinė atsargų apskaita šiuo metu nepalaiko visų išlaidų valdymo priemonių, kurios yra įtrauktos į „Supply Chain Management”. Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti, atitiks jūsų reikalavimus.

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a> Kaip gauti visuotinių atsargų apskaitos priedą

> [!IMPORTANT]
> Norėdami naudoti Visuotinę atsargų apskaitą, privalote turėti LCS įgalintą didelio užimtumo aplinką (ne „OneBox” aplinką). Be to, turite paleisti 10.0.19 ar vėlesnę „Supply Chain Management” versiją.

### <a name="supply-chain-management-version-10019-to-10026"></a>Tiekimo grandinės valdymo versija nuo 10.0.19 iki 10.0.26

Norėdami įdiegti tiekimo grandinės valdymo versiją nuo 10.0.19 iki 10.0.26 visuotinę atsargų apskaitą, [pradėkite diegti priedą](#install). Tada LCS aplinkos ID ir įmonės pavadinimą siųskite el. paštu visuotinės [atsargų apskaitos komandai](mailto:GlobalInvAccount@microsoft.com). Komanda išsiųs jums tolesnės informacijos el. laišką, kuriame yra jūsų visuotinių atsargų apskaitos paslaugų galiniai punktai.

### <a name="supply-chain-management-version-10027-and-later"></a>Tiekimo grandinės valdymo versija 10.0.27 ir vėlesnė

Norėdami įdiegti tiekimo grandinės valdymo 10.0.27 ir naujesnės versijos visuotinę atsargų apskaitą, [tiesiog įdiekite priedą](#install). Šiose tiekimo grandinės valdymo versijose visuotiniai atsargų apskaitos tarnybos galiniai punktai bus nustatyti automatiškai, todėl jų reikės rasti rankiniu būdu. Jei nustatydami papildinį patiriate kokių nors problemų, kreipkitės į visuotinės [atsargų apskaitos komandą](mailto:GlobalInvAccount@microsoft.com).

## <a name="licensing"></a>Licencijavimas

Visuotinė atsargų apskaita licencijuojama kartu su standartinėmis atsargų apskaitos funkcijomis, kurios pasiekiamos „Supply Chain Management”. Nereikia pirkti papildomos licencijos, norint naudoti Visuotinę atsargų apskaitą.

## <a name="prerequisites"></a>Būtinieji komponentai

### <a name="set-up-microsoft-power-platform-integration"></a>Nustatyti „Microsoft Power Platform“ integravimą

Kad būtų galima įgalinti papildinio funkcionalumą, turite jį integruoti su „Microsoft Power Platform” atlikdami šiuos veiksmus.

1. Atidarykite LCS aplinką, į kurią norite įtraukti paslaugą.
1. Eikite į **Išsami informacija**.
1. **„Power Platform“ integravimas** srityje rinkitės **Nustatymas**.
1. Dialogo lange **„Power Platform” aplinkos nustatymas** pasirinkite žymės langelį, o tada – **Nustatymas**. Įprastai nustatymas trunka nuo 60 iki 90 minučių.
1. Baigus „Microsoft Power Platform” aplinkos nustatymą, puslapyje rodomas jūsų aplinkos pavadinimas. Be to, **„Power Platform” integravimo** skyriuje rodomas sakinys: „'Power Platform' aplinkos nustatymas yra baigtas.” Visuotinei atsargų apskaitai nereikia dvigubo rašymo prašymo.

Daugiau informacijos rasite [Įjungimas po aplinkos diegimo](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="install-the-add-in"></a><a name="install"></a>Papildinio įdiegimas

Atlikite šiuos veiksmus, kad įdiegtumėte priedą, skirtą Visuotinės atsargų apskaitos naudojimui.

1. Prisijunkite prie [LCS](https://lcs.dynamics.com/Logon/Index).
1. Atidarykite LCS aplinką, į kurią norite įtraukti paslaugą.
1. Eikite į **Išsami informacija**.
1. Eikite į **„Power Platform” integravimas** ir pasirinkite **Nustatymas**.
1. Dialogo lange **„Power Platform” aplinkos nustatymas** pasirinkite žymės langelį, o tada – **Nustatymas**. Įprastai nustatymas trunka nuo 60 iki 90 minučių.
1. Užbaigę aplinkos Microsoft Power Platform nustatymą, prisiregistruokite [Power Platform prie administravimo](https://admin.powerplatform.microsoft.com) centro ir įdiekite visuotinio atsargų apskaitos priedą, atlikdami šiuos veiksmus:
   1. Pasirinkite aplinką, kurioje norite įdiegti priedą.
   1. Pasirinkite " **Dynamics 365" programėles**.
   1. Pasirinkite **įdiegti programą**.
   1. Pasirinkite **"Dynamics 365" visuotinių atsargų apskaita**.
   1. Pasirinkite **Pirmyn,** jei norite įdiegti.
1. Grįžkite į LCS aplinką. „FastTab” **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.
1. Pasirinkite **Visuotinė atsargų apskaita**.
1. Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.
1. Pasirinkti **Diegti**.
1. „FastTab” **Aplinkos papildiniai** turėtumėte matyti, kad Visuotinė atsargų apskaita yra diegiama. Po kelių minučių būsena turėtų pasikeisti iš *Diegiama* į *Įdiegta*. (Gali reikėti atnaujinti puslapį, kad pamatytumėte šį pakeitimą.) Tada Visuotinė atsargų apskaita bus parengta naudoti.

Jei jūsų diegimo numatytoji kalba yra Dataverse ne anglų kalba, atlikite šiuos veiksmus:
1. Eikite į **Išplėstiniai parametrai \> Administravimas \> Kalbos**.
1. Pasirinkite *Anglų* (*LanguageCode (Kalbos kodas)=1033*), o tada – **Taikyti**.

## <a name="set-up-the-integration"></a>Integravimo nustatymas

Norėdami nustatyti integravimą tarp Visuotinės atsargų apskaitos ir „Supply Chain Management”, atlikite šiuos veiksmus.

1. Prisijunkite prie „Supply Chain Management“.
1. Eikite į **Sistemos administravimas \> Funkcijų valdymas**.
1. Pasirinkite **Tikrinti, ar yra naujinimų**.
1. Skirtuke **Visi** ieškokite priemonės, kuri pavadinta *(Peržiūra) Visuotinių atsargų apskaita*.
1. Pasirinkite **Įjungti dabar**.
1. Eikite į **Visuotinė atsargų apskaita \> Nustatymas \> Visuotinės atsargų apskaitos parametrai \> Integravimo parametrai**.
1. Atsižvelgdami į tai, kokią tiekimo grandinės valdymo versiją naudojate, atlikite vieną iš šių veiksmų:
    - **Tiekimo grandinės valdymo 10.0.19 versija 10.0.26**: **·** **duomenų** paslaugos galinio punkto ir visuotinių atsargų apskaitos galinio punkto laukuose įveskite URL, kurie buvo išsiųsti el. paštu iš visuotinės atsargų apskaitos komandos ([taip](#sign-up) pat žr. kaip gauti visuotinių atsargų apskaitos priedą).
    - **Tiekimo grandinės valdymo versija 10.0.27** ir naujesnė versija: jums nereikia įvesti galinių punktų, todėl galite praleisti šį veiksmą.

Visuotinė atsargų apskaita dabar yra parengta naudoti.
