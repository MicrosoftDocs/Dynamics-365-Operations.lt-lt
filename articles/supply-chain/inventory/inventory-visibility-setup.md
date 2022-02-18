---
title: Įdiekite Inventoriaus matomumo papildinį
description: Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „ Microsoft Dynamics 365 Supply Chain Management“.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a49f35211f30cdb76104cc5be78f5b114320a228
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062655"
---
# <a name="install-and-set-up-inventory-visibility"></a>Atsargų matomumo nustatymas ir diegimas

[!include [banner](../includes/banner.md)]


Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „ Microsoft Dynamics 365 Supply Chain Management“.

Jums būtina naudoti „Microsoft Dynamics Lifecycle Services“ (LCS) siekiant įdiegti inventoriaus matomumo papildinį. LCS yra bendradarbiavimo portalas suteikiantis aplinką ir reguliariai naujinamų paslaugų rinkinį, kuris padeda jums valdyti programos gyvavimo ciklą jūsų „finance and operations“ programose.

Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Atsargų matomumo išankstinės sąlygos

Prieš jums įdiegiant inventoriaus matomumo papildinį, atlikite šiuos veiksmus:

- Gaukite LCS diegimo projektą su mažiausiai viena patalpinta aplinka.
- Įsitikinkite, kad baigtos būtinosios priedų nustatymo sąlygos, pateikiamos skyriuje Priedų apžvalga buvo patenkintos. Informacijos apie šias būtinąsias sąlygas rasite [Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Atsargų matomumui nereikia dvigubo rašymo susiejimo.

> [!NOTE]
> Šiuo metu palaikomos šalys ir regionai yra Kanada (HOU, ECA), Jungtinės Valstijos (ISPANIJOS, ESS), Europos Sąjunga (NEU, WEU), Jungtinė Karalystė (SUK,VZK) ir Australija (HOU, SEAU), Japonija (EJP, WJP) ir Brazilija (SBR, SCUS).

Jei turite kokių klausimų apie šias būtinąsias sąlygas, susisiekite su papildinio produkto komanda [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Įdiekite Inventoriaus matomumo papildinį

Prieš įdiegsdami priedą, užregistruokite programą ir pridėkite kliento slaptažodį Azure Active Directory (Azure AD) pagal savo „Azure" abonementą. Instrukcijų ieškokite Registruoti [programą ir Pridėti kliento](/azure/active-directory/develop/quickstart-register-app) ir [Įtraukti kliento raktą](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Įsitikinkite, kad užsirašėte **Programos (kliento) ID**, **Kliento raktą**, ir **Nuomotojo ID** vertes, nes Jums jų reikės vėliau.

Kai užregistruojate programą ir pridedate kliento slaptą seką, atlikite šiuos veiksmus, kad įdiegtumėte atsargų „Azure AD“ matomumo priedą.

1. Prisijunkite prie [LCS](https://lcs.dynamics.com/Logon/Index).
1. Pagrindiniame puslapyje pasirinkite projektą, kuriame jūsų aplinka talpinta.
1. Projekto puslapyje pasirinkite aplinką, kurioje norite įdiegti papildinį.
1. Aplinkos puslapyje slinkite žemyn, kol pamatysite skyrių **Aplinkos priedai** skyriuje **„Power Platform“ integravimas** skyriuje. Ten galite rasti aplinkos „Dataverse“ pavadinimą. „Dataverse“ patvirtinkite, kad aplinkos pavadinimas yra tas, kurį norite naudoti atsargų matomumui.

    > [!NOTE]
    > Šiuo metu „Dataverse“ palaikomos tik aplinkos, kurios sukurtos naudojant LCS. Jei jūsų aplinka „Dataverse“ buvo sukurta kokiu nors kitu būdu (pavyzdžiui, naudojant „Power Apps“ administravimo centrą), ir jei ji susieta su jūsų „Supply Chain Management“ aplinka, pirmiausia turite susisiekti su atsargų matomumo produktų komanda, kad išspręskite susiejimo [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) problemą. Galite tada įdiekti Inventoriaus matomumo papildinį.

1. Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.

    ![Aplinkos puslapis LCS](media/inventory-visibility-environment.png "Aplinkos puslapis LCS")

1. Rinkitės **Diegti naują papildinį** nuorodą. Pasirodo esamų atvirų papildinių sąrašas.
1. Sąraše rinkitės **Atsargų matomumas**.
1. Tada nustatykite šiuos laukus savo aplinkai:

    - **AAD programos (kliento) ID** – Įveskite „Azure AD“ programos ID, kurią sukūrėte ir anksčiau užsirašėte.
    - **ADD nuomotojo ID** – Įveskite anksčiau pasižymėtą nuomotojo ID.

    ![Įtraukite į papildinių puslapį](media/inventory-visibility-setup.png "Įtraukite į papildinių puslapį")

1. Sutikite su sąlygomis ir terminais pasirinkę **Sąlygos ir terminai** žymimą laukelį.
1. Pasirinkti **Diegti**. Papildinio būsena bus rodoma kaip **diegiama**. Tada, kai diegimas bus baigtas, paleiskite iš naujo puslapį. Būsena turi pasikeisti į **Įdiegta**.
1. Kairiajame „Dataverse“ naršymo lange **pasirinkite** Programėlių **skyrių ir patikrinkite** ar atsargų matomumas sėkmingai „Power Apps“ įdiegtas. Jei **Programos** skyrius neegzistuoja, susisiekite su atsargumo matomumo produkto komanda [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!TIP]
> Rekomenduojame prisijungti prie atsargų matomumo priedo vartotojų grupės, kurioje galite rasti naudingų vadovų, gauti naujausius atnaujinimus ir paskelbti visus klausimus, susijusius su Inventorių matomumo naudojimu. Norėdami prisijungti, atsiųskite el. laišką Inventoriaus matomumo produktų komandai adresu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) ir įtraukite savo tiekimo grandinės valdymo aplinkos ID.

> [!IMPORTANT]
> Jei turite daugiau nei vieną LCS aplinką, kiekvienai aplinkai „Azure AD“ sukurkite kitą programą. Jei norėdami įdiegti atsargų matomumo priedą skirtingoms aplinkai naudojate tą patį programos ID ir nuomininko ID, atpažinimo ženklo išdavimas bus taikomas senesnėms aplinkai. Galios tik paskutinė įdiegta versija.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Išdiekite Inventoriaus matomumo papildinį

Norėdami pašalinti atsargų matomumo priedą, **Išdiegti** LCS puslapyje pasirinkite. Pašalinimo procesas pašalina atsargų matomumo priedą, išregistruojami iš LCS ir panaikinami visi laikini duomenys, saugomi atsargų matomumo duomenų talpykloje. Tačiau pirminiai atsargų duomenys, saugomi jūsų „Dataverse“ abonemente, nėra naikinami.

Norėdami pašalinti savo abonemente saugomus atsargų duomenis, savo „Dataverse“ prenumeratoje atverkite [„Power Apps“](https://make.powerapps.com), rinkitės **Aplinka** naršymo juostoje ir rinkitės „Dataverse“ aplinką, kuri yra susieta su Jūsų LCS aplinka. Tada eikite į **sprendimus** ir panaikinkite šiuos penkis sprendimus šiame užsakyme:

1. Atsargų matomumo programos inkaro sprendimas „Dynamics 365" sprendimuose
1. „Dynamics 365" FNO SCM atsargų matomumo programų sprendimas
1. Atsargų saugumo konfigūravimas
1. Atsargų matomumo atskiras dėmuo
1. „Dynamics 365" FNO SCM atsargų matomumo pagrindo sprendimas

Kai panaikinate šiuos sprendimus, duomenys, saugomi lentelėse, taip pat bus panaikinti.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Nustatyti atsargų matomumą „Supply Chain Management“ dalyje

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Aplinkos matomumo integravimo paketo diegimas

Jei naudojate „Supply Chain Management” 10.0.17 ar senesnę versiją, susisiekite su atsargų matomumo samdymo palaikymo komanda el. paštu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte paketo failą. Tada įdiekite paketą LCS.

> [!NOTE]
> Jei diegiant įvyksta versijų neatitikimo klaida, turite rankiniu būdu importuoti X++ projektą į savo programavimo aplinką. Tada sukurkite diegiamą paketą savo programavimo aplinkoje ir įdiekite jį savo gamybos aplinkoje.
>
> Kodas įtrauktas į „Supply Chain Management” 10.0.18 versiją. Jei naudojate tą ar vėlesnę versiją, įdiegti nereikia.

Įsitikinkite, kad šios priemonės yra įjungtos jūsų „Supply Chain Management” aplinkoje. (Numatyta, kad jos yra įjungtos.)

| Funkcijos aprašymas | Kodo versija | Klasės kaitaliojimas |
|---|---|---|
| Atsargų dimensijų naudojimo „InventSum“ lentelėje įjungimas arba išjungimas      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Atsargų dimensijų naudojimo „InventSumDelta“ lentelėje įjungimas arba išjungimas | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Atsargų matomumo integravimo nustatymas

Įdiegę priedą parenkite savo „Supply Chain Management“ sistemą dirbti su juo atlikdami nurodytus veiksmus.

1. „Supply Chain Management“ atverkite **[Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbo sritį ir tada įjunkite tokias funkcijas:
    - *Atsargų matomumo integravimas* – Būtinas.
    - *Atsargų matomumo integravimas su rezervavimo korespondentinė sąskaita* – rekomenduojama, bet pasirinktinai. Reikia 10.0.22 arba naujesnės versijos. Dėl daugiau informacijos, žr. [Inventoriaus matomumo rezervavimas](inventory-visibility-reservations.md).

1. Eikite į **Atsargų valdymas \> Nustatymas \> Atsargų ir sandėlio integravimo parametrai**.
1. Atidarykite skirtuką **Bendra** ir atlikite šiuos parametrus:
    - **Atsargų matomumo galinis punktas** – įveskite aplinkos, kurioje vykdomas atsargų matomumas, URL. Daugiau informacijos žr. [Surasti paslaugų galinį tašką](inventory-visibility-configuration.md#get-service-endpoint).
    - **Didžiausias įrašų skaičius vienoje užklausoje** – nustatykite didžiausią įrašų, kuriuos reikia įtraukti į vieną užklausą, skaičių. Turite įvesti teigiamą s integerį, mažesnį arba lygų 1000. Numatytoji vertė yra 512. Primygtinai rekomenduojame išsaugoti numatytąją vertę, nebent gavote „Microsoft Support" rekomendacijų arba esate tikri, kad ją reikia pakeisti.

1. Jei įgalinote pasirinktinį *atsargų matomumo integravimą su rezervavimo korespondentinės* sąskaitos funkcija, atidarykite skirtuką **Rezervavimas ir atlikite** šiuos parametrus:
    - **Įgalinti rezervavimo korespondentinę sąskaitą** – nustatykite kaip *Taip*, norėdami įgalinti šią funkciją.
    - **Rezervavimo korespondentinis modifikatorius** – pasirinkite atsargų operacijos būseną, kuri koresponduos rezervavimus, atliktas atsargų matomumo metu. Šis parametras nustato užsakymo apdorojimo etapą, kuris suaktyvina kompensavimus. Etapą seka užsakymo atsargų operacijos būsena. Pasirinkite vieną iš šių parinkčių:
        - *Užsakyta* – kai operacijos būsena Yra, sukūrus užsakymą, *užsakymas* atsiųs korespondentinę užklausą. Korespondentinis kiekis bus sukurto užsakymo kiekis.
        - *Rezervas* – kai *operacijos būsena Rezervuota,* Užsakytas užsakymas siųs korespondentinę užklausą, kai ji rezervuota, paimta, užregistruotas važtaraštis arba išrašyta SF. Užklausa bus suaktyvinta tik vieną kartą, pirmojo žingsnio atveju, kai bus įvyksta nurodytas procesas. Korespondentinis kiekis bus kiekis, kai atsargų operacijos būsena atitinkamoje užsakymo eilutėje pasikeičia iš *Užsakyta* į *Rezervuota* (arba vėlesnė būsena).

1. Eikite į **Atsargų valdymas \> Periodinis \> Atsargų matomumo integravimas** ir įjunkite užduotį. Visi atsargų keitimo įvykiai iš „Supply Chain Management” dabar bus užregistruoti atsargų matomumo srityje.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
