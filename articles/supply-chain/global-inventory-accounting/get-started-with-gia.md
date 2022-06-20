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
ms.openlocfilehash: 493e0be8ab56abc2a3253876107b7f4fefabf4ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891095"
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

### <a name="set-up-dataverse"></a>Nustatyti Dataverse

Prieš nustatydami „Dataverse”, įtraukite Visuotinės atsargų apskaitos tarnybos principus savo nuomininkui atlikdami šiuos veiksmus.

1. Įdiekite „Azure AD“ modulį, skirtą „Windows” „PowerShell“ v2, kaip aprašyta skyriuje [„Azure Active Directory“ „PowerShell for Graph“ diegimas](/powershell/azure/active-directory/install-adv2).
1. Paleiskite šią „PowerShell“ komandą.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

Tada sukurkite programos vartotojus Visuotinei atsargų apskaitai „Dataverse” platformoje atlikdami šiuos veiksmus.

1. Atidarykite savo „Dataverse“ aplinkos URL.
1. Eikite į **Išplėstiniai nustatymai \> Sistema \> Sauga \> Naudotojai** ir sukurkite programos naudotoją. Naudokite lauką **Peržiūrėti**, kad pakeistumėte puslapio rodinį į *Programos naudotojai*.
1. Pasirinkite **Naujas**.
1. Nustatykite lauką **Programos ID** į *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.
1. Pasirinkite **Priskirti vaidmenį**, tada pasirinkite *Sistemos administratorius*. Jei yra vaidmuo, kuris vadinamas Vartotojas *Common Data Service*, pasirinkite jį taip pat.
1. Pakartokite ankstesnius veiksmus, tačiau nustatykite **Programos ID** lauką kaip *„5f58fc56-0202-49a8-ac9e-0946b049718b”*.

Daugiau informacijos žr. skyriuje [Programos naudotojo kūrimas](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

Jei numatytoji „Dataverse” diegimo kalba nėra anglų, atlikite šiuos veiksmus.

1. Eikite į **Išplėstiniai parametrai \> Administravimas \> Kalbos**.
1. Pasirinkite *Anglų* (*LanguageCode (Kalbos kodas)=1033*), o tada – **Taikyti**.

## <a name="install-the-add-in"></a><a name="install"></a>Papildinio įdiegimas

Atlikite šiuos veiksmus, kad įdiegtumėte priedą, skirtą Visuotinės atsargų apskaitos naudojimui.

1. Prisijunkite prie [LCS](https://lcs.dynamics.com/Logon/Index).
1. Atidarykite LCS aplinką, į kurią norite įtraukti paslaugą.
1. Eikite į **Išsami informacija**.
1. Eikite į **„Power Platform” integravimas** ir pasirinkite **Nustatymas**.
1. Dialogo lange **„Power Platform” aplinkos nustatymas** pasirinkite žymės langelį, o tada – **Nustatymas**. Įprastai nustatymas trunka nuo 60 iki 90 minučių.
1. Užbaigę „Microsoft Power Platform” aplinkos nustatymą, „FastTab” **Aplinkos papildiniai** pasirinkite **Diegti naują priedą**.
1. Pasirinkite **Visuotinė atsargų apskaita**.
1. Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.
1. Pasirinkti **Diegti**.
1. „FastTab” **Aplinkos papildiniai** turėtumėte matyti, kad Visuotinė atsargų apskaita yra diegiama. Po kelių minučių būsena turėtų pasikeisti iš *Diegiama* į *Įdiegta*. (Gali reikėti atnaujinti puslapį, kad pamatytumėte šį pakeitimą.) Tada Visuotinė atsargų apskaita bus parengta naudoti.

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
