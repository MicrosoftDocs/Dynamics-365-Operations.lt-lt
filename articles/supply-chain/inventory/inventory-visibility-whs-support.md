---
title: WMS prekių „Inventory Visibility“ palaikymas
description: Šiame straipsnyje aprašomas prekių, kurios įgalintos sandėlio valdymo procesams (WMS prekėms), atsargų matomumo palaikymas.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762760"
---
# <a name="inventory-visibility-support-for-wms-items"></a>WMS prekių „Inventory Visibility“ palaikymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas prekių, kurios įgalintos sandėlio valdymo procesams (WMS), atsargų matomumo palaikymas. Funkcija, kuri įtraukia šią galimybę į atsargų matomumą, vadinama išplėsta *WMS*.

## <a name="wms-items"></a>WMS prekės

WMS prekė yra prekė, kurią galima naudoti WMS ir apdoroti sandėlyje, kuriame taip pat įgalinta WMS.

Daugiau informacijos apie WMS ir "Microsoft" sandėlio **valdymo** modulį Dynamics 365 Supply Chain Management ieškokite Sandėlio [valdymo peržiūra](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Priemonės apimtis

Išplėstinė WMS funkcija, skirta atsargų matomumo židiniams, skirti turimo kiekio skaičiavimams, pagrįstiems turimo kiekio užklausomis. Ši funkcija nėra skirta leisti naudoti atsargų matomumą norint bendrai valdyti sandėlio apdorojimo veiklas. Atsargų matomumas neturi tam tikrų sandėlio sąvokų savo vartotojams. Štai keletas šių sąvokų pavyzdžių:

- Rezervavimo hierarchija
- Ar prekė arba sandėlis yra įgalinti WMS
- Vienetų sekų grupės ID
- Sandėliui konkretūs procesai, pvz., siuntos, kroviniai, bangos ir darbas

Ši informacija, paremta duomenimis, siunčiamais iš tiekimo grandinės valdymo, rodo atsargų matomumą. WMS konkretūs duomenys (kitaip tariant, lentelės duomenys `WHSInventReserve`) nematomi vartotojams.

Kai naudojate išplėstinę WMS funkciją atsargų matomumui nustatyti, visi užklausos rezultatai bus identiški užklausų, tiesiogiai gaminamų tiekimo grandinės valdymo funkcijai, rezultatams. Tačiau jos nebus identiškos užklausų, kurios buvo pagamintos naudojant sandėlio valdymo mobiliąją programą, rezultatams, nes mobiliųjų įrenginių programa šiek tiek naudoja kitokią skaičiavimo logiką.

## <a name="when-to-use-the-feature"></a>Kada naudoti funkciją

Rekomenduojame pasirinkti WMS funkciją atsargų matomumui scenarijuose, kuriuose yra įvykdytos visos šios sąlygos:

- Sinchronizuojate tiekimo grandinės valdymo duomenis su atsargų matomumu.
- WMS naudojate tiekimo grandinės valdymo srityje.
- Vartotojai rezervuos WMS prekes po sandėlio lygiu (pvz., numerio lentelės lygiu, nes apdorosite sandėlio darbą).

Kituose scenarijuose turimų atsargų užklausų rezultatai bus vienodi, nepaisant to, ar įgalinta atsargų matomumo išplėstinė WMS funkcija. Be to, jei šių scenarijų funkcijos įjungsite ne taip, bus geriau veikia našumas, nes yra mažiau skaičiavimų ir mažiau papildomų duomenų.

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>Įjungti WMS funkciją atsargų matomumui

Norėdami įjungti WMS funkciją atsargų matomumui, atlikite šiuos veiksmus.

1. Prisijungti prie tiekimo grandinės valdymo kaip administratorius.
1. Atidarykite [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį ir įgalinkite šias priemones šia tvarka:

    1. *Atsargų matomumo integravimas*
    1. *Įgalinti sandėlio prekes atsargų matomumo skiltyje*

1. Eikite į **Atsargų valdymas \> Sąranka \> Atsargų ir sandėlio matomumo integravimo parametrai**.
1. Skirtuke **Įgalinti WMS prekes** nustatykite parinktį **Įgalinti WMS prekes** kaip *Taip*.
1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **konfigūracijos** puslapį, tada funkcijų valdymo **skirtuke** įjunkite funkciją *AdvancedWHS*.
1. Tiekimo grandinės valdymo srityje eikite į atsargų **valdymo periodinių užduočių \> atsargų \> matomumo integravimą**.
1. Veiksmų srityje pasirinkite Uždrausti, kad **laikinai** išjungtumėte atsargų matomumą.
1. Veiksmų srityje pasirinkite Įgalinti **, kad** atsargų matomumą būtų galima pakeisti. Priedas įkeliamas iš naujo ir dabar įgalinta nauja funkcija. Su WMS susiję duomenys pradedama sinchronizuoti su atsargų matomumu.

## <a name="query-on-hand-quantities-of-wms-items"></a>Pateikti užklausą dėl WMS prekių turimos kiekio

Norėdami pateikti WMS prekių užklausą naudokite tą pačią [programos programavimo sąsają (API)](inventory-visibility-api.md) ir pranešimo sintaksę, kurią naudojate ne WMS prekėms. Jums nereikia nurodyti, ar prekė yra WMS prekė, ar ne WMS prekė. Atsargų matomumas automatiškai atskiria prekes pagal saugomus duomenis.

WMS prekių užklausų rezultatai iš esmės yra tokie patys, kaip ir ne WMS prekių rezultatai. Vienintelis skirtumas yra tai, kad šie faktiniai duomenų `fno` šaltinio duomenys apskaičiuojami remiantis tiekimo grandinės valdymo WMS logika:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Visi kiti faktiniai priedai skaičiuojami taip pat, kaip kai išjungta WMS atsargų matomumo funkcija.

Išsamesnės informacijos apie tai, kaip veikia WMS prekių turimi skaičiavimai, [ieškokite sandėlio valdymo baltosios knygos rezervavimuose](https://www.microsoft.com/download/details.aspx?id=43284).

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>Turimų atsargų sąrašo rodinys ir duomenų objektas WMS prekėms

Iš **anksto įkelkite atsargų matomumo suvestinės** puslapį, kad būtų galima peržiūrėti turimos indekso *užklausos iš anksto įkelti rezultatų objektą*. Skirtingai nei *atsargų suvestinės objektas*, *turimų* atsargų indekso užklausos išankstinio įkėliaus rezultatų objektas pateikia produktų su pasirinktomis dimensijomis turimų atsargų sąrašą. Atsargų matomumas sinchronizuoja iš anksto įkeltus suvestinės duomenis kas 15 minučių.

Jei atsargų matomumą naudojate su WMS prekėmis ir norite peržiūrėti WMS prekių turimų atsargų sąrašą, *rekomenduojame* įgalinti atsargų matomumo suvestinės funkciją iš anksto ([taip](inventory-visibility-power-platform.md#preload-streamlined-onhand-query) pat žr. iš anksto įkelti supaprastintą turimų atsargų užklausą). Atitinkamas duomenų objektas saugomas Dataverse jūsų užklausos išankstinio įkelties rezultate, kuris atnaujinamas kas 15 minučių. Duomenų objekto pavadinimas yra `Onhand Index Query Preload Result`.

> [!IMPORTANT]
> Objektą Dataverse leidžiama tik skaityti. Galite peržiūrėti ir eksportuoti duomenis, esančių atsargų matomumo objektuose, bet **nekeiskite**.

WMS prekių kiekių, saugomų tiekimo grandinės valdymo duomenų šaltinyje, pakeitimai yra`fno` draudžiami. Šis veikimo būdas atitinka kitų atsargų matomumo funkcijų elgseną. Šis apribojimas taikomas, kad būtų išvengta konfliktų.

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>WMS prekės suderinamumas su kitomis atsargų matomumo funkcijomis

[Palaikomi WMS](inventory-visibility-reservations.md)[prekių švelniai rezervavimai](inventory-visibility-allocation.md) ir atsargų paskirstymas. Galite įtraukti su WMS susijusius faktinius duomenis į tam tikrą rezervavimą ir paskirstymo skaičiavimus.

## <a name="calculate-available-to-promise-quantities"></a>Apskaičiuoti prieinamų prekių kiekius

Sprendimas visiškai palaiko WMS [prekių prieinamų prekių prieinamą](inventory-visibility-available-to-promise.md) atsargos (ATP). Galite nurodyti ATP skaičiavimus nenaudodami WMS konkrečios informacijos.
