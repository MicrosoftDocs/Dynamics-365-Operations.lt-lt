---
title: WHS prekių „Inventory Visibility“ palaikymas
description: Šioje temoje aprašomas prekių, kurios įgalintos išplėstiniams sandėlio procesams (WHS prekėms), atsargų matomumo palaikymas.
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: cfbff05697f4159cb74d110887b8029f28fbf96b
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625429"
---
# <a name="inventory-visibility-support-for-whs-items"></a>WHS prekių „Inventory Visibility“ palaikymas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas prekių, kurios įgalintos išplėstiniams sandėlio procesams (WHS prekėms), atsargų matomumo palaikymas. Funkcija, kuri įtraukia šią galimybę į atsargų matomumą, vadinama išplėstiniais sandėlio *valdymo sistemos funkcija*.

## <a name="whs-items"></a>Sandėlio kasos sandėlio sandėlio prekės

Sandėlio valdymo proceso prekė yra prekė, kuri įjungta išplėstiniams sandėlio procesams (WHS) ir apdorojama sandėlyje, kuriame taip pat įjungtas sandėlio valdymo procesas.

Daugiau informacijos apie sandėlio valdymo ir sandėlio valdymo **modulį** "Microsoft" Dynamics 365 Supply Chain Management ieškokite sandėlio [valdymo apžvalga](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Priemonės apimtis

Išplėstinės sandėlio valdymo (WHS) funkcija, skirta atsargų matomumo židiniams, skirti turimo kiekio skaičiavimams, pagrįstiems turimo kiekio užklausomis. Ši funkcija nėra skirta leisti naudoti atsargų matomumą norint bendrai valdyti sandėlio apdorojimo veiklas. Atsargų matomumas neturi tam tikrų sandėlio sąvokų savo vartotojams. Štai keletas šių sąvokų pavyzdžių:

- Rezervavimo hierarchija
- Ar įgalintas prekės arba sandėlio sandėlio valdymo procesų raktas
- Vienetų sekų grupės ID
- Sandėliui konkretūs procesai, pvz., siuntos, kroviniai, bangos ir darbas

Ši informacija, paremta duomenimis, siunčiamais iš tiekimo grandinės valdymo, rodo atsargų matomumą. Konkretūs sandėlio sandėlio duomenys (kitaip tariant, lentelės `WHSInventReserve` duomenys) nematomi vartotojams.

Kai atsargų matomumui naudojate išplėstinę WHS funkciją, visi užklausos rezultatai bus identiški užklausų, tiesiogiai gaminamų tiekimo grandinės valdymo funkcijai, rezultatams. Tačiau jos nebus identiškos užklausų, kurios buvo pagamintos naudojant sandėlio valdymo mobiliąją programą, rezultatams, nes mobiliųjų įrenginių programa šiek tiek naudoja kitokią skaičiavimo logiką.

## <a name="when-to-use-the-feature"></a>Kada naudoti funkciją

Rekomenduojame naudoti funkciją Išplėstiniai sandėlio valdymo valdymo parametrai atsargų matomumui nustatyti, kai tenkinamos visos šios sąlygos:

- Sinchronizuojate tiekimo grandinės valdymo duomenis su atsargų matomumu.
- Tiekimo grandinės valdymo metu naudojate WHS.
- Vartotojai rezervuos sandėlio valdymo procesų prekes ne sandėlio lygiu (pvz., todėl, kad naudojate sandėlio darbą).

Kituose scenarijuose turimų atsargų užklausų rezultatai bus vienodi, nepaisant to, ar įgalinta atsargų matomumo išplėstinio WHS funkcija. Be to, jei šių scenarijų funkcijos įjungsite ne taip, bus geriau veikia našumas, nes yra mažiau skaičiavimų ir mažiau papildomų duomenų.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>Įjungti išplėstinę sandėlio valdymo funkciją atsargų matomumui nustatyti

Norėdami įjungti atsargų matomumo išplėstinę WHS funkciją, atlikite šiuos veiksmus.

1. Prisijungti prie tiekimo grandinės valdymo kaip administratorius.
1. Atidarykite [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį ir įgalinkite šias priemones šia tvarka:

    1. *Atsargų matomumo integravimas*
    1. *Įgalinti sandėlio prekes atsargų matomumo skiltyje*

1. Eikite į **Atsargų valdymas \> Sąranka \> Atsargų ir sandėlio matomumo integravimo parametrai**.
1. Skirtuke **Įgalinti sandėlio sandėlio sandėlio** prekes nustatykite parinktį **Įgalinti sandėlio parinktis** *Taip*.
1. Prisijungti prie „Power Apps”.
1. Atidarykite **konfigūracijos** puslapį, tada funkcijų valdymo **skirtuke** įjunkite funkciją *AdvancedWHS*.
1. Tiekimo grandinės valdymo srityje eikite į atsargų **valdymo periodinių užduočių \> atsargų \> matomumo integravimą**.
1. Veiksmų srityje pasirinkite Uždrausti, kad **laikinai** išjungtumėte atsargų matomumą.
1. Veiksmų srityje pasirinkite Įgalinti **, kad** atsargų matomumą būtų galima pakeisti. Priedas įkeliamas iš naujo ir dabar įgalinta nauja funkcija. Su sandėlio valdymo procesas susiję duomenys pradedama sinchronizuoti su atsargų matomumu.

## <a name="query-on-hand-quantities-of-whs-items"></a>Pateikti užklausą dėl sandėlio ir sandėlio sandėlio prekių turimo kiekio

Norėdami pateikti užklausą dėl sandėlio valdymo sistemos prekių, naudojate tą pačią programos programavimo sąsają (API) [ir pranešimo sintaksę,](inventory-visibility-api.md) kurią naudojate ne WHS prekėms. Jums nereikia nurodyti, ar prekė yra whS prekė, ar ne WHS prekė. Atsargų matomumas automatiškai atskiria prekes pagal saugomus duomenis.

WhS prekių užklausų rezultatai iš esmės yra tokie patys, kaip ir ne WHS prekių rezultatai. Vienintelis skirtumas yra tai, kad šie faktiniai duomenų šaltinio `fno` duomenys apskaičiuojami remiantis tiekimo grandinės valdymo sandėlio valdymo logika:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Visi kiti faktiniai priemonės skaičiuojamos taip pat, kaip kai išjungta atsargų matomumo išplėstinių WHS funkcija.

Išsamesnės informacijos apie tai, kaip veikia sandėlio valdymo sistemos prekių turimi skaičiavimai, [ieškokite sandėlio valdymo baltosios knygos rezervavimuose](https://www.microsoft.com/download/details.aspx?id=43284).

Duomenų objektai, eksportuoti į dar Dataverse negalima atnaujinti sandėlio sandėlio prekių kiekių. Kiekiai, rodomi duomenų objektuose, yra tinkami ir ne WHS prekėms, ir kiekiams, kurių neveikia WHS logika (t.vz., priemonės, `AvailPhysical` išskyrus, `AvailOrdered``ReservPhysical``ReservOrdered``fno` ir duomenų šaltinyje).

Gamybos valdymo sistemos prekių kiekių, saugomų tiekimo grandinės valdymo duomenų šaltinyje, pakeitimus draudžiama. Šis apribojimas taikomas, kaip ir kitoms atsargų matomumo funkcijoms, kad išvengtų konfliktų.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>Švelniai sandėlio valdymo ir valdymo prekių rezervavimas atsargų matomumo metu

Bendrai palaikomas [soft rezervavimas](inventory-visibility-reservations.md) sandėlio sandėlio sandėlio prekėms. Galite įtraukti su sandėlio valdymo sandėliu susijusius faktinius duomenis į soft reservation skaičiavimą. 

Žinomame apribojime, galimas *rezervavimo skaičiavimas* šiuo metu nepalaikomas sandėlio prekėse. Todėl jei rezervavimas viršija dabartines dimensijas, kuriose vyksta švelniai rezervavimas, *galimas rezervavimo skaičiavimas* yra klaidingas. Soft rezervavimai nebus paveikti, kai parinktisCheckAvailForReserv **yra** išjungta soft [reservation API](inventory-visibility-api.md#create-one-reservation-event).

Šis apribojimas taip pat taikomas funkcijoms ir pritaikymams, kurie pagrįsti švelniais rezervavimais (pvz., paskirstymu).

## <a name="calculate-available-to-promise-quantities"></a>Apskaičiuoti prieinamų prekių kiekius

Sprendimas visiškai palaiko prieinamus [prieinamus pasižadėti (ATP) sandėlio](inventory-visibility-available-to-promise.md) sandėlio sandėlio elementams. AtP skaičiavimus galima nustatyti nepaisant sandėlio informacijos, konkrečios sandėlio informacijos.
